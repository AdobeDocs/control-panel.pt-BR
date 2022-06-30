---
product: campaign
solution: Campaign
title: Renovar um certificado SSL de subdomínio
description: Saiba como renovar certificados SSL de subdomínios
feature: Control Panel
role: Architect
level: Experienced
exl-id: e9b7c67d-6afa-44f9-b19d-39c0ec9a7edd
source-git-commit: 5a5ac1a604fe5bdce07479ff84184abdb2e0ddba
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 28%

---

# Renovação de um certificado SSL {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="Renovação do certificado SSL"
>abstract="Para renovar um certificado SSL, você precisa gerar uma CSR, comprar o certificado SSL para seus subdomínios e instalar o Pacote de certificados."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#generating-csr" text="Gerar uma solicitação de assinatura de certificado (CSR)"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html#installing-ssl-certificate" text="Instalação de um certificado SSL"

>[!IMPORTANT]
>
>A renovação do certificado SSL pelo Painel de controle do Campaign está disponível em beta e está sujeita a atualizações e modificações frequentes sem aviso prévio.
>
>Se estiver usando uma instância com um modelo de hospedagem híbrido, você só poderá exibir certificados associados aos subdomínios delegados e não poderá renová-los.

O processo de renovação do certificado SSL inclui 3 etapas:

1. **Geração da Solicitação de Assinatura de Certificado (CSR)**

   A Solicitação de assinatura de certificado deve ser gerada para a instância e os subdomínios que você pretende proteger antes de adquirir um certificado.  Você precisará fornecer algumas informações necessárias para gerar a CSR (como Nome, Nome e endereço da organização etc.). [Saiba mais](generate-csr.md)

1. **Compra do certificado SSL**

   Depois que a CSR é gerada, você pode usá-la para comprar o certificado SSL da autoridade de certificação que sua empresa aprovar.

1. **Instalação do certificado SSL**

   Instale o certificado SSL adquirido no subdomínio desejado para protegê-los. [Saiba mais](install-ssl-certificate.md)

![](assets/do-not-localize/how-to-video.png) Descubra este recurso em vídeo usando [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html#subdomains-and-certificates) ou [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html#adding-ssl-certificates)

**Tópicos relacionados:**

* [Guia de práticas recomendadas de entrega - processo de solicitação de certificado SSL para Adobe Campaign](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/campaign/ac-ssl-certificate-request.html)
* [Marca de subdomínios](../../subdomains-certificates/using/subdomains-branding.md)
* [Monitoramento de subdomínios](../../subdomains-certificates/using/monitoring-subdomains.md)
