---
title: Monitorando certificados SSL de subdomínios
description: Saiba como monitorar certificados SSL de seus subdomínios
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Monitorando certificados SSL de subdomínios {#monitoring-ssl-certificates}

O Adobe Campaign recomenda que você proteja os subdomínios que hospedam suas páginas iniciais, especialmente aqueles que estão coletando informações confidenciais de seus clientes.

**A criptografia** SSL (Secure Socket Layer) garante a segurança dos subdomínios que você delegou à Adobe. Quando o cliente preenche um formulário da Web ou visita uma página de aterrissagem hospedada pelo Adobe Campaign, por padrão as informações são enviadas por protocolo não seguro (HTTP). Para garantir segurança adicional, proteja as informações enviadas com um protocolo HTTPS. Por exemplo, seu endereço de subdomínio &quot;http://info.mywebsite.com/&quot; agora será &quot;https://info.mywebsite.com/&quot;.

**Os certificados SSL não são instalados nos próprios** subdomínios delegados. Eles são instalados em subdomínios associados, principalmente aqueles que hospedam páginas iniciais, páginas de recursos e outros.

**Os certificados SSL são fornecidos por um período** específico (1 ano, 60 dias etc.). Depois que um certificado expirar, você poderá enfrentar problemas ao acessar as páginas iniciais ou usar recursos do subdomínio. Para evitar isso, o Painel de controle permite que você monitore os certificados SSL de seus subdomínios, bem como inicie seu processo de renovação.

![](assets/no_certificate.png)

Se um certificado SSL de seu subdomínio estiver prestes a expirar, você poderá renová-lo rapidamente do Painel de controle. Para obter mais informações, consulte esta seção: [Renovando um certificado](../../subdomains-certificates/using/renewing-subdomain-certificate.md)SSL de subdomínio.
