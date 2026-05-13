---
product: campaign
solution: Campaign
title: Monitoramento de subdomínios
description: Monitore os seus subdomínios para garantir que todos estejam configurados corretamente para funcionar com o Adobe Campaign.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
TQID: https://experienceleague.adobe.com/49fMBOZ2iN7xs7PpnYRLDHpQO5eXMTvn-veAxpjeH7w
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 06babfad697fb874f2b77c5204e30580c55cd0d1
workflow-type: tm+mt
source-wordcount: 154
ht-degree: 77%

---

# Monitorar subdomínios {#monitoring-subdomains}

É essencial monitorar os seus subdomínios para garantir que todos estejam configurados corretamente para funcionar com o Adobe Campaign.

A lista de subdomínios para cada uma das suas instâncias de produção pode ser acessada diretamente ao selecionar o cartão **[!UICONTROL Subdomínios e certificados]**.

A coluna **[!UICONTROL Última verificação]** indica quando um subdomínio foi verificado pela última vez. É possível iniciar uma verificação a qualquer momento, clicando-se no botão **...** / **[!UICONTROL Verificar subdomínio]**.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>A Adobe não recomenda usar subdomínios sem data de certificado, pois isso pode significar que esses subdomínios podem estar com alguns problemas de capacidade de entrega.

Ao iniciar uma verificação, várias operações são executadas para verificar se o subdomínio está configurado corretamente (verificação de locatário de instância, teste de envio de email etc.) Se a verificação do subdomínio falhar, entre em contato com o Atendimento ao cliente da Adobe para obter mais investigação.

**Tópicos relacionados:**

* [Renovar um certificado SSL de subdomínio](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Marca de subdomínios](../../subdomains-certificates/using/subdomains-branding.md)
