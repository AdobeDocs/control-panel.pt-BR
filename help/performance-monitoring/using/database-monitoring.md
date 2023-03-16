---
product: campaign
solution: Campaign
title: Sobre o monitoramento de banco de dados
description: Saiba como monitorar os bancos de dados no Painel de controle
feature: Control Panel
role: Architect
level: Experienced
exl-id: 2bd7d2dd-97be-49bb-9f8e-7161d0742bc1
source-git-commit: 80a96152ffcfa184fbeb6fc5cddcb119655ffab1
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 79%

---

# Sobre o monitoramento de banco de dados {#database-monitoring}

## Sobre bancos de dados de instâncias {#about-instances-databases}

De acordo com seu contrato, cada uma das instâncias do Campaign é provisionada com uma quantidade específica de espaço no banco de dados. Os bancos de dados incluem todos os **ativos**, **workflows** e **dados** que estão armazenados no Adobe Campaign.

Com o tempo, os bancos de dados podem atingir sua capacidade máxima, especialmente se os recursos armazenados nunca são excluídos da instância ou se há muitos workflows em um estado pausado.

A sobrecarga de um banco de dados de instância pode gerar vários problemas (incapacidade de fazer logon, enviar emails etc.). Portanto, o monitoramento dos bancos de dados das instâncias é essencial para garantir o desempenho ideal.

Se você se inscreveu em [alerta por email](../../performance-monitoring/using/email-alerting.md), você receberá notificações por email quando um dos bancos de dados de suas instâncias atingir 80% ou mais de sua capacidade.

## Monitoramento do uso do banco de dados{#monitoring-database-usage}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_database"
>title="Sobre o monitoramento de banco de dados"
>abstract="Nesta guia, você pode obter informações em tempo real sobre a utilização e evolução mais recente e histórica do banco de dados para cada uma das instâncias do Campaign."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=pt-BR" text="Sobre o monitoramento de desempenho"

O Painel de controle permite monitorar a utilização do banco de dados para cada uma das instâncias do Campaign. Para fazer isso, abra o cartão **[!UICONTROL Performance Monitoring]** e selecione a guia **[!UICONTROL Databases]**.

Selecione a instância desejada em **[!UICONTROL Instance List]** para exibir informações sobre a capacidade do banco de dados da instância e o espaço usado.

>[!NOTE]
>
>Se o espaço de banco de dados fornecido, conforme mostrado no Painel de controle, não refletir o espaço especificado em seu contrato, entre em contato com o Atendimento ao cliente.

![](assets/databases_dashboard.png)

Os dados desse painel são atualizados com base no **[!UICONTROL Database cleanup technical workflow]** que é executado na instância do Campaign (consulte [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=pt-BR#list-of-technical-workflows) e [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html?lang=pt-BR) documentação). Você pode verificar a última vez que o workflow foi executado abaixo do **[!UICONTROL Used Space]** e **[!UICONTROL Provided Space]** métricas. Observe que, se o fluxo de trabalho não está em execução há mais de três dias, recomendamos entrar em contato com o Atendimento ao cliente da Adobe para investigar por que o fluxo de trabalho não está em execução.

Métricas adicionais estão disponíveis neste painel para ajudar você a analisar o uso do banco de dados da instância. Eles estão detalhados nestas seções:

* [Utilização do banco de dados](../../performance-monitoring/using/database-utilization.md)
* [Visão geral de armazenamento](../../performance-monitoring/using/database-storage-overview.md)
* [Os 10 principais recursos temporários](../../performance-monitoring/using/database-top-ten-resources.md)
* [Consultas ativas](../../performance-monitoring/using/database-active-queries.md)

![](assets/do-not-localize/how-to-video.png) Descubra este recurso no vídeo usando o [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=pt-BR#performance-monitoring) ou o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=pt-BR#performance-monitoring)
