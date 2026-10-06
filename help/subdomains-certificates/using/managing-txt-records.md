---
product: campaign
solution: Campaign
title: Adição de registros de verificação de site do Google a um subdomínio
description: Saiba como adicionar um registro de verificação de site do Google a um subdomínio para verificação da propriedade do domínio.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: 547ca6f2-720f-4d58-b31b-5b2611ba9156
TQID: 'https://experienceleague.adobe.com/TtF1W0tOklUuEpihvsYlxdszEujRrDXv-Ar0y3c7QX8'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ae9127b0-c11d-467b-903d-a84cef43f6ed
    internal-label: Control Panel
  - id: a7760dfc-5c44-4d77-bb68-c50b1e265c93
    internal-label: Security and privacy
subfeature_v2:
  - id: f807e46f-d823-43a9-98be-82e0b2f3a05c
    internal-label: Subdomains and certificates
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 100%
---
# Adição de registros de verificação de site do Google {#adding-a-google-txt-record}

Para garantir altas taxas de caixa de entrada e baixas taxas de spam, alguns serviços como o Google exigem a adição de um registro TXT às configurações de domínio para verificar se você é o proprietário do domínio.

Atualmente, o Gmail está entre os provedores de endereços de email mais usados. Para garantir uma boa entrega de emails para endereços Gmail, o Adobe Campaign permite adicionar registros especiais TXT de verificação de site do Google aos subdomínios para garantir que eles sejam verificados.

Para adicionar um registro TXT do Google ao subdomínio usado para enviar emails para endereços Gmail, siga estas etapas:

1. Na lista de subdomínios, clique no botão de reticências ao lado do subdomínio desejado e selecione **[!UICONTROL Detalhes do subdomínio]**.

1. Clique no botão **[!UICONTROL Adicionar registro em TXT]** e escolha **[!UICONTROL Verificação de site do Google]** na lista suspensa **[!UICONTROL Tipo de registro]**.

1. Insira o valor gerado pelas ferramentas do administrador do G Suite. Para obter mais informações, consulte [Ajuda do administrador do G Suite](https://support.google.com/a/answer/183895).

   ![](assets/txt_addtxt.png)

1. Clique no botão **[!UICONTROL Adicionar]** para confirmar.

   ![](assets/txt_txtadded.png)

Depois de adicionado, o registro TXT deve ser verificado pelo Google. Para fazer isso, navegue até as ferramentas do administrador do G Suite e inicie a etapa de verificação (consulte [Ajuda do administrador do G Suite](https://support.google.com/a/answer/183895)).

Para excluir um registro, selecione-o na lista de registros e clique no botão remover.

>[!NOTE]
>
>O único registro que pode ser excluído da lista de registros DNS é o que você adicionou anteriormente (nesse caso, o registro TXT do Google).

![](assets/do-not-localize/how-to-video.png) Conheça este recurso no vídeo usando o [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html?lang=pt-BR#subdomains-and-certificates) ou o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html?lang=pt-BR#subdomains-and-certificates)
