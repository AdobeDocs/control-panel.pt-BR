---
product: campaign
solution: Campaign
title: Monitorar certificados SSL de subdomínios
description: Saiba como monitorar certificados SSL de subdomínios
feature: Control Panel
role: Architect
level: Experienced
exl-id: a7888e1c-259d-4601-951b-0f1062d90dc2
source-git-commit: 62ad3edb604ebd9fab6a3f930b7c79af6b9ca968
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 91%

---

# Monitorar certificados SSL de subdomínios {#monitoring-ssl-certificates}

>[!AVAILABILITY]
>
>Esse recurso não está disponível para o Campaign v8.

## Sobre certificados SSL {#about-ssl-certificates}

O Adobe Campaign recomenda proteger os subdomínios que hospedam suas páginas de aterrissagem, especialmente aqueles que estão coletando informações confidenciais dos clientes.

**A** criptografia SSL (Secure Socket Layer) garante a segurança dos subdomínios que você configurou para trabalhar com o Adobe. Quando o cliente preenche um formulário da Web ou visita uma página de aterrissagem hospedada pelo Adobe Campaign, por padrão as informações são enviadas por protocolo não seguro (HTTP). Para garantir ainda mais segurança, proteja as informações enviadas com um protocolo HTTPS. Por exemplo, o endereço de subdomínio &quot;http://info.mywebsite.com/&quot; agora será &quot;https://info.mywebsite.com/&quot;.

**Os certificados SSL não são instalados nos próprios** subdomínios configurados. Eles são instalados em subdomínios associados, principalmente aqueles que hospedam páginas de aterrissagem, páginas de recursos e outros.

**Os certificados SSL são fornecidos por um período específico** (1 ano, 60 dias, etc.). Depois que um certificado expirar, você poderá enfrentar problemas ao acessar as páginas de aterrissagem ou usar recursos do subdomínio. Para evitar isso, o Painel de controle do Campaign permite monitorar os certificados SSL dos subdomínios e iniciar o processo de renovação.

![](assets/no_certificate.png)

## Monitorar certificados SSL {#monitoring-certificates}

>[!CONTEXTUALHELP]
>id="cp_subdomain_details"
>title="Detalhes do subdomínio"
>abstract="Recupere informações dos certificados SSL dos subdomínios."

O status dos certificados SSL dos subdomínios está disponível diretamente na lista de subdomínios ao selecionar o cartão **[!UICONTROL Subdomains & Certificates]**.

Os subdomínios são organizados pela data de expiração mais próxima do certificado SSL, com informações visuais sobre a expiração, em dias:

* **Verde**: o subdomínio não tem certificado que expira nos próximos 60 dias.
* **Laranja**: um ou mais subdomínios têm um certificado que expirará nos próximos 60 dias.
* **Vermelho**: um ou mais subdomínios têm um certificado que expirará nos próximos 30 dias.
* **Cinza**: nenhum certificado foi instalado para o subdomínio.

![](assets/subdomains_list.png)

Para obter mais detalhes sobre um subdomínio, clique no botão **[!UICONTROL Subdomain Details]**.
A lista de todos os subdomínios relacionados é exibida. Em geral, a lista inclui subdomínios de páginas de aterrissagem, páginas de recursos, etc.

A guia **[!UICONTROL Sender info]** fornece informações sobre as caixas de entrada configuradas (Remetente, Responder para, Email de erro).

![](assets/subdomain_details.png)

Se um dos certificados SSL de subdomínio estiver prestes a expirar, você poderá renová-lo diretamente no Painel de controle do Campaign. Para obter mais informações, consulte esta seção: [Renovar um certificado SSL de subdomínio](../../subdomains-certificates/using/renewing-subdomain-certificate.md).

>[!IMPORTANT]
>
>A renovação do certificado pelo Painel de controle do Campaign está disponível em beta e está sujeita a atualizações e modificações frequentes sem aviso prévio.

**Tópicos relacionados:**

* [Renovar um certificado SSL de subdomínio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Marca de subdomínios](../../subdomains-certificates/using/subdomains-branding.md)
