---
title: Monitorando certificados SSL de subdomínios
description: Saiba como monitorar certificados SSL de seus subdomínios
translation-type: tm+mt
source-git-commit: 7726a8ef8863d2e2d57e5be7ade7de636a7d2ea1

---


# Monitorando certificados SSL de subdomínios {#monitoring-ssl-certificates}

## Sobre certificados SSL {#about-ssl-certificates}

O Adobe Campaign recomenda que você proteja os subdomínios que hospedam suas páginas iniciais, especialmente aqueles que estão coletando informações confidenciais de seus clientes.

**A criptografia** SSL (Secure Socket Layer) garante a segurança dos subdomínios que você delegou à Adobe. Quando o cliente preenche um formulário da Web ou visita uma página de aterrissagem hospedada pelo Adobe Campaign, por padrão as informações são enviadas por protocolo não seguro (HTTP). Para garantir segurança adicional, proteja as informações enviadas com um protocolo HTTPS. Por exemplo, seu endereço de subdomínio &quot;http://info.mywebsite.com/&quot; agora será &quot;https://info.mywebsite.com/&quot;.

**Os certificados SSL não são instalados nos próprios** subdomínios delegados. Eles são instalados em subdomínios associados, principalmente aqueles que hospedam páginas iniciais, páginas de recursos e outros.

**Os certificados SSL são fornecidos por um período** específico (1 ano, 60 dias etc.). Depois que um certificado expirar, você poderá enfrentar problemas ao acessar as páginas iniciais ou usar recursos do subdomínio. Para evitar isso, o Painel de controle permite que você monitore os certificados SSL de seus subdomínios, bem como inicie seu processo de renovação.

![](assets/no_certificate.png)

## Monitorando certificados SSL {#monitoring-certificates}

O status dos certificados SSL dos subdomínios está disponível diretamente na lista de subdomínios ao selecionar o **[!UICONTROL Subdomains & Certificates]**cartão.

Os subdomínios são organizados pela data de expiração mais próxima do certificado SSL, com informações visuais sobre a expiração, em dias:

* **Verde**: o subdomínio não tem certificado que expira nos próximos 60 dias.
* **Laranja**: um ou mais subdomínios têm um certificado que expirará nos próximos 60 dias.
* **Vermelho**: um ou mais subdomínios têm um certificado que expirará nos próximos 30 dias.
* **Cinza**: nenhum certificado foi instalado para o subdomínio.

![](assets/subdomains_list.png)

Para obter mais detalhes sobre um subdomínio, clique no **[!UICONTROL Subdomain Details]**botão.
A lista de todos os subdomínios relacionados é exibida. Geralmente inclui subdomínios de páginas iniciais, páginas de recursos etc.

A **[!UICONTROL Sender info]**guia fornece informações sobre as caixas de entrada configuradas (Remetente, Responder para, e-mail de erro).

![](assets/subdomain_details.png)

Se um certificado SSL de seu subdomínio estiver prestes a expirar, você poderá renová-lo diretamente do Painel de controle. Para obter mais informações, consulte esta seção: [Renovando um certificado](../../subdomains-certificates/using/renewing-subdomain-certificate.md)SSL de subdomínio.

>[!NOTE]
>
>A renovação do certificado do Painel de controle estará disponível em beta no final de janeiro.
