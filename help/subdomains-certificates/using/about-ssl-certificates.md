---
title: Sobre certificados SSL
description: Saiba mais sobre certificados SSL
translation-type: tm+mt
source-git-commit: 6bc165f995d34d21b5bce379db3095317db10906

---


# Sobre certificados SSL {#about-ssl-certificates}

O Adobe Campaign recomenda que você proteja os subdomínios que hospedam suas páginas iniciais, especialmente aqueles que estão coletando informações confidenciais de seus clientes.

**A criptografia** SSL (Secure Socket Layer) garante a segurança dos subdomínios que você delegou à Adobe. Quando o cliente preenche um formulário da Web ou visita uma página de aterrissagem hospedada pelo Adobe Campaign, por padrão as informações são enviadas por protocolo não seguro (HTTP). Para garantir segurança adicional, proteja as informações enviadas com um protocolo HTTPS. Por exemplo, seu endereço de subdomínio &quot;http://info.mywebsite.com/&quot; agora será &quot;https://info.mywebsite.com/&quot;.

**Os certificados SSL não são instalados nos próprios** subdomínios delegados. Eles são instalados em subdomínios associados, principalmente aqueles que hospedam páginas iniciais, páginas de recursos e outros.

**Os certificados SSL são fornecidos por um período** específico (1 ano, 60 dias etc.). Depois que um certificado expirar, você poderá enfrentar problemas ao acessar as páginas iniciais ou usar recursos do subdomínio. Para evitar isso, o Painel de controle permite que você monitore os certificados SSL de seus subdomínios, bem como inicie seu processo de renovação.

Mais detalhes sobre a delegação de subdomínio estão disponíveis [aqui](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).
