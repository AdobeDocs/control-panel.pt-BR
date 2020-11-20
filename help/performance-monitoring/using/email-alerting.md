---
product: campaign
solution: Campaign
title: Alerta por email
description: Saiba como receber notificações por email em caso de problemas com as instâncias de Campanha
translation-type: tm+mt
source-git-commit: 168ae32d7931497bb37d63f7dd1d14eadbb4b1bf
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 2%

---


# Alerta por email {#email-alerting}

Para oferecer maior flexibilidade ao seu trabalho, o Painel de controle do Campaign está equipado com funcionalidade de alertas por email em tempo real.

Para assinar esses alertas, siga estas etapas:

1. Clique no **[!UICONTROL Alerting notifications]** botão disponível em qualquer local no Painel de controle do Campaign e, em seguida, clique em **[!UICONTROL Subscribe]**.

   ![](assets/subscribing.png)

1. Um email é enviado para confirmar sua subscrição.

   ![](assets/email_subscription.png)

1. Após a inscrição, o Painel de controle do Campaign notificará sobre problemas do sistema e recomendará as ações a serem tomadas. Os alertas de email são enviados para todos os que se inscreveram em **todas as instâncias** das quais são administradores.

   ![](assets/alert_sample.png)


A lista das indicações é a seguinte:

* **Uso** do armazenamento SFTP: Um de seus servidores SFTP alcançou 80% ou mais de sua capacidade. See [SFTP storage management](../../sftp/using/sftp-storage-management.md).

* **Uso** do banco de dados: Um dos bancos de dados de suas instâncias alcançou 80% ou mais de sua capacidade. Consulte Monitoramento [de](../../performance-monitoring/using/database-monitoring.md)banco de dados.

* **Expiração** do certificado SSL: Um dos certificados SSL de seus subdomínios expirou ou vai expirar em 60 dias ou menos. See [Monitoring subdomains&#39; SSL certificates](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

