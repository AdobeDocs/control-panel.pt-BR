---
product: campaign
solution: Campaign
title: Sobre o gerenciamento de SFTP
description: Saiba mais sobre o gerenciamento de SFTP no Painel de controle do Campaign
testing: SSECD-836 2
feature: Control Panel
role: Architect
level: Intermediate
exl-id: b2c3be80-0d1b-4998-87ab-5280c6213f3d
source-git-commit: 4fc34b07b497c743e2ca6c182e68d6ea5c180ac9
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 16%

---

# Sobre o gerenciamento de SFTP {#about-sftp-management}

No Painel de controle, é possível interagir com todos os servidores SFTP conectados às instâncias do Campaign às quais você tem acesso. A maioria das instâncias conectou servidores SFTP (em alguns casos, as instâncias de desenvolvimento e de estágio podem não estar conectadas a servidores SFTP).

O acesso aos servidores SFTP é feito usando um software cliente SFTP, que você pode localizar e baixar online. Para se conectar a um servidor, por meio desse aplicativo cliente ou de uma API, é necessário configurar uma chave SSH pública e adicionar o endereço IP que se conecta ao servidor SFTP na lista de permissões.

O Painel de controle do Campaign permite executar as ações abaixo para gerenciar os servidores SFTP:

* Monitorar seus **capacidade de armazenamento**,
* Gerenciar **Lista de permissões de endereços IP**: adicionar ou excluir intervalos de endereços IP para um ou vários servidores,
* Gerenciar **chaves SSH públicas** para acessar seus servidores.

Informações detalhadas sobre cada uma dessas ações estão disponíveis nas seções abaixo.
