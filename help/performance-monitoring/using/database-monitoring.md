---
product: campaign
solution: Campaign
title: Monitoramento de banco de dados
description: Saiba como monitorar os bancos de dados no Painel de controle do Campaign
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: cca04cd965c00a9e2bc496de632ee41ce53a166a
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 100%

---

# Monitoramento de banco de dados {#database-monitoring}

## Sobre bancos de dados de instâncias {#about-instances-databases}

De acordo com seu contrato, cada uma das instâncias do Campaign é provisionada com uma quantidade específica de espaço no banco de dados.

Os bancos de dados incluem todos os **ativos**, **workflows** e **dados** que estão armazenados no Adobe Campaign.

Com o tempo, os bancos de dados podem atingir sua capacidade máxima, especialmente se os recursos armazenados nunca são excluídos da instância ou se há muitos workflows em um estado pausado.

A sobrecarga de um banco de dados de instância pode gerar vários problemas (incapacidade de fazer logon, enviar emails etc.). Portanto, o monitoramento dos bancos de dados das instâncias é essencial para garantir o desempenho ideal.

>[!NOTE]
>
>Se o espaço de banco de dados fornecido, conforme mostrado no Painel de controle do Campaign, não refletir o espaço especificado em seu contrato, entre em contato com o Atendimento ao cliente.

## Monitoramento do uso do banco de dados {#monitoring-instances-database}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_database"
>title="Sobre o monitoramento de banco de dados"
>abstract="Nesta guia, você pode obter informações em tempo real sobre a utilização e evolução mais recente e histórica do banco de dados para cada uma das instâncias do Campaign."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=pt-BR" text="Sobre o monitoramento de desempenho"

![](assets/do-not-localize/how-to-video.png) Descubra este recurso no vídeo usando o [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=pt-BR#performance-monitoring) ou o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=pt-BR#performance-monitoring)

O Painel de controle do Campaign permite monitorar a utilização do banco de dados para cada uma das instâncias do Campaign. Para fazer isso, abra o cartão **[!UICONTROL Performance Monitoring]** e selecione a guia **[!UICONTROL Databases]**.

Selecione a instância desejada em **[!UICONTROL Instance List]** para exibir informações sobre a capacidade do banco de dados da instância e o espaço usado.

![](assets/databases_dashboard.png)

>[!NOTE]
>
>Observe que os dados desse painel são atualizados com base no **[!UICONTROL Database cleanup technical workflow]** que é executado na instância do Campaign (consulte a documentação do [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=pt-BR#list-of-technical-workflows) e [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html?lang=pt-BR)).
>
>Além disso, você pode receber notificações quando um de seus bancos de dados estiver atingindo seu limite da última vez que o fluxo de trabalho foi executado abaixo do **[!UICONTROL Used Space]** e das métricas **[!UICONTROL Provided Space]**. Observe que, se o fluxo de trabalho não está em execução há mais de três dias, recomendamos entrar em contato com o Atendimento ao cliente da Adobe para investigar por que o fluxo de trabalho não está em execução.

Métricas adicionais, descritas abaixo, estão disponíveis neste painel para ajudar você a analisar o uso do banco de dados da instância.

### Utilização do banco de dados {#database-utilization}

A área **[!UICONTROL Database utilization]** fornece uma representação gráfica da utilização mínima, média e máxima do banco de dados nos últimos sete dias, bem como o limite de utilização do banco de dados de 90% representado por uma curva pontilhada vermelha.

Para alterar o período, use os filtros disponíveis no canto superior direito do gráfico.

Para melhorar a compreensão, também é possível destacar uma ou várias curvas no gráfico. Para fazer isso, selecione-as na legenda **[!UICONTROL Aggregation Type]**.

Para obter mais detalhes sobre um período específico, passe o mouse sobre o gráfico para exibir as informações sobre o uso do banco de dados que foi feito no momento.

![](assets/databases_dashboard_detail.png)

### Visão geral de armazenamento {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="Sobre a visão geral do armazenamento"
>abstract="Nesta guia, você pode obter informações detalhadas sobre os diferentes recursos do Campaign que estão consumindo espaço no banco de dados."

A área **[!UICONTROL Storage overview]** fornece uma representação gráfica do espaço ocupado por:

* **[!UICONTROL System resources]**

   Observe que, se os recursos do sistema estiverem consumindo uma grande parte do espaço do banco de dados, recomendamos entrar em contato com o Atendimento ao cliente.

* **[!UICONTROL Out-of-the-box tables]** fornecido por padrão com as instâncias do Campaign,
* **[!UICONTROL Temporary tables]** criado por workflows e deliveries,
* **[!UICONTROL Non-out of the box tables]** gerado após a criação de recursos personalizados.

![](assets/database-storage-overview.png)

Clique no botão **[!UICONTROL View details]** para obter mais detalhes sobre os diferentes assets que estão consumindo espaço no banco de dados.

![](assets/database-storage-details.png)

Use o filtro para refinar suas tabelas de pesquisa e exibição somente de um tipo de ativo específico.

![](assets/database-storage-overview-filter.png)

### Os 10 principais recursos temporários {#top-10}

A área **[!UICONTROL Top 10 temporary resources]** lista os 10 maiores recursos temporários gerados por workflows e deliveries.

Monitorar workflows e deliveries que estão criando grandes recursos temporários é uma etapa essencial para monitorar seu banco de dados. Se qualquer recurso temporário estiver consumindo muito espaço no banco de dados, verifique se esse fluxo de trabalho ou delivery é necessário e navegue até sua instância para interrompê-lo.

>[!IMPORTANT]
>
>A recomendação geral é evitar ter **mais de 40 colunas** em recursos não prontos para uso.

![](assets/database-top10.png)

>[!NOTE]
>
>Se um fluxo de trabalho tiver muitas tabelas ou um banco de dados grande, recomendamos examinar o fluxo de tabalho para investigar por que ele está gerando tantos dados.
>
>Os recursos do Campaign Standard e do Classic também estão disponíveis no final desta página para ajudar você a evitar a sobrecarga do banco de dados.

O botão **[!UICONTROL View all]** permite acessar informações detalhadas sobre esses recursos temporários.

![](assets/database-top10-view.png)

O valor na coluna **[!UICONTROL Keep interim results]** indica se a opção está ativada (&quot;1&quot;) ou desativada (&quot;0&quot;) no Campaign. Essa opção permite salvar os resultados das transições entre as várias atividades de um fluxo de trabalho (consulte a documentação do [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/executing-a-workflow/managing-execution-options.html?lang=pt-BR) e do [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/introduction/workflow-best-practices.html?lang=pt-BR#logs)).

>[!IMPORTANT]
>
>Essa opção nunca deve ser verificada em um fluxo de trabalho de produção. Essa opção é usada para analisar os resultados e é projetada apenas para fins de teste e, portanto, deve ser usada apenas em ambientes de desenvolvimento ou de preparo.
>
>Se o valor no Painel de controle do Campaign indicar que a opção está habilitada para um de seus workflows, recomendamos desativar o Campaign.

## Como impedir a sobrecarga do banco de dados {#preventing-database-overload}

O Campaign Standard e o Classic oferecem várias maneiras de evitar o consumo excessivo de espaço em disco do banco de dados.

A seção abaixo fornece recursos úteis das documentações do Campaign para ajudar você a otimizar o uso dos bancos de dados:

**Monitoramento de workflows**

* [Práticas recomendadas para workflows](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.html?lang=pt-BR) (Campaign Standard)
* [Monitoramento da execução de fluxo de trabalho](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html?lang=pt-BR) (Campaign Classic)

**Manutenção do banco de dados**

* Fluxo de trabalho técnico de limpeza de banco de dados: [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) - [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html)
* [Manual de manutenção de banco de dados](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html?lang=pt-BR) (Campaign Classic)
* [Solução de problemas de desempenho do banco de dados](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/troubleshooting-toc/database-issues-toc/database-performances.html?lang=pt-BR) (Campaign Classic)
* [Opções relacionadas ao banco de dados](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html?lang=pt-BR#database) (Campaign Classic)
* Retenção de dados: [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/data-retention.html?lang=pt-BR) — [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/configuring-campaign-classic/data-model/data-model-best-practices.html?lang=pt-BR#data-retention)

>[!NOTE]
>
>Além disso, você poderá receber notificações quando um de seus bancos de dados estiver atingindo sua capacidade. Para fazer isso, assine os [alertas de email](../../performance-monitoring/using/email-alerting.md).
