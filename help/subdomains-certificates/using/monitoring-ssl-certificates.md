---
product: campaign
solution: Campaign
title: Monitorar certificados SSL de subdomínios
description: Saiba como monitorar certificados SSL de subdomínios
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: a7888e1c-259d-4601-951b-0f1062d90dc2
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
source-wordcount: '578'
ht-degree: 100%
---
# Monitorar certificados SSL de subdomínios {#monitoring-ssl-certificates}

## Sobre certificados SSL {#about-ssl-certificates}

O Adobe Campaign recomenda proteger os subdomínios que hospedam suas páginas de destino, especialmente aqueles que estão coletando informações confidenciais dos clientes.

A **criptografia SSL (Secure Socket Layer, Camada de Soquete de Segurança)** garante a segurança dos subdomínios configurados para trabalhar com a Adobe. Quando o(a) cliente preenche um formulário web ou visita uma página de destino hospedada pelo Adobe Campaign, as informações são enviadas por protocolo não seguro (HTTP) por padrão. Para garantir ainda mais segurança, proteja as informações enviadas com um protocolo HTTPS. Por exemplo, o endereço de subdomínio &quot;http://info.mywebsite.com/&quot; agora será &quot;https://info.mywebsite.com/&quot;.

**Os certificados SSL não são instalados nos subdomínios configurados em si**. Eles são instalados em subdomínios associados, principalmente aqueles que hospedam páginas de destino, páginas de recursos e outros.

**Os certificados SSL são fornecidos por um período específico** (1 ano, 60 dias, etc.). Depois que um certificado expirar, você poderá enfrentar problemas ao acessar as páginas de destino ou usar recursos do subdomínio. Para evitar isso, o Painel de controle permite monitorar os certificados SSL dos subdomínios e iniciar o processo de renovação.

![](assets/no_certificate.png)

## Gerenciamento de certificados SSL {#management}

O monitoramento de certificados SSL é fundamental para garantir a segurança dos seus subdomínios. Com o Painel de controle, é possível instalar e renovar os certificados SSL dos seus subdomínios diretamente por conta própria ou delegá-los à Adobe, para que esse processo seja executado automaticamente sem a necessidade de nenhuma ação da sua parte.

É altamente recomendado delegar o gerenciamento dos certificados SSL de seus subdomínios à Adobe, pois ela criará automaticamente o certificado e o renovará todos os anos antes da expiração. Isso reduz o risco de erros que podem ocorrer ao gerenciar certificados manualmente. [Saiba como delegar os certificados SSL dos seus subdomínios à Adobe](delegate-ssl.md)

Abaixo, você encontrará uma lista abrangente dos impactos associados ao gerenciamento manual de certificados, em contraste com delegar essa operação à Adobe:

|       | Certificado gerenciado pelo cliente | Certificado gerenciado pela Adobe |
|  ---  |  ---  |  ---  |
| Provedor de certificados | Autoridades de certificação de terceiros | Adobe por meio dos gerenciadores de certificados da AWS |
| Etapas manuais | Geração de CSR, compra e instalação de certificados | nenhuma |
| Processo de renovação | Responsabilidade do cliente | Administrado automaticamente pela Adobe |
| Segurança dos subdomínios | O domínio pode conter subdomínios desprotegidos (rastreamento, espelho e res), a menos que você esteja instalando/renovando certificados. | Todos os subdomínios de novos domínios (se você optar pelo gerenciamento pela Adobe) estarão protegidos por padrão. |
| Custo dos certificados | O cliente arca com o custo dos certificados | Gratuito |

## Monitorar certificados SSL {#monitoring-certificates}

>[!CONTEXTUALHELP]
>id="cp_subdomain_details"
>title="Detalhes do subdomínio"
>abstract="Recupere informações dos certificados SSL dos subdomínios."

O status dos certificados SSL dos seus subdomínios está disponível diretamente na lista de subdomínios ao selecionar o cartão **[!UICONTROL Subdomínios e certificados]**.

Os subdomínios são organizados pela data de expiração mais próxima do certificado SSL, com informações visuais sobre a expiração, em dias:

* **Verde**: o subdomínio não tem certificado que expira nos próximos 60 dias.
* **Laranja**: um ou mais subdomínios têm um certificado que expirará nos próximos 60 dias.
* **Vermelho**: um ou mais subdomínios têm um certificado que expirará nos próximos 30 dias.
* **Cinza**: nenhum certificado foi instalado para o subdomínio.

![](assets/subdomains_list.png)

Para mais detalhes sobre um subdomínio, clique no botão **[!UICONTROL Detalhes do subdomínio]**.
A lista de todos os subdomínios relacionados é exibida. Em geral, a lista inclui subdomínios de páginas de destino, páginas de recursos etc.

A guia **[!UICONTROL Informações do remetente]** fornece informações sobre as caixas de entrada configuradas (remetente, responder para, email de erro).

![](assets/subdomain_details.png)

Se um dos certificados SSL de subdomínio estiver prestes a expirar, você poderá renová-lo diretamente no Painel de controle. Para obter mais informações, consulte esta seção: [Renovar um certificado SSL de subdomínio](../../subdomains-certificates/using/renewing-subdomain-certificate.md).

**Tópicos relacionados:**

* [Renovar um certificado SSL de subdomínio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Marca de subdomínios](../../subdomains-certificates/using/subdomains-branding.md)
