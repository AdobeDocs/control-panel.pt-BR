---
product: campaign
solution: Campaign
title: Adicionar registros de verificação de site do Google para um subdomínio
description: Saiba como adicionar um registro de Verificação de site do Google para um subdomínio para verificação de propriedade de domínio.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: 547ca6f2-720f-4d58-b31b-5b2611ba9156
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 83%

---

# Adicionar registros de verificação de site do Google {#adding-a-google-txt-record}

Para garantir altas taxas de caixa de entrada e baixas taxas de spam, alguns serviços como o Google exigem a adição de um registro TXT às configurações de domínio para verificar se você é o proprietário do domínio.

Atualmente, o Gmail está entre os provedores de endereços de email mais usados. Para garantir uma boa entrega de emails para endereços Gmail, o Adobe Campaign permite adicionar registros especiais TXT de verificação de site do Google aos subdomínios para garantir que eles sejam verificados.

Para adicionar um registro TXT do Google ao subdomínio usado para enviar emails para endereços Gmail, siga estas etapas:

1. Na lista de subdomínios, clique no botão de reticências ao lado do subdomínio desejado e selecione **[!UICONTROL Subdomain details]**.

1. Clique no botão **[!UICONTROL Add TXT record]** e escolha **[!UICONTROL Google Site Verification]** na lista suspensa **[!UICONTROL Record Type]**.

1. Insira o valor gerado nas ferramentas do administrador do G Suite. Para obter mais informações, consulte [Ajuda do administrador do G Suite](https://support.google.com/a/answer/183895).

   ![](assets/txt_addtxt.png)

1. Clique no botão **[!UICONTROL Add]** para confirmar.

   ![](assets/txt_txtadded.png)

Depois de adicionado, o registro TXT deve ser verificado pelo Google. Para fazer isso, navegue até as ferramentas do administrador do G Suite e inicie a etapa de verificação (consulte [Ajuda do administrador do G Suite](https://support.google.com/a/answer/183895)).

Para excluir um registro, selecione-o na lista de registros e clique no botão remover.

>[!NOTE]
>
>O único registro que pode ser excluído da lista de registros DNS é o que você adicionou anteriormente (nesse caso, o registro TXT do Google).

![](assets/do-not-localize/how-to-video.png) Descubra este recurso no vídeo usando o [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html#subdomains-and-certificates) ou o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html#subdomains-and-certificates)
