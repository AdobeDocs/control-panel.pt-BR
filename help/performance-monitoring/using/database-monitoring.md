---
title: Monitoramento de banco de dados
description: Saiba como monitorar seu banco de dados de Campanhas no Painel de controle
translation-type: tm+mt
source-git-commit: f995e0dc51fd95d00fdcaa2eb347b2aedfdef60d

---


# Monitoramento de banco de dados {#database-monitoring}

## Sobre bancos de dados de instâncias {#about-instances-databases}

De acordo com seu contrato, cada uma das instâncias de Campanha é provisionada com uma quantidade específica de espaço no banco de dados.

Os bancos de dados incluem todos os **ativos**, **workflows** e **dados** armazenados no Adobe Campaign.

Com o tempo, os bancos de dados podem atingir sua capacidade máxima, especialmente se os recursos armazenados nunca forem excluídos da instância, ou se houver muitos workflows em um estado de pausa.

O sobrefluxo de um banco de dados de instância pode levar a vários problemas (incapacidade de fazer logon, enviar emails etc.). O monitoramento dos bancos de dados de suas instâncias é, portanto, essencial para garantir o desempenho ideal.

>[!NOTE]
>
>Observe que pode haver algumas discrepâncias entre a capacidade de espaço do banco de dados atual e a quantidade especificada no contrato por períodos de tempo distintos para garantir um desempenho mais alto.

## Monitoramento do uso do banco de dados {#monitoring-instances-database}

1. Abra o **[!UICONTROL Health Monitoring]** cartão e selecione a **[!UICONTROL Databases]** guia.

1. Selecione a instância desejada no **[!UICONTROL Instance List]**.

   A área superior fornece informações sobre a capacidade do banco de dados da instância e o espaço utilizado.

   ![](assets/databases_dashboard.png)

   A área inferior fornece uma representação gráfica da utilização do banco de dados nos últimos 7 dias. Você pode alterar o período de tempo exibido usando os filtros disponíveis no canto superior direito.

   Passar o mouse sobre o gráfico permite obter informações detalhadas sobre o período selecionado.

   ![](assets/databases_dashboard_detail.png)

## Impedindo a sobrecarga do banco de dados {#preventing-database-overload}

Campaign Standard e oferta clássica de várias maneiras de evitar o consumo excessivo de espaço em disco do banco de dados.

A seção abaixo fornece recursos úteis de documentações de Campanha para ajudá-lo a otimizar o uso de bancos de dados:

**Monitoramento de Workflows**

* [Práticas recomendadas](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.html) para os Workflows (Campaign Standard)
* [Monitoramento da execução](https://docs.adobe.com/help/en/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html) do fluxo de trabalho (Campaign Classic)

**Manutenção do banco de dados**

* Fluxo de trabalho técnico de limpeza de banco de dados ([Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflowshtml#list-of-technical-workflows) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html))
* [Guia](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html) de manutenção do banco de dados (Campaign Classic)
* [Solução de problemas](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/troubleshooting/database-performances.html) de desempenho do banco de dados (Campaign Classic)
* [Opções](https://docs.adobe.com/help/en/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html#database) relacionadas ao banco de dados (Campaign Classic)
