---
product: campaign
solution: Campaign
title: Monitorar certificados SSL de subdomínios
description: Saiba como monitorar certificados SSL de subdomínios
feature: 'Painel de controle do Campaign   '
role: Arquiteto
level: Experienciado
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 17%

---


# Monitorar subdomínios {#monitoring-subdomains}

É essencial monitorar os subdomínios para garantir que todos estejam configurados corretamente para funcionar com o Adobe Campaign.

A lista de subdomínios para cada uma das instâncias de produção é acessível diretamente ao selecionar o cartão **[!UICONTROL Subdomains & Certificates]**.

A coluna **[!UICONTROL Last verification]** indica quando um subdomínio foi verificado pela última vez. Você pode iniciar uma verificação a qualquer momento clicando no **...Botão** / **[!UICONTROL Verify subdomain]**.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>O Adobe não recomenda usar subdomínios sem data de certificado, pois pode significar que esses subdomínios podem estar tendo alguns problemas de deliverability.

Ao iniciar uma verificação, várias operações são executadas para verificar se o subdomínio está configurado corretamente (verificação do locatário da instância, teste de envio de email, etc.)

Se a verificação do subdomínio falhar, entre em contato com o Atendimento ao cliente do Adobe para obter mais investigações.

**Tópicos relacionados:**

* [Renovar um certificado SSL de subdomínio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Marca de subdomínios](../../subdomains-certificates/using/subdomains-branding.md)
