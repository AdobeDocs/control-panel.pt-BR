---
product: campaign
solution: Campaign
title: Monitoramento de consultas ativas
description: Saiba como monitorar consultas ativas nas instâncias do Campaign no Painel de controle do Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: 6922e132321f67e1e8122e33ead3c5e54c639763
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---

# Monitoramento de consultas ativas {#long-running-queries}

O **[!UICONTROL Active queries]** da **[!UICONTROL Databases]** A guia lista os cinco queries que estão sendo executados por mais tempo na instância selecionada.

![](assets/active-queries.png)

O **[!UICONTROL Duration]** columns especifica por quanto tempo um query está sendo executado na instância. A duração é exibida neste formato: `hh:mm:ss.ms`.

>[!IMPORTANT]
>
>Se uma das consultas estiver ativa por mais de 24 horas, entre em contato com o Atendimento ao cliente para que ele identifique e resolva o problema. Nesse caso, será necessário fornecer a eles a variável **[!UICONTROL PID]** valor da coluna , que é um identificador exclusivo para a consulta.
