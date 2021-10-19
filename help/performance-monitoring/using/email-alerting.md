---
product: campaign
solution: Campaign
title: Alerta por email
description: Saiba como receber notificações por email em caso de problemas com as instâncias do Campaign
feature: Control Panel
role: Architect
level: Experienced
exl-id: 7942d2b1-d28f-4760-aa25-5ba94a627fd0
source-git-commit: 6249776ef4981cd3d706bf1946be0e054b471fb6
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---

# Alerta por email {#email-alerting}

Para oferecer maior flexibilidade ao seu trabalho, o Painel de controle do Campaign está equipado com funcionalidade de alerta por email em tempo real.

Para se inscrever nesses alertas, siga estas etapas:

1. Clique no botão **[!UICONTROL Alerting notifications]** botão disponível em qualquer local no Painel de controle do Campaign e clique em **[!UICONTROL Subscribe]**.

   ![](assets/subscribing.png)

1. Um email é enviado para confirmar a assinatura.

   ![](assets/email_subscription.png)

1. Após a assinatura, o Painel de controle do Campaign notificará sobre problemas do sistema e recomendará as ações a serem executadas. Alertas por email são enviados para todos que se inscreveram **todas as instâncias** que são administradores do.

   ![](assets/alert_sample.png)

A lista de alertas é a seguinte:

* **Uso do armazenamento SFTP**: Um dos servidores SFTP atingiu 80% ou mais de sua capacidade. Consulte [Gerenciamento de armazenamentos SFTP](../../sftp/using/sftp-storage-management.md).

* **Uso do banco de dados**: Um dos bancos de dados de suas instâncias atingiu 80% ou mais de sua capacidade. Consulte [Monitoramento de banco de dados](../../performance-monitoring/using/database-monitoring.md).

* **Expiração do certificado SSL**: Um dos certificados SSL de subdomínios expirou ou expirará em 60 dias ou menos. Consulte [Monitorar certificados SSL de subdomínios](../../subdomains-certificates/using/monitoring-ssl-certificates.md).

* **Expiração da lista de permissões de IP SFTP**: Um dos intervalos IP definidos expirou ou expirará em 10 dias ou menos. Consulte [Lista de permissões de intervalo IP](../../sftp/using/ip-range-allow-listing.md).

* **Expiração de chave pública SFTP**: Uma das chaves públicas que você definiu expirou ou expirará em 10 dias ou menos. Consulte [Gerenciamento de chaves](../../sftp/using/key-management.md).