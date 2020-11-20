---
product: campaign
solution: Campaign
title: Monitoramento de banco de dados
description: Saiba como monitorar seu banco de dados de Campanhas no Painel de controle do Campaign
translation-type: tm+mt
source-git-commit: 168ae32d7931497bb37d63f7dd1d14eadbb4b1bf
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 1%

---


# Monitoramento de banco de dados {#database-monitoring}

## Sobre bancos de dados de instâncias {#about-instances-databases}

De acordo com seu contrato, cada uma das instâncias de Campanha é provisionada com uma quantidade específica de espaço no banco de dados.

Os bancos de dados incluem todos os **ativos**, **workflows** e **dados** armazenados no Adobe Campaign.

Com o tempo, os bancos de dados podem atingir sua capacidade máxima, especialmente se os recursos armazenados nunca forem excluídos da instância, ou se houver muitos workflows em um estado de pausa.

O sobrefluxo de um banco de dados de instância pode levar a vários problemas (incapacidade de fazer logon, enviar emails etc.). O monitoramento dos bancos de dados de suas instâncias é, portanto, essencial para garantir o desempenho ideal.

>[!NOTE]
>
>Se a quantidade de espaço do banco de dados fornecido, conforme mostrado no Painel de controle do Campaign, não refletir a quantidade especificada em seu contrato, entre em contato com o Atendimento ao cliente.

## Monitoramento do uso do banco de dados {#monitoring-instances-database}

O Painel de controle do Campaign permite monitorar o uso do banco de dados para cada uma das instâncias de Campanha. Para fazer isso, abra o **[!UICONTROL Performance Monitoring]** cartão e selecione a **[!UICONTROL Databases]** guia.

Selecione a instância desejada do **[!UICONTROL Instance List]** para exibir informações sobre a capacidade do banco de dados da instância e o espaço utilizado.

![](assets/databases_dashboard.png)

>[!NOTE]
>
>Observe que os dados desse painel são atualizados com base no **[!UICONTROL Database cleanup technical workflow]** que é executado na instância da Campanha (consulte a documentação [Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) e [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html) ).
>
>Você pode verificar a última vez que o fluxo de trabalho foi executado abaixo das métricas **[!UICONTROL Used Space]** e **[!UICONTROL Provided Space]** . Observe que, se o fluxo de trabalho não estiver em execução há mais de 3 dias, recomendamos que você entre em contato com o Atendimento ao cliente do Adobe para que ele investigue por que o fluxo de trabalho não está em execução.

Métricas adicionais, descritas abaixo, estão disponíveis neste painel para ajudá-lo a analisar o uso do banco de dados da instância:

* [Utilização do banco de dados](../../performance-monitoring/using/database-monitoring.md#database-utilization)
* [Visão geral do armazenamento](../../performance-monitoring/using/database-monitoring.md#storage-overview)
* [Os 10 principais recursos temporários](../../performance-monitoring/using/database-monitoring.md#top-10)

### Utilização do banco de dados {#database-utilization}

A **[!UICONTROL Database utilization]** área fornece uma representação gráfica da utilização mínima, média e máxima do banco de dados nos últimos 7 dias, bem como do limite de 90% de utilização do banco de dados representado por uma curva pontilhada vermelha.

Para alterar o período de tempo, use os filtros disponíveis no canto superior direito do gráfico.

Para melhorar a leitura, você também pode realçar uma ou várias curvas no gráfico. Para fazer isso, selecione-os na **[!UICONTROL Aggregation Type]** legenda.

Para obter mais detalhes sobre um período específico, passe o mouse sobre o gráfico para exibir informações sobre o uso do banco de dados que foi feito no momento.

![](assets/databases_dashboard_detail.png)

### Visão geral do armazenamento {#storage-overview}

A **[!UICONTROL Storage overview]** área fornece uma representação gráfica do espaço ocupado por:

* **[!UICONTROL System resources]**

   Observe que, se os recursos do sistema estiverem consumindo grande parte do espaço do banco de dados, recomendamos que você entre em contato com o Atendimento ao cliente.

* **[!UICONTROL Out-of-the-box tables]** fornecido por padrão com suas instâncias de Campanha,
* **[!UICONTROL Temporary tables]** criados por workflows e delivery,
* **[!UICONTROL Non-out of the box tables]** gerado após a criação de recursos personalizados.

![](assets/database-storage-overview.png)

Clique no **[!UICONTROL View details]** botão para obter mais detalhes sobre os diferentes ativos que estão consumindo espaço no banco de dados.

![](assets/database-storage-details.png)

Use o filtro para refinar suas tabelas de pesquisa e exibição somente de um tipo de ativo específico.

![](assets/database-storage-overview-filter.png)

### Os 10 principais recursos temporários {#top-10}

A **[!UICONTROL Top 10 temporary resources]** área lista os 10 maiores recursos temporários gerados por workflows e delivery.

O monitoramento de workflows e delivery que estão criando grandes recursos temporários é uma etapa essencial para monitorar seu banco de dados. Se algum recurso temporário estiver consumindo muito espaço no banco de dados, verifique se esse fluxo de trabalho ou delivery é necessário e, eventualmente, navegue até sua instância para pará-lo.

>[!IMPORTANT]
>
>A recomendação geral é evitar ter **mais de 40 colunas** em recursos não prontos para uso.

![](assets/database-top10.png)

>[!NOTE]
>
>Se um fluxo de trabalho tiver um grande número de contagens de tabela ou tamanho de banco de dados, recomendamos revisar o fluxo de trabalho para investigar por que está gerando tantos dados.
>
>Os recursos de Campaign Standard e Classic também estão disponíveis no final desta página para ajudar a impedir a sobrecarga do banco de dados.

O **[!UICONTROL View all]** botão permite acessar informações detalhadas sobre esses recursos temporários.

![](assets/database-top10-view.png)

>[!NOTE]
>
>O valor na **[!UICONTROL Keep interim results]** coluna indica se a opção está ativada (&quot;1&quot;) ou desativada (&quot;0&quot;) na Campanha. A **[!UICONTROL Keep interim results]** opção está acessível nas propriedades dos workflows. Ele permite salvar os resultados das transições entre as várias atividades de um fluxo de trabalho (consulte a documentação [Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/executing-a-workflow/managing-execution-options.html) e [Campaign Classic](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/workflow-best-practices.html#logs) ).
>
>Se a opção estiver ativada para um de seus workflows, o fluxo de trabalho de limpeza do banco de dados não conseguirá recuperar o espaço consumido pelos resultados intermediários. Portanto, recomendamos revisar o fluxo de trabalho para verificar se a opção pode ser desativada.

## Impedindo a sobrecarga do banco de dados {#preventing-database-overload}

Campaign Standard e oferta clássica de várias maneiras de evitar o consumo excessivo de espaço em disco do banco de dados.

A seção abaixo fornece recursos úteis de documentações de Campanha para ajudá-lo a otimizar o uso de bancos de dados:

**Monitoramento de workflows**

* [Práticas recomendadas](https://docs.adobe.com/content/help/pt-BR/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.html) para os workflows (Campaign Standard)
* [Monitoramento da execução](https://docs.adobe.com/help/en/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html) do fluxo de trabalho (Campaign Classic)

**Manutenção do banco de dados**

* Fluxo de trabalho técnico de limpeza de banco de dados ([Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html))
* [Guia](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html) de manutenção do banco de dados (Campaign Classic)
* [Solução de problemas](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/troubleshooting/database-performances.html) de desempenho do banco de dados (Campaign Classic)
* [Opções](https://docs.adobe.com/help/en/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html#database) relacionadas ao banco de dados (Campaign Classic)
* Retenção de dados ([Campaign Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/data-retention.html) / [Campaign Classic](https://docs.adobe.com/help/en/campaign-classic/using/configuring-campaign-classic/data-model/data-model-best-practices.html#data-retention))

>[!NOTE]
>
>Além disso, você pode receber notificações quando um de seus bancos de dados estiver atingindo sua capacidade. Para fazer isso, inscreva-se em alertas [por](../../performance-monitoring/using/email-alerting.md)email.
