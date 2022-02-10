---
product: campaign
solution: Campaign
title: Monitoramento de consultas ativas
description: Saiba como monitorar consultas ativas nas instâncias do Campaign no Painel de controle.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 12e9326ba220776874654705587152bf3978949c
workflow-type: ht
source-wordcount: '118'
ht-degree: 100%

---

# Monitoramento de consultas ativas {#long-running-queries}

Á área **[!UICONTROL Active queries]**, da guia **[!UICONTROL Databases]**, lista as cinco consultas sendo executadas há mais tempo na instância selecionada.

![](assets/active-queries.png)

As colunas **[!UICONTROL Duration]** especificam há quanto tempo uma consulta está sendo executada na instância. A duração é exibida neste formato: `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Se uma das consultas estiver ativa por mais de 24 horas, você será notificado por email caso esteja inscrito no [alerta por email](email-alerting.md).
>
>Nesse caso, entre em contato com o Atendimento ao cliente para identificar e resolver o problema. Em seguida, será necessário informar o valor da coluna **[!UICONTROL PID]**, que é um identificador exclusivo da consulta.
