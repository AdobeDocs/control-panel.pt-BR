---
title: Monitorando certificados SSL de subdomínios
description: Saiba como monitorar certificados SSL de seus subdomínios
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Monitoramento de seus subdomínios {#monitoring-subdomains}

É essencial monitorar seus subdomínios para garantir que todos estejam configurados corretamente para funcionar com o Adobe Campaign.

A lista de subdomínios para cada uma das instâncias de produção pode ser acessada diretamente ao selecionar o **[!UICONTROL Subdomains & Certificates]**cartão.

![](assets/subdomains_list.png)

Para obter mais detalhes sobre um subdomínio, clique no **[!UICONTROL Subdomain Details]**botão.
A lista de todos os subdomínios relacionados é exibida. Geralmente inclui subdomínios de páginas iniciais, páginas de recursos etc.

A **[!UICONTROL Sender info]**guia fornece informações sobre as caixas de entrada configuradas (Remetente, Responder para, e-mail de erro).

![](assets/subdomain_details.png)


Na lista de subdomínios, a **[!UICONTROL Last verification]**coluna indica quando um subdomínio foi verificado pela última vez.** Você pode iniciar uma verificação a qualquer momento clicando em **... /**[!UICONTROL Verify subdomain]** .

>[!CAUTION]
>
>A Adobe não recomenda o uso de subdomínios sem data de verificação, pois isso pode significar que esses subdomínios podem estar com problemas de entrega.

![](assets/subdomain_verification.png)

Ao iniciar uma verificação, várias operações são executadas para verificar se o subdomínio está configurado corretamente:

1. O Painel de controle verifica se o subdomínio pertence ao locatário da instância.
1. Um email é enviado da instância usando esse subdomínio para um conjunto de destinatários de teste de &quot;250ok&quot; (uma plataforma de terceiros para análise de email e entrega).
1. Após receber o email, 250ok lê os cabeçalhos de email e verifica se o SPF e o DKIM estão configurados e válidos.
1. O Painel de controle pesquisa continuamente o status de entrega de 250 ok por cerca de 20 minutos. Se o SPF e o DKIM passarem, isso significa que o subdomínio solicitado é verificado e está totalmente configurado e pronto para ser usado no envio de emails.
