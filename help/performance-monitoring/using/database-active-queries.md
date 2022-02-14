---
product: campaign
solution: Campaign
title: Monitoramento de consultas ativas
description: Saiba como monitorar consultas ativas nas instâncias do Campaign no Painel de controle.
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: efad3b82a498cfc88a06479e40c3e5c75d814740
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 100%

---

# Monitoramento de consultas ativas {#long-running-queries}

Á área **[!UICONTROL Active queries]**, da guia **[!UICONTROL Databases]**, lista as cinco consultas sendo executadas há mais tempo na instância selecionada.

![](assets/active-queries.png)

As colunas **[!UICONTROL Duration]** especificam há quanto tempo uma consulta está sendo executada na instância. A duração é exibida neste formato: `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Se uma das consultas estiver ativa há mais de 24 horas, entre em contato com o Atendimento ao cliente para que eles identifiquem e resolvam o problema. Em seguida, será necessário informar o valor da coluna **[!UICONTROL PID]**, que é um identificador exclusivo da consulta.
