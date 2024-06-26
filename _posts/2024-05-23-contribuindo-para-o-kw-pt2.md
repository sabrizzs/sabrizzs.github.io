---
title: Contribuindo para o Kworkflow (parte 2)
date: 2024-05-23 10:30:00-03:00
categories: [MAC0470, Blog]
tags: [kernel, kworkflow] 
author: <author_id>
---

Olá!

Esse post é sobre a contribuição que fizemos ao Kworkflow. Com os feedbacks que recebemos, fizemos ajustes e nosso pull request para o Kworkflow foi aceito. 

Antes, a implementação de print_files_authors só capturava e imprimia autores encontrados em uma única linha da declaração de macro MODULE_AUTHOR. Isso causava problemas quando os autores eram declarados em múltiplas linhas. Nossa modificação da função permitiu que o comando ´kw m --authors´ também capturasse e imprimisse autores em declarações de múltiplas linhas.

Recebemos algumas sugestões para melhorar a legibilidade do código, modificar alguns testes e corrigir outros pequenos problemas no arquivo ´src/maintainers.sh´. Modificamos alguns blocos de comandos para que ficassem menores e adicionamos comentários para melhorar a legibilidade.

Durante esse processo, encontramos um trecho de código que usa 'sed' e não entendemos muito bem a função dele. Com a ajuda de um mantenedor, entendemos que ele tentava resolver o mesmo problema que estávamos resolvendo, que era capturar autores em declarações de várias linhas. Decidimos remover esse código e criar novos testes para garantir a funcionalidade.

Após adicionar todas essas mudanças nos commits, atualizamos a branch do nosso fork remoto. Nossas melhorias foram aceitas e mescladas no upstream do kworkflow, primeiro no branch unstable e, posteriormente, os mantenedores irão adicionar no master. Nossa contribuição pode ser visualizada [aqui](https://github.com/kworkflow/kworkflow/commit/328449c949d5a7e71baa4bdec4ca326ebcbc77c1).

Até o próximo post!
