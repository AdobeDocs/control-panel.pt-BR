---
product: campaign
solution: Campaign
title: Monitorar certificados SSL de subdomínios
description: Saiba como monitorar certificados SSL de subdomínios
translation-type: tm+mt
source-git-commit: 317b4c1cee34667a36f5e1a1197649bfd69c151a
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 16%

---


# Monitorar subdomínios {#monitoring-subdomains}

É essencial monitorar seus subdomínios para garantir que todos estejam configurados corretamente para funcionar com o Adobe Campaign.

A lista de subdomínios para cada uma das instâncias de produção pode ser acessada diretamente ao selecionar o **[!UICONTROL Subdomains & Certificates]** cartão.

A **[!UICONTROL Last verification]** coluna indica quando um subdomínio foi verificado pela última vez. Você pode iniciar uma verificação a qualquer momento clicando em **...** / **[!UICONTROL Verify subdomain]** .

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>O Adobe não recomenda o uso de subdomínios sem data de certificado, pois isso pode significar que esses subdomínios podem estar com problemas de entrega.

Ao iniciar uma verificação, várias operações são executadas para verificar se o subdomínio está configurado corretamente (verificação do locatário da instância, teste de envio de email etc.)

Se a verificação do subdomínio falhar, entre em contato com o Atendimento ao cliente da Adobe para obter mais informações.

**Tópicos relacionados:**

* [Renovar um certificado SSL de subdomínio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Marca de subdomínios](../../subdomains-certificates/using/subdomains-branding.md)
