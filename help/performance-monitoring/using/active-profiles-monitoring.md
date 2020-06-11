---
title: Monitoramento de perfis ativos
description: Saiba como obter informações em tempo real sobre a utilização e evolução mais recentes e históricas dos Perfis ativos para cada uma de suas instâncias de Campanha.
translation-type: tm+mt
source-git-commit: 024eb750021ff2446b34d648b5abfb016eabc289
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 14%

---


# Monitoramento de perfis ativos {#active-profiles-monitoring}

>[!IMPORTANT]
>
>O monitoramento de perfis ativos pelo Painel de controle está disponível em beta e sujeito a atualizações e modificações frequentes sem aviso prévio.
>
>O recurso está disponível para clientes hospedados no AWS a partir da compilação do Campaign Standard 10368 e da compilação do Campaign Classic 8931. Se estiver usando uma versão anterior, é necessário atualizar para usar esse recurso.

## Sobre perfis ativos {#about-active-profiles}

De acordo com seu contrato, cada uma das instâncias de Campanha é provisionada com uma quantidade específica de perfis ativos que são contados para fins de faturamento. Consulte seu contrato mais recente para obter referência sobre o número de perfis ativos comprados.

“Perfil” significa um registro de informações (por exemplo: um registro na tabela nmsRecipient ou uma tabela externa contendo uma ID de cookie, ID do cliente, identificador móvel ou outras informações relevantes para um canal específico) representando um cliente final, um prospecto ou um cliente potencial.

Os Perfis são considerados ativos se tiverem sido direcionados ou comunicados nos últimos 12 meses por meio de qualquer canal.

>[!NOTE]
>
>Os canais Facebook e Twitter não são considerados.

Para obter mais informações sobre perfis ativos, consulte as documentações [Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) e [Campaign Classic](https://docs.adobe.com/content/help/en/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles) .

## Monitoramento de perfis ativos {#monitoring-active-profiles}

O Painel de controle permite que você monitore a utilização de perfis ativos para cada uma das instâncias de Campanha.

Para fazer isso, siga estas etapas:

1. Abra o cartão **[!UICONTROL Performance Monitoring]** e selecione a guia **[!UICONTROL Active Profiles]**.

1. Selecione a instância desejada no **[!UICONTROL Instance List]**.

1. O número de perfis ativos usados pela instância é exibido, bem como a última vez que o fluxo de trabalho de cobrança foi executado em sua instância.

![](assets/active-profiles-graph.png)

>[!NOTE]
>
>Os perfis ativos são contados com base em workflows técnicos dedicados que são executados diariamente em suas instâncias:
>
>* O fluxo de trabalho [&quot;cobrança&quot;](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html) para o Campaign Standard,
>* O fluxo de trabalho [&quot;Número de perfis de faturamento ativos&quot;](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/technical-workflows/deliveries.html) para o Campaign Classic.


A área inferior fornece uma representação gráfica do uso de perfis ativos nos últimos 30 dias. Você pode alterar o período de tempo exibido para 1 ano usando os filtros disponíveis no canto superior direito.

Passar o mouse sobre uma das barras de gráficos permite obter o número exato de perfis ativos usados no período selecionado.
