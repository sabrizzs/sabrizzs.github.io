---
title: Configurando e compilando o kernel do Linux 
date: 2024-04-19 10:30:00-03:00
categories: [MAC0470, Blog]
tags: [kernel, linux, QEMU, libvirt]     # TAG names should always be lowercase
author: <author_id>
---

Olá! Esse é meu primeiro post no meu blog!

Eu iniciei o curso MAC0470 sem ter muito conhecimento sobre o kernel linux, então está sendo bem desafiador para entender tudo que está acontecendo. 

Para poder contribuir com o kernel, foi necessário seguir uma série de tutoriais disponibilizados no site do [FLUSP](https://flusp.ime.usp.br/).

O tutorial 1 consistia em configurar um ambiente de teste para o desenvolvimento do kernel Linux usando QEMU e libvirt. Comecei o tutorial e logo percebi que havia algo errado com a distro. Após algumas tentativas de consertar o erro, decidi recomeçar o tutorial do zero. 

O tutorial 2 consistia em construir o kernel Linux para ARM. Ocorreu o mesmo do tutorial 1 com o tutorial 2 e precisei recomeçar o tutorial. Ainda assim tive erros, mas depois entendi que era um problema com o parâmetro `ARCH=arm64`.

Ao longo dos tutoriais, aprendi bastante sobre as configurações e parâmetros de instalação. Tive que repetir os mesmos comandos várias vezes, porém isso fez eu entender mais o que eu estava fazendo.

Ainda estou enfrentando alguns erros com o kernel, mas logo serão resolvidos!

Até o pŕoximo post!
