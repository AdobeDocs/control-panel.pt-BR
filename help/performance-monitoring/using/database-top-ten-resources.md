---
product: campaign
solution: Campaign
title: Os 10 principais recursos temporários
description: Saiba como usar o painel de controle para monitorar os 10 maiores recursos temporários gerados por fluxos de trabalho e entregas no banco de dados do Campaign.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: 2fa2ffbb-102b-42c4-8feb-b0263ee9c930
TQID: 'https://experienceleague.adobe.com/HeAm1BE6NkD-6rtbBXrHlJ-5KpgipvlH7UsHmPw2M-E'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ae9127b0-c11d-467b-903d-a84cef43f6ed
    internal-label: Control Panel
  - id: c5474392-5419-4296-9e41-f6f4ce4f6e9b
    internal-label: Administration
subfeature_v2:
  - id: e519a22f-a06a-42fc-9d09-d78a3ab2c434
    internal-label: Monitoring guidelines
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 100%
---
# Os 10 principais recursos temporários {#top-10}

A área **[!UICONTROL 10 principais recursos temporários]** lista os 10 maiores recursos temporários gerados por fluxos de trabalho e entregas.

Monitorar fluxos de trabalho e entregas que estão criando grandes recursos temporários é uma etapa essencial para monitorar seu banco de dados. Se qualquer recurso temporário estiver consumindo muito espaço no banco de dados, verifique se esse fluxo de trabalho ou entrega é necessário e navegue até sua instância para interrompê-lo.

>[!IMPORTANT]
>
>A recomendação geral é evitar ter **mais de 40 colunas** em recursos qua não já vêm prontos para uso. Se um fluxo de trabalho tiver muitas tabelas ou um banco de dados grande, recomendamos examinar o workflow para investigar por que ele está gerando tantos dados.
>
>As diretrizes do Campaign Standard e Classic também estão disponíveis [nesta página](database-preventing-overload.md) para ajudar a evitar a sobrecarga do banco de dados.

![](assets/database-top10.png)

O botão **[!UICONTROL Exibir todos]** permite acessar os detalhes da **[!UICONTROL Visão geral do armazenamento]** para obter informações precisas sobre esses recursos temporários. Para obter mais informações, consulte [esta página](database-storage-overview.md).
