---
title: Contribuindo para o Kworkflow
date: 2024-05-02 10:30:00-03:00
categories: [MAC0470, Blog]
tags: [kernel, kworkflow]     # TAG names should always be lowercase
author: <author_id>
---

Olá! Após conhecer mais sobre o kernel do Linux, chegamos no momento de conhecer sobre o Kworkflow e contribuir para o projeto!

O Kworkflow (KW) é uma ferramenta de linha de comando criada para auxilixar os desenvolvedores do kernel do Linux.

Nessa etapa da disciplina MAC0470, o objetivo era encontrar uma issue no repositório do KW e trabalhar nela. Meu grupo achou que seria interessante trabalhar na issue #69. Essa issue trata de melhorar a função responsável por capturar e imprimir os autores dos drivers definidos através da macro MODULE_AUTHOR. O problema era que a função não conseguia lidar adequadamente com declarações de autores em várias linhas e assim nenhum autor era impresso. 

Modificamos essa função e estamos esperando o feedback dos mantenedores. Nosso commit pode ser visualizado [aqui](https://github.com/kworkflow/kworkflow/pull/1100/commits).

Até o próximo post!

