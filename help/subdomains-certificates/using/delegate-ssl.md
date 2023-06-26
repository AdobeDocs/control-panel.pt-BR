---
product: campaign
solution: Campaign
title: Delegação de certificados SSL de subdomínios para a Adobe
description: Saiba como delegar certificados SSL de subdomínios ao Adobe
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 0eefdbde25c955c84ee7534976256ca4df9a686c
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 25%

---

# Delegação de certificados SSL de subdomínios para a Adobe {#delegate-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_managed_ssl"
>title="Delegação de certificados SSL de subdomínios para a Adobe"
>abstract="O Painel de controle permite que os certificados SSL de subdomínios sejam gerenciados pela Adobe. Se estiver usando CNAMEs para configurar o subdomínio, os registros de certificados serão gerados e fornecidos automaticamente para gerar um certificado na sua solução de hospedagem de domínio."

Delegar os certificados SSL dos subdomínios para o Adobe é altamente recomendado, pois o Adobe criará automaticamente o certificado e o renovará todos os anos antes da expiração do certificado.

Se você estiver usando CNAMEs para configurar uma delegação de subdomínio, o Adobe fornecerá registros de certificado para usar em sua solução de hospedagem de domínio para gerar seu certificado.

A delegação de certificados SSL para o Adobe pode ser executada ao configurar um novo subdomínio ou para subdomínios já delegados.

>[!NOTE]
>
>O SSL gerenciado pela Adobe é um recurso gratuito que está disponível para os usuários.

## Delegar novos certificados SSL de subdomínios {#new}

Para delegar certificados SSL ao configurar um novo subdomínio, habilite o **[!UICONTROL Opt for Adobe managed SSL for sub-domains]** opção do assistente de configuração de subdomínio. Os registros de certificados a serem copiados para sua solução de hospedagem serão fornecidos posteriormente no assistente de configuração. As etapas detalhadas estão documentadas em [nesta seção](setting-up-new-subdomain.md).

![](assets/cname-adobe-managed.png){width="70%" align="left"}

## Delegar certificados SSL para subdomínios já delegados {#delegated}

Para delegar certificados SSL para um subdomínio já delegado, clique no botão de reticências ao lado do subdomínio desejado e clique em **[!UICONTROL Switch to Managed SSL]**.

![](assets/delegate-ssl-list.png){width="70%" align="left"}

Uma caixa de diálogo é exibida com os registros de certificado que foram gerados automaticamente pelo Adobe. Copie esses registros, um por um ou baixando um arquivo CSV, e navegue até a solução de hospedagem de domínio para gerar o certificado correspondente.

Verifique se todos os registros de certificado foram gerados em sua solução de hospedagem de domínio. Se tudo estiver configurado corretamente, confirme a criação dos registros e clique em **[!UICONTROL Submit]**.

![](assets/delegate-ssl.png){width="70%" align="left"}
