---
product: campaign
solution: Campaign
title: Sobre o gerenciamento de SFTP
description: Saiba mais sobre o gerenciamento de SFTP no Painel de controle do Campaign
testing: SSECD-836 2
feature: Control Panel
role: Architect
level: Intermediate
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 4%

---


# Sobre o gerenciamento de SFTP {#about-sftp-management}

No Painel de controle do Campaign, é possível interagir com todos os servidores SFTP conectados às instâncias do Campaign às quais você tem acesso. A maioria das instâncias conectou servidores SFTP (em alguns casos, instâncias de desenvolvimento e estágio podem não estar conectadas a nenhum servidor SFTP).

O acesso a servidores SFTP é feito usando um software cliente SFTP, que pode ser encontrado e baixado online. Para se conectar a um servidor, por meio desse aplicativo cliente ou de uma API, é necessário configurar uma chave SSH pública e adicionar o endereço IP que se conecta ao servidor SFTP na lista de permissões.

O Painel de controle do Campaign permite executar as ações abaixo para gerenciar os servidores SFTP:

* Monitorar a **capacidade de armazenamento**,
* Gerenciar **Endereços IP para permitir a listagem**: adicionar ou excluir intervalos de endereços IP de um ou vários servidores,
* Gerencie **chaves SSH públicas** para acessar seus servidores.

Informações detalhadas sobre cada uma dessas ações estão disponíveis nas seções abaixo.
