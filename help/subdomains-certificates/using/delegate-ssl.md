---
product: campaign
solution: Campaign
title: Delegação de certificados SSL de subdomínios para a Adobe
description: Saiba como delegar seus certificados SSL de subdomínios para a Adobe
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: a2b3d409-704b-4e81-ae40-b734f755b598
source-git-commit: 31d181770474428a7b42e96f2e603cc820db48d4
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 61%

---

# Delegação de certificados SSL de subdomínios para a Adobe {#delegate-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_managed_ssl"
>title="Delegação de certificados SSL de subdomínios para a Adobe"
>abstract="O Painel de controle permite que os certificados SSL de subdomínios sejam gerenciados pela Adobe. Se estiver usando CNAMEs para configurar o subdomínio, os registros de certificados serão gerados e fornecidos automaticamente para gerar um certificado na sua solução de hospedagem de domínio."

É altamente recomendado delegar seus certificados SSL de subdomínios para a Adobe, pois ela criará automaticamente o certificado e o renovará todos os anos antes da expiração.

Se estiver usando CNAMEs para configurar uma delegação de subdomínio, a Adobe fornecerá registros de certificado para usar em sua solução de hospedagem de domínio e gerar seu certificado.

A delegação de certificados SSL para a Adobe pode ser executada ao configurar um novo subdomínio ou em subdomínios já delegados.

>[!NOTE]
>
>O SSL gerenciado pela Adobe é um recurso gratuito que está disponível para usuários. Delegar o certificado de um subdomínio à Adobe é um processo transparente e não afeta suas campanhas e a capacidade de entrega. [Saiba mais sobre o gerenciamento de certificados SSL](monitoring-ssl-certificates.md#management)


## Delegação de novos certificados SSL de subdomínios {#new}

Para delegar certificados SSL ao configurar um novo subdomínio, habilite a opção **[!UICONTROL Optar por SSLs gerenciados pela Adobe para subdomínios]** do assistente de configuração de subdomínios. O processo de geração de certificado é diferente com base no método de delegação de subdomínio:

* **Delegação completa de subdomínio**: o certificado SSL é automaticamente solicitado e instalado pela Adobe sem nenhuma ação necessária. Depois de enviar a configuração de subdomínio, a solicitação de instalação do certificado é processada imediatamente como parte do fluxo de trabalho de configuração do subdomínio. [Saiba mais sobre a delegação completa de subdomínio](setting-up-new-subdomain.md#full-subdomain-delegation)

* **Delegação CNAME**: os registros de certificado a serem copiados para a solução de hospedagem serão fornecidos posteriormente no assistente de configuração. Você precisa gerar esses registros de certificado na solução de hospedagem de domínio antes de enviar a configuração do subdomínio. [Saiba mais sobre a delegação CNAME](setting-up-new-subdomain.md#use-cnames)

![](assets/cname-adobe-managed.png){width="70%" align="left"}

## Delegação de certificados SSL para subdomínios já delegados {#delegated}

Para delegar certificados SSL para um subdomínio já delegado, clique no botão de reticências ao lado do subdomínio desejado e selecione **[!UICONTROL Alterar para SSL gerenciado]**.

![](assets/delegate-ssl-list.png){width="70%" align="left"}

O processo de geração de certificado depende de como o subdomínio foi configurado originalmente:

### Subdomínios totalmente delegados

Para subdomínios configurados usando a delegação completa de subdomínio (com servidores de nomes da Adobe), o certificado SSL é solicitado e instalado automaticamente pela Adobe. Depois de clicar em **[!UICONTROL Alternar para SSL Gerenciado]** e confirmar, a solicitação de instalação do certificado será enviada imediatamente sem exigir nenhuma ação adicional.

### Subdomínios delegados CNAME

Para subdomínios configurados usando a delegação CNAME, uma caixa de diálogo é exibida com os registros de certificado que foram gerados automaticamente pelo Adobe. Copie esses registros um por um ou baixando um arquivo CSV e navegue até a sua solução de hospedagem de domínio para gerar o certificado correspondente.

Certifique-se de que todos os registros de certificado tenham sido gerados em sua solução de hospedagem de domínio. Se tudo estiver configurado corretamente, confirme a criação do registro e clique em **[!UICONTROL Enviar]**.

![](assets/delegate-ssl.png){width="70%" align="left"}
