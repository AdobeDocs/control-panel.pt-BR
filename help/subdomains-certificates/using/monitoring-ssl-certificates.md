---
product: campaign
solution: Campaign
title: Monitorar certificados SSL de subdomínios
description: Saiba como monitorar certificados SSL de subdomínios
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: a7888e1c-259d-4601-951b-0f1062d90dc2
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 57%

---

# Monitorar certificados SSL de subdomínios {#monitoring-ssl-certificates}

## Sobre certificados SSL {#about-ssl-certificates}

O Adobe Campaign recomenda proteger os subdomínios que hospedam suas landing pages, especialmente aqueles que estão coletando informações confidenciais dos clientes.

**Criptografia SSL (Secure Socket Layer)** A garante a segurança dos subdomínios configurados para trabalhar com o Adobe. Quando o cliente preenche um formulário da Web ou visita uma landing page hospedada pelo Adobe Campaign, por padrão as informações são enviadas por protocolo não seguro (HTTP). Para garantir ainda mais segurança, proteja as informações enviadas com um protocolo HTTPS. Por exemplo, o endereço de subdomínio &quot;http://info.mywebsite.com/&quot; agora será &quot;https://info.mywebsite.com/&quot;.

**Os certificados SSL não são instalados nos próprios subdomínios configurados**. Eles são instalados em subdomínios associados, principalmente aqueles que hospedam landing pages, páginas de recursos e outros.

**Os certificados SSL são fornecidos por um período específico** (1 ano, 60 dias, etc.). Depois que um certificado expirar, você poderá enfrentar problemas ao acessar as landing pages ou usar recursos do subdomínio. Para evitar isso, o Painel de controle permite monitorar os certificados SSL dos subdomínios e iniciar o processo de renovação.

![](assets/no_certificate.png)

## Gerenciamento de certificados SSL {#management}

O monitoramento de certificados SSL é fundamental para garantir que seus subdomínios estejam seguros. Com o Painel de controle do Campaign, você pode instalar e renovar os certificados SSL de subdomínios diretamente por conta própria ou delegá-los ao Adobe para que esse processo seja executado automaticamente sem a necessidade de nenhuma ação da sua parte.

É altamente recomendado delegar o gerenciamento dos certificados SSL de seus subdomínios à Adobe, pois ela criará automaticamente o certificado e o renovará todos os anos antes da expiração. Isso reduz o risco de erros que podem ocorrer ao gerenciar certificados manualmente. [Saiba como delegar certificados SSL de subdomínios para o Adobe](delegate-ssl.md)

Abaixo, você encontrará uma lista abrangente dos impactos associados ao gerenciamento manual de certificados, em vez de delegar essa operação ao Adobe:

|       | Certificado gerenciado pelo cliente | Certificado gerenciado por Adobe |
|  ---  |  ---  |  ---  |
| Provedor de certificados | Autoridades de certificação de terceiros | Adobe pelos gerentes de certificado da AWS |
| Etapas manuais | Geração, compra e instalação de certificados CSR | nenhuma |
| Processo de renovação | Responsabilidade do cliente | Gerenciado pelo Adobe automaticamente |
| Segurança de subdomínio | O domínio pode ter subdomínios inseguros (rastreamento, espelho e res), a menos que você esteja instalando/renovando certificados. | Todos os novos domínios (se optados por Adobe gerenciado) terão todos os subdomínios protegidos por padrão. |
| Custo do certificado | O cliente suporta o custo dos certificados | Gratuito |

## Monitoramento de certificados SSL {#monitoring-certificates}

>[!CONTEXTUALHELP]
>id="cp_subdomain_details"
>title="Detalhes do subdomínio"
>abstract="Recupere informações dos certificados SSL dos subdomínios."

O status dos certificados SSL dos subdomínios está disponível diretamente na lista de subdomínios ao selecionar o **[!UICONTROL Subdomínios e certificados]** cartão.

Os subdomínios são organizados pela data de expiração mais próxima do certificado SSL, com informações visuais sobre a expiração, em dias:

* **Verde**: o subdomínio não tem certificado que expira nos próximos 60 dias.
* **Laranja**: um ou mais subdomínios têm um certificado que expirará nos próximos 60 dias.
* **Vermelho**: um ou mais subdomínios têm um certificado que expirará nos próximos 30 dias.
* **Cinza**: nenhum certificado foi instalado para o subdomínio.

![](assets/subdomains_list.png)

Para obter mais detalhes sobre um subdomínio, clique no link **[!UICONTROL Detalhes do subdomínio]** botão.
A lista de todos os subdomínios relacionados é exibida. Em geral, a lista inclui subdomínios de landing pages, páginas de recursos, etc.

A variável **[!UICONTROL Informações do remetente]** A guia fornece informações sobre as caixas de entrada configuradas (Remetente, Responder para, Email de erro).

![](assets/subdomain_details.png)

Se um dos certificados SSL de subdomínio estiver prestes a expirar, você poderá renová-lo diretamente no Painel de controle. Para obter mais informações, consulte esta seção: [Renovar um certificado SSL de subdomínio](../../subdomains-certificates/using/renewing-subdomain-certificate.md).

**Tópicos relacionados:**

* [Renovar um certificado SSL de subdomínio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Marca de subdomínios](../../subdomains-certificates/using/subdomains-branding.md)
