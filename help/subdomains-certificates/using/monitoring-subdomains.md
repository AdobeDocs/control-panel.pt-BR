---
product: campaign
solution: Campaign
title: Monitoramento de subdomínios
description: Monitore subdomínios para garantir que todos estejam configurados corretamente para funcionar com o Adobe Campaign.
feature: Control Panel
role: Admin
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: e8bffd8e7f571fd85c725adf837c2997f7615fcd
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 10%

---


# Monitorar subdomínios {#monitoring-subdomains}

É essencial monitorar os subdomínios para garantir que todos estejam configurados corretamente para funcionar com o Adobe Campaign.

A lista de subdomínios para cada uma das instâncias de produção pode ser acessada diretamente ao selecionar o **[!UICONTROL Subdomains & Certificates]** cartão.

A variável **[!UICONTROL Last verification]** indica quando um subdomínio foi verificado pela última vez. É possível iniciar uma verificação a qualquer momento, clicando no link **..** / **[!UICONTROL Verify subdomain]** botão.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>O Adobe não recomenda usar subdomínios sem data de certificado, pois isso pode significar que esses subdomínios podem estar tendo alguns problemas de entrega.

Ao iniciar uma verificação, várias operações são executadas para verificar se o subdomínio está configurado corretamente (verificação de locatário de instância, teste de envio de email etc.) Se a verificação do subdomínio falhar, entre em contato com o Atendimento ao cliente da Adobe para obter mais investigação.

**Tópicos relacionados:**

* [Renovar um certificado SSL de subdomínio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Marca de subdomínios](../../subdomains-certificates/using/subdomains-branding.md)
