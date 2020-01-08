---
title: Renovando um certificado SSL de subdomínio
description: Saiba como renovar os certificados SSL de seus subdomínios
translation-type: tm+mt
source-git-commit: 50d29d25891adc866d624888ca72e16e529ae7bf

---


# Renovando um certificado SSL de subdomínio {#renewing-subdomains-ssl-certificates}

>[!IMPORTANT]
>
>A delegação de subdomínios do Painel de Controle estará disponível em versão beta até o final de janeiro e estará sujeita a atualizações e modificações frequentes sem aviso prévio.

## Sobre a renovação de certificados {#about-certificate-renewal-process}

O processo de renovação do certificado SSL inclui 3 etapas:

1. **Geração da Solicitação de assinatura de certificado (CSR)O Atendimento ao cliente da** Adobe gera um CSR para você. Será necessário fornecer algumas informações necessárias para gerar o CSR (como Nome comum, Nome da organização e endereço, etc.).
1. **Compra do certificado** SSL Depois que o CSR é gerado, você pode baixá-lo e usá-lo para comprar o certificado SSL da autoridade de certificação que sua empresa aprovar.
1. **Instalação do certificado** SSL Depois de comprar o certificado SSL, você pode instalá-lo no subdomínio desejado.

>[!NOTE]
>
>A renovação de certificados SSL por meio do Painel de controle está disponível somente para subdomínios **** totalmente delegados.

## Gerando uma solicitação de assinatura de certificado (CSR) {#generating-csr}

Para gerar uma solicitação de assinatura de certificado (CSR), siga estas etapas:

1. No **[!UICONTROL Subdomains & Certificates]**cartão, selecione a instância desejada e clique no**[!UICONTROL Manage Certificate]** botão.

   ![](assets/renewal1.png)

1. Selecione **[!UICONTROL Generate a CSR]**e clique**[!UICONTROL Next]** para iniciar o assistente que o guiará pelo processo de geração de CSR.

   ![](assets/renewal2.png)

1. Um formulário é exibido, com todos os detalhes necessários para gerar seu CSR.

   Certifique-se de preencher as informações solicitadas de forma completa e precisa; caso contrário, o certificado pode não ser renovado (entre em contato com sua equipe interna, equipes de segurança e TI, se necessário) e clique em **[!UICONTROL Next]**.

   * **[!UICONTROL Organization]**: nome oficial da organização.
   * **[!UICONTROL Organization Unit]**: unidade vinculada ao subdomínio (por exemplo: Marketing, TI).
   * **[!UICONTROL Instance]**(pré-cheia): URL da instância Campaign associada ao subdomínio.
   ![](assets/renewal3.png)

1. Selecione os subdomínios a serem incluídos no CSR e clique em **[!UICONTROL OK]**.

   ![](assets/renewal4.png)

1. Os subdomínios selecionados são exibidos na lista. Para cada um deles, selecione os subdomínios a serem incluídos e clique em **[!UICONTROL Next]**.

   ![](assets/renewal5.png)

1. Um resumo dos subdomínios a serem incluídos no CSR é exibido. Clique em **[!UICONTROL Submit]**para confirmar sua solicitação.

   ![](assets/renewal6.png)

1. O arquivo .csr correspondente à sua seleção é gerado e baixado automaticamente. Agora você pode usá-lo para adquirir o certificado SSL da Autoridade de certificação que sua empresa aprovar.

   >[!NOTE]
   >
   >Se o CSR não for salvo/baixado, ele será perdido e você terá que gerá-lo novamente.

## Comprar um certificado com o CSR {#purchasing-certificate}

Depois de obter um CSR de Solicitação de assinatura de certificado do Painel de controle, adquira um certificado SSL de uma autoridade de certificação aprovada pela sua organização.

## Instalação do certificado SSL {#installing-ssl-certificate}

Depois que um certificado SSL for adquirido, você poderá instalá-lo em sua instância. Antes de continuar, verifique se você está ciente dos pré-requisitos abaixo:

* A Solicitação de assinatura de certificado (CSR) deve ter sido gerada a partir do Painel de controle. Caso contrário, você não poderá instalar o certificado do Painel de controle.
* A Solicitação de assinatura de certificado (CSR) deve corresponder ao subdomínio que foi delegado à Adobe. Por exemplo, ele não pode conter mais subdomínios que o que foi delegado.
* O certificado deve ter uma data atual. Não é possível instalar certificados com datas futuras e eles não devem estar expirados (ou seja, datas de início e término válidas).
* O certificado deve ser emitido por uma autoridade de certificação (CA) confiável, como Comodo, DigiCert, Goaddy etc.
* O tamanho do certificado deve ser de 2048 bits e o algoritmo deve ser RSA.
* O certificado deve estar no formato X.509 PEM.
* Os certificados SAN são suportados.
* Certificados curingas não são suportados.
* O arquivo ZIP ou o certificado não deve ser protegido por senha.
* O arquivo ZIP deve conter apenas o seguinte em arquivos individuais de preferência:
   * Certificado de entidade final.
   * Cadeia de certificados intermédia (ordenada em ordem adequada).
   * Certificado raiz (opcional).

Para instalar o certificado, siga estas etapas:

1. No **[!UICONTROL Subdomains & Certificates]**cartão, selecione a instância desejada e clique no**[!UICONTROL Manage Certificate]** botão.

   ![](assets/renewal1.png)

1. Clique em **[!UICONTROL Install SSL Certificate]**, em seguida,**[!UICONTROL Next]** para iniciar o assistente que o guiará pelo processo de instalação do certificado.

   ![](assets/install1.png)

1. Selecione o arquivo .zip que contém o certificado a ser instalado e clique em **[!UICONTROL Submit]**.

   ![](assets/install2.png)

Depois que o certificado SSL é instalado, a data de expiração e o ícone de status do certificado são atualizados de acordo.
