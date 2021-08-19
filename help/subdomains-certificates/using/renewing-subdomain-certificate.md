---
product: campaign
solution: Campaign
title: Renovar um certificado SSL de subdomínio
description: Saiba como renovar certificados SSL de subdomínios
feature: Painel de controle do Campaign
role: Architect
level: Experienced
exl-id: e9b7c67d-6afa-44f9-b19d-39c0ec9a7edd
source-git-commit: 3bd3dcc0e09d887cab7d810d43f2c72bb4251ac9
workflow-type: tm+mt
source-wordcount: '868'
ht-degree: 93%

---

# Renovar um certificado SSL de subdomínio {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="Adicionar certificado SSL"
>abstract="Para adicionar um certificado SSL, você precisa gerar uma CSR, comprar o certificado SSL para os subdomínios e instalar o Pacote de certificados."
>additional-url="https://docs.adobe.com/content/help/pt-BR/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr" text="Gerar uma solicitação de assinatura de certificado (CSR)"
>additional-url="https://docs.adobe.com/content/help/pt-BR/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#installing-ssl-certificate" text="Como instalar um certificado SSL"

## Sobre a renovação de certificados {#about-certificate-renewal-process}

>[!IMPORTANT]
>
>A delegação de subdomínios pelo Painel de controle do Campaign está disponível em beta e está sujeita a atualizações e modificações frequentes sem aviso prévio.
>
>Esse recurso não está disponível para o Campaign v8.

O processo de renovação do certificado SSL inclui 3 etapas:

1. **Geração da Solicitação de assinatura de certificado (CSR)**
O Atendimento ao cliente da Adobe gera uma CSR para você. Você precisará fornecer algumas informações necessárias para gerar a CSR (como Nome, Nome e endereço da organização etc.).
1. **Compra do certificado SSL**
Depois que a CSR é gerada, você pode baixá-la e usá-la para comprar o certificado SSL da autoridade de certificação que sua empresa aprovar.
1. **Instalação do certificado SSL**
Depois de comprar o certificado SSL, você pode instalá-lo no subdomínio desejado.

![](assets/do-not-localize/how-to-video.png) Descubra este recurso no vídeo usando o [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=en#subdomains-and-certificates) ou o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=en#adding-ssl-certificates)

## Gerar uma solicitação de assinatura de certificado (CSR) {#generating-csr}

>[!CONTEXTUALHELP]
>id="cp_generate_csr"
>title="Gerar CSR"
>abstract="A Solicitação de assinatura de certificado deve ser gerada para a instância e os subdomínios que você pretende proteger antes de adquirir um certificado."

>[!CONTEXTUALHELP]
>id="cp_select_subdomains"
>title="Selecione os subdomínios para sua CSR"
>abstract="Você pode optar por incluir todos ou somente subdomínios específicos na solicitação de assinatura de certificado. Somente os subdomínios selecionados serão certificados por meio do certificado SSL adquirido."
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr" text="Gerar uma solicitação de assinatura de certificado (CSR)"
>additional-url="https://docs.adobe.com/content/help/pt-BR/control-panel/using/subdomains-and-certificates/subdomains-branding.html" text="Sobre a marca de subdomínios"

Para gerar uma Solicitação de assinatura de certificado (CSR), siga estas etapas:

1. No cartão **[!UICONTROL Subdomains & Certificates]**, selecione a instância desejada e clique no botão **[!UICONTROL Manage Certificate]**.

   ![](assets/renewal1.png)

1. Selecione **[!UICONTROL 1 - Generate a CSR]** e clique em **[!UICONTROL Next]** para iniciar o assistente que guiará você pelo processo de geração de CSR.

   ![](assets/renewal2.png)

1. Um formulário é exibido com todos os detalhes necessários para gerar a CSR.

   Preencha as informações solicitadas completamente e com precisão, caso contrário, o certificado pode não ser renovado (entre em contato com a equipe interna, as equipes de segurança e de TI, se necessário) e clique em **[!UICONTROL Next]**.

   * **[!UICONTROL Organization]**: nome oficial da organização.
   * **[!UICONTROL Organization Unit]**: unidade vinculada ao subdomínio (por exemplo: Marketing, TI).
   * **[!UICONTROL Instance]** (pré-preenchido): URL da instância do Campaign associado ao subdomínio.

   ![](assets/renewal3.png)

1. Selecione os subdomínios que serão incluídos na CSR e clique em **[!UICONTROL OK]**.

   ![](assets/renewal4.png)

1. Os subdomínios selecionados são exibidos na lista. Para cada um deles, selecione os subdomínios que serão incluídos e clique em **[!UICONTROL Next]**.

   ![](assets/renewal5.png)

1. Um resumo dos subdomínios que serão incluídos na CSR é exibido. Clique em **[!UICONTROL Submit]** para confirmar a solicitação.

   ![](assets/renewal6.png)

1. O arquivo .csr correspondente à seleção é gerado e baixado automaticamente. Agora você pode usá-lo para adquirir o certificado SSL da Autoridade de certificação que sua empresa aprovar.

   >[!NOTE]
   >
   >Se a CSR não for salva/baixada, ela será perdida e você terá que gerá-la novamente.

## Comprar um certificado com a CSR {#purchasing-certificate}

Após obter uma Solicitação de assinatura de certificado (CSR) pelo Painel de controle do Campaign, adquira um certificado SSL de uma autoridade de certificação aprovada pela sua organização.

## Instalação do certificado SSL {#installing-ssl-certificate}

>[!CONTEXTUALHELP]
>id="cp_install_ssl_certificate"
>title="Instalar Certificado SSL"
>abstract="Instale o Certificado SSL adquirido da autoridade de certificação aprovada pela sua organização."
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/subdomains-branding.html" text="Sobre a marca de subdomínios"

Depois que um certificado SSL for adquirido, você poderá instalá-lo em sua instância. Antes de continuar, verifique os pré-requisitos abaixo:

* A Solicitação de assinatura de certificado (CSR) deve ter sido gerada pelo Painel de controle do Campaign. Caso contrário, você não poderá instalar o certificado pelo Painel de controle do Campaign.
* A Solicitação de assinatura de certificado (CSR) deve corresponder ao subdomínio que foi configurado para funcionar com o Adobe. Por exemplo, ele não pode conter mais subdomínios do que o que foi configurado.
* O certificado deve ter uma data atual. Não é possível instalar certificados com datas futuras e eles não devem estar expirados (ou seja, datas de início e término devem ser válidas).
* O certificado deve ser emitido por uma autoridade de certificação (CA) confiável, como Comodo, DigiCert, Goaddy, etc.
* O tamanho do certificado deve ser de 2048 bits e o algoritmo deve ser RSA.
* O certificado deve estar no formato X.509 PEM.
* Os certificados SAN são compatíveis.
* Certificados curinga não são compatíveis.
* O arquivo ZIP ou o certificado não deve ser protegido por senha.
* De preferência, o arquivo ZIP deve conter apenas o seguinte em arquivos individuais:
   * Certificado de entidade final.
   * Cadeia intermediária de certificados (ordenada na ordem correta).
   * Certificado raiz (opcional).

Para instalar o certificado, siga estas etapas:

1. No cartão **[!UICONTROL Subdomains & Certificates]**, selecione a instância desejada e clique no botão **[!UICONTROL Manage Certificate]**.

   ![](assets/renewal1.png)

1. Selecione **[!UICONTROL 3 - Install Certificate Bundle]** e clique em **[!UICONTROL Next]** para iniciar o assistente que guiará você pelo processo de instalação do certificado.

   ![](assets/install1.png)

1. Selecione o arquivo .zip que contém o certificado que será instalado e clique em **[!UICONTROL Submit]**.

   ![](assets/install2.png)

>[!NOTE]
>
>O certificado será instalado em todos os domínios/subdomínios incluídos na CSR. Nenhum domínio/subdomínio adicional presente no certificado será considerado.

Depois que o certificado SSL é instalado, a data de expiração e o ícone de status do certificado são devidamente atualizados.

**Tópicos relacionados:**

* [Marca de subdomínios](../../subdomains-certificates/using/subdomains-branding.md)
* [Monitoramento de subdomínios](../../subdomains-certificates/using/monitoring-subdomains.md)
