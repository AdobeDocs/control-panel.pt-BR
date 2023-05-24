---
product: campaign
solution: Campaign
title: Os 10 principais recursos temporários
description: Saiba como monitorar no Painel de controle os 10 maiores recursos temporários gerados por workflows e deliveries no banco de dados do Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: 2fa2ffbb-102b-42c4-8feb-b0263ee9c930
source-git-commit: b17abddf6bad7e58cb7bd825cd97322427a0b21f
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 69%

---

# Os 10 principais recursos temporários {#top-10}

A área **[!UICONTROL Top 10 temporary resources]** lista os 10 maiores recursos temporários gerados por workflows e deliveries.

Monitorar workflows e deliveries que estão criando grandes recursos temporários é uma etapa essencial para monitorar seu banco de dados. Se qualquer recurso temporário estiver consumindo muito espaço no banco de dados, verifique se esse fluxo de trabalho ou delivery é necessário e navegue até sua instância para interrompê-lo.

>[!IMPORTANT]
>
>A recomendação geral é evitar ter **mais de 40 colunas** em recursos não prontos para uso. Se um fluxo de trabalho tiver muitas tabelas ou um banco de dados grande, recomendamos examinar o fluxo de tabalho para investigar por que ele está gerando tantos dados.
>
>As diretrizes para o Campaign Standard e o Classic também estão disponíveis em [esta página](database-preventing-overload.md) para ajudar a evitar a sobrecarga do banco de dados.

![](assets/database-top10.png)

A variável **[!UICONTROL View all]** permite acessar a variável **[!UICONTROL Storage overview]** detalhes para obter informações detalhadas sobre esses recursos temporários. Para obter mais informações, consulte [esta página](database-storage-overview.md).
