---
title: Contribuindo para o Kworkflow
date: 2024-05-02 10:30:00-03:00
categories: [MAC0470, Blog]
tags: [kernel, kworkflow]     # TAG names should always be lowercase
author: <author_id>
---

Olá! 

Após conhecer mais sobre o kernel do Linux, chegamos no momento de conhecer sobre o Kworkflow e contribuir para o projeto!

O Kworkflow (KW) é uma ferramenta de linha de comando criada para auxilixar os desenvolvedores do kernel do Linux.

Neste [link](https://kworkflow.org/content/howtocontribute.html#development-cycle-and-branches), é possível encontrar como contribuir para o Kworkflow.

Nessa etapa da disciplina MAC0470, o objetivo era encontrar uma issue no repositório do KW e trabalhar nela. Meu grupo achou que seria interessante trabalhar na issue [#69](https://github.com/kworkflow/kworkflow/issues/69). Essa issue trata de melhorar a função responsável por capturar e imprimir os autores dos drivers definidos através da macro MODULE_AUTHOR. 

O problema era que a função não conseguia lidar adequadamente com declarações de autores em várias linhas e assim nenhum autor era impresso. Modificamos essa função para que o comando ´kw m --authors´ também capture e imprima autores em declarações de múltiplas linhas.

Agora, estamos esperando o feedback dos mantenedores. Nosso commit pode ser visualizado [aqui](https://github.com/kworkflow/kworkflow/pull/1100/commits) e as discussões e mudanças [aqui](https://github.com/kworkflow/kworkflow/pull/1100).

Até o próximo post!

