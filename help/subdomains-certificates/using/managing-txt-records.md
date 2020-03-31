---
title: Gerenciamento de registros TXT
description: Saiba como gerenciar registros TXT para verificação de propriedade de domínio.
translation-type: tm+mt
source-git-commit: 3ce9f62be9df0f6e6a61c16ddaf3ab8ae58712ce

---


# Gerenciamento de registros TXT {#managing-txt-records}

>[!CONTEXTUALHELP]
>id=&quot;cp_siteverify_add&quot;
>title=&quot;Gerenciando registros TXT&quot;
>abstract=&quot;Alguns serviços como o Google exigem que você adicione um registro TXT às suas configurações de domínio para verificar se você é o proprietário do domínio.&quot;

## Sobre registros TXT {#about-txt-records}

Os registros TXT são um tipo de registro DNS usado para fornecer informações de texto sobre um domínio, que pode ser lido por fontes externas.

Para garantir altas taxas de caixa de entrada e baixas taxas de spam, alguns serviços como o Google exigem que você adicione um registro TXT às configurações de domínio para verificar se você é o proprietário do domínio.

Atualmente, o Gmail está entre os provedores de endereços de email mais populares. Para garantir boa entrega e delivery bem-sucedido de emails para endereços de Gmail, o Adobe Campaign permite que você adicione registros TXT de verificação de site especiais do Google aos seus subdomínios para garantir que eles sejam verificados.

## Adicionar um registro TXT do Google para um subdomínio {#adding-a-google-txt-record}

Para adicionar um registro TXT do Google ao seu subdomínio usado para enviar emails para endereços Gmail, siga estas etapas:

1. Navegue até o **[!UICONTROL Subdomain and Certificates]** cartão.

1. Selecione sua instância e abra os detalhes do subdomínio ao qual você deseja adicionar um registro DNS.

   ![](assets/txt_subdomaindetails.png)

1. Clique no **[!UICONTROL Add TXT record]** botão e digite o valor gerado nas ferramentas administrativas do G Suite. Para obter mais informações, consulte a Ajuda [administrativa do](https://support.google.com/a/answer/183895)G Suite.

   ![](assets/txt_addtxt.png)

1. Clique no **[!UICONTROL Add]** botão para confirmar.

   ![](assets/txt_txtadded.png)

Depois que o registro TXT é adicionado, é necessário que seja verificado pelo Google. Para fazer isso, navegue até as ferramentas administrativas do G Suite e, em seguida, inicie a etapa de verificação (consulte a Ajuda [do administrador do](https://support.google.com/a/answer/183895)G Suite).


Para excluir um registro, selecione-o na lista de registros e clique no botão remover.

>[!NOTE]
>
>O único registro que você pode excluir da lista de registros DNS é aquele que você adicionou anteriormente (no nosso caso, o registro TXT do Google).