---
title: Contribuindo para o kernel
date: 2024-04-21 10:30:00-03:00
categories: [MAC0470, Blog]
tags: [kernel, linux, contribuição]
author: <author_id>
---

Olá! 

Após todos os tutoriais, chegamos na parte de contribuir para o kernel. 

Além das aulas, meu grupo se organizou através do Google Meet para que todos pudessem visualizar e contribuir com o código. Das sugestões de patch, seguimos a sugestão 01, que tinha complexidade fácil a moderada e consistia em utilizar a macro `device_for_each_child_node_scoped()` para simplificar o tratamento de erros e evitar bugs.

A macro `device_for_each_child_node_scoped()` foi introduzida no commit `365130fd47af`. Essa nova versão "scoped" da macro remove a necessidade de chamar manualmente a `fwnode_handle_put()` em todo fluxo de código que precocemente deixa o loop.

Alguns drivers iteram sobre nodes de firmware (`struct fwnode_handle`) e incrementam (`_get`) uma referência para o node à medida que a iteração avança. Deixar o loop cedo requer que o driver libere (`_put`) a referência para que outros drivers possam usar esse node. Isso é uma potencial fonte de bugs caso o desenvolvedor não tome cuidado com esse detalhe. Usar essa nova macro ajuda a mitigar essa possibilidade e, aleḿ disso, faz com que o código fique mais limpo.

Apesar dessa nova macro ter sido aceita e introduzida no kernel a um certo tempo, ainda existem diversos drivers que ainda estão usando a antiga. Essa é uma boa oportunidade para refatorar o código de alguns arquivos fazendo uso dela.

Em particular o driver que modificamos é `drivers/iio/adc/ti-ads1015.c`.

Primeiro, enfrentamos algumas dificuldades para entender o código que precisávamos alterar no kernel. Então, fomos atrás de entender e encontramos alguns exemplos de contribuições anteriores que nos ajudaram exatamente no que tínhamos que fazer. E então percebi que não seria tão complicado quanto eu esperava.

A alteração que tínhamos que fazer consistia em substituir a chamada `device_for_each_child_node()` por `device_for_each_child_node_scoped` e remover a chamada `fwnode_handle_put(node)`. 

No final, apenas ficamos em dúvida em como testar as alterações. Agora, estamos esperando o feedback dos monitores da disciplina para saber se podemos enviar a nossa contribuição diretamente para os mantenedores do kernel.

Até o próximo post!
