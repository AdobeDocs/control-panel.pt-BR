---
product: campaign
solution: Campaign
title: Sobre o gerenciamento de SFTP
description: Saiba mais sobre o gerenciamento de SFTP no Painel de controle
testing: SSECD-836 2
feature: Control Panel, SFTP Management
role: Admin
level: Intermediate
exl-id: b2c3be80-0d1b-4998-87ab-5280c6213f3d
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 100%

---

# Sobre o gerenciamento de SFTP {#about-sftp-management}

No Painel de controle, é possível interagir com todos os servidores SFTP conectados às instâncias do Campaign às quais você tem acesso. A maioria das instâncias contam com servidores SFTP conectados (em alguns casos, as instâncias de desenvolvimento e de estágio podem não estar conectadas a servidores SFTP).

O acesso aos servidores SFTP é realizado por meio de um software do cliente SFTP, que você pode encontrar e baixar online. Para conectar-se a um servidor, seja por meio de um aplicativo do cliente ou de uma API, é necessário configurar uma chave SSH pública e adicionar o endereço IP que se conecta ao seu servidor SFTP na lista de permissões.

O Painel de controle permite realizar as ações abaixo para gerenciar os servidores SFTP:

* Monitorar a **capacidade de armazenamento**,
* Gerenciar a **lista de permissões de endereços IP**: adicione ou exclua intervalos de endereços IP para um ou vários servidores,
* Gerenciar **chaves públicas SSH** para acessar os seus servidores.

Informações detalhadas sobre cada uma dessas ações estão disponíveis nas seções abaixo.
