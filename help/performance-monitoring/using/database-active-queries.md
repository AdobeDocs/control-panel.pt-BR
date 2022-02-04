---
product: campaign
solution: Campaign
title: Monitoramento de consultas ativas
description: Saiba como monitorar consultas ativas nas instâncias do Campaign no Painel de controle.
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: 6922e132321f67e1e8122e33ead3c5e54c639763
workflow-type: ht
source-wordcount: '106'
ht-degree: 100%

---

# Monitoramento de consultas ativas {#long-running-queries}

Á área **[!UICONTROL Active queries]**, da guia **[!UICONTROL Databases]**, lista as cinco consultas sendo executadas há mais tempo na instância selecionada.

![](assets/active-queries.png)

As colunas **[!UICONTROL Duration]** especificam há quanto tempo uma consulta está sendo executada na instância. A duração é exibida neste formato: `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Se uma das consultas estiver ativa há mais de 24 horas, entre em contato com o Atendimento ao cliente para que eles identifiquem e resolvam o problema. Nesse caso, será necessário fornecer a eles o valor da coluna **[!UICONTROL PID]**, que é um identificador exclusivo para a consulta.
