---
product: campaign
solution: Campaign
title: Alerta por email
description: Saiba como receber notificações por email em caso de problemas com as instâncias do Campaign
feature: Control Panel
role: Admin
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: e8bffd8e7f571fd85c725adf837c2997f7615fcd
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 3%

---

# Alerta por email {#email-alerting}

Para oferecer maior flexibilidade ao seu trabalho, o Painel de controle do Campaign está equipado com a funcionalidade de alerta por email em tempo real.

## Lista de alertas {#list}

A lista de alertas é a seguinte:

* **Uso do armazenamento SFTP**: um dos servidores SFTP atingiu 80% ou mais de sua capacidade. Ver [Gerenciamento de armazenamentos SFTP](../../sftp/using/sftp-storage-management.md).

* **Uso do banco de dados**: o banco de dados de uma de suas instâncias atingiu 80% ou mais de sua capacidade. Consulte [Monitoramento de banco de dados](../../performance-monitoring/using/database-monitoring.md).

* **Expiração da lista de permissões de IP SFTP**: um dos intervalos IP definidos expirou ou expirará em 10 dias ou menos. Consulte [Lista de permissões de intervalos IP](../../sftp/using/ip-range-allow-listing.md).

* **Expiração da chave pública SFTP**: Uma das chaves públicas definidas expirou ou expirará em 10 dias ou menos. Consulte [Gerenciamento de chaves](../../sftp/using/key-management.md).

* **Expiração do certificado SSL**: um dos certificados SSL de um dos subdomínios expirou ou expirará em 30 dias ou menos. Consulte [Monitorar certificados SSL de subdomínios](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

<!--* **Long running Queries**: A query has been running for more than 24 hours on one of your instances. See [Monitoring active queries](database-active-queries.md).-->

>[!NOTE]
>
>Além disso, o Painel de controle do Campaign permite **definir lembretes** para ser notificado por email antes que um evento ocorra em suas instâncias (versões e revisões de serviço).
>
>Para fazer isso, você precisa se inscrever nos alertas de email e definir um lembrete para os eventos futuros desejados. [Saiba como definir lembretes para eventos futuros](../../service-events/service-events.md#reminders)

## Assinar alertas {#subscribe}

Para assinar esses alertas, siga estas etapas:

1. Clique em **[!UICONTROL Alerting notifications]** botão disponível em qualquer local no Painel de controle do Campaign e clique em **[!UICONTROL Subscribe]**.

   ![](assets/subscribing.png)

1. Um email é enviado para confirmar sua assinatura.

   ![](assets/email_subscription.png)

1. Após a assinatura, o Painel de controle do Campaign notificará sobre problemas do sistema e recomendará as ações a serem executadas. Os alertas de email são enviados a todos que se inscreveram no **todas as instâncias** que são administradores do.

   ![](assets/alert_sample.png)
