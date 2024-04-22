---
title: Contribuindo para o kernel
date: 2024-04-21 10:30:00-03:00
categories: [MAC0470, BLOG]
tags: [kernel]
author: <author_id>
---

Olá! 

Após todos os tutoriais, chegamos na parte de contribuir para o kernel. 

Além das aulas, meu grupo se organizou através do Google Meet para que todos pudessem visualizar e contribuir com o código. Das sugestões de patch, seguimos a sugestão 01, que tinha complexidade fácil a moderada e consistia em utilizar `device_for_each_child_node_scoped()` para simplificar o tratamento de erros e evitar bugs.

Primeiro, enfrentamos algumas dificuldades para entender o código que precisávamos alterar no kernel. Então, fomos atrás de entender e encontramos alguns exemplos de contribuições anteriores que nos ajudaram exatamente no que tinhamos que fazer. E então percebi que não seria tão complicado quanto eu esperava.

A alteração que tinhamos que fazer consistia em substituir a chamada `device_for_each_child_node()` por `device_for_each_child_node_scoped` e remover a chamada `fwnode_handle_put(node)`. No final, apenas ficamos em dúvida em como testar as alterações. Agora, estamos esperando o feedback dos monitores da disciplina para saber se podemos enviar a nossa contribuição diretamente para os mantenedores do kernel.

Até o próximo post!
