---
product: campaign
solution: Campaign
title: Monitoramento de subdomínios
description: Monitore subdomínios para garantir que todos estejam configurados corretamente para funcionar com o Adobe Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: a6a77cf6e564f4607c0c12facb2061cfb102a5a5
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 7%

---

# Monitoramento de subdomínios {#monitoring-subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="Remover subdomínios delegados "
>abstract="Essa tela permite remover qualquer subdomínio que tenha sido delegado no Painel de controle do Campaign. Lembre-se de que a remoção de subdomínio não pode ser desfeita e será irreversível após o envio.<br>Se estiver tentando remover o domínio primário da instância selecionada, você será solicitado a escolher o domínio que a substituirá."

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
