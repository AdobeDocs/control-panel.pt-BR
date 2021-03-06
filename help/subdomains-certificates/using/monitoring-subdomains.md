---
product: campaign
solution: Campaign
title: Monitoramento de subdomínios
description: Monitore subdomínios para garantir que todos estejam configurados corretamente para funcionar com o Adobe Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: fa45ec38ff06a0b02ab724e7ced79b7b5de2c766
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 10%

---

# Monitoramento de subdomínios {#monitoring-subdomains}

É essencial monitorar os subdomínios para garantir que todos estejam configurados corretamente para funcionar com o Adobe Campaign.

A lista de subdomínios para cada uma das instâncias de produção é acessível diretamente ao selecionar a variável **[!UICONTROL Subdomains & Certificates]** cartão.

O **[!UICONTROL Last verification]** indica quando um subdomínio foi verificado pela última vez. Você pode iniciar uma verificação a qualquer momento clicando no botão **...** / **[!UICONTROL Verify subdomain]** botão.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>O Adobe não recomenda usar subdomínios sem data de certificado, pois pode significar que esses subdomínios podem estar tendo alguns problemas de deliverability.

Ao iniciar uma verificação, várias operações são executadas para verificar se o subdomínio está configurado corretamente (verificação do locatário da instância, teste de envio de email, etc.)

Se a verificação do subdomínio falhar, entre em contato com o Atendimento ao cliente do Adobe para obter mais investigações.

**Tópicos relacionados:**

* [Renovar um certificado SSL de subdomínio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Marca de subdomínios](../../subdomains-certificates/using/subdomains-branding.md)
