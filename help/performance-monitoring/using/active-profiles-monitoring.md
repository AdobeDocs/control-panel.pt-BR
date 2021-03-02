---
product: campaign
solution: Campaign
title: Monitoramento de perfis ativos
description: Saiba como obter informações em tempo real sobre a utilização e evolução mais recente e histórica dos Perfis ativos para cada uma de suas instâncias do Campaign.
translation-type: tm+mt
source-git-commit: 90c6d50dcb0d70616745170b5c35e42b7e5d784e
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 97%

---


# Monitoramento de perfis ativos {#active-profiles-monitoring}

## Sobre perfis ativos {#about-active-profiles}

>[!IMPORTANT]
>
>O monitoramento de perfis ativos pelo Painel de controle do Campaign está disponível em beta e está sujeito a atualizações e modificações frequentes sem aviso prévio.
>
>O recurso está disponível para clientes hospedados no AWS a partir da build 10368 do Campaign Standard e da build 8931 do Campaign Classic. Se você estiver usando uma build com versão anterior, será necessário uma atualização para usar esse recurso.

De acordo com seu contrato, cada uma das instâncias do Campaign é provisionada com uma quantidade específica de perfis ativos que são contados para fins de faturamento. Consulte seu contrato mais recente para obter uma referência sobre o número de perfis ativos adquiridos.

“Perfil” significa um registro de informações (por exemplo: um registro na tabela nmsRecipient ou uma tabela externa contendo um cookie de identificação, uma identificação do cliente, um identificador para dispositivos móveis ou outras informações relevantes para um canal específico) representando um cliente final, um prospecto ou um cliente potencial.

Os perfis são considerados ativos se tiverem sido direcionados ou comunicados nos últimos 12 meses por meio de qualquer canal.

>[!NOTE]
>
>Os canais Facebook e Twitter não são considerados.

Para obter mais informações sobre Perfis ativos, consulte as documentações do [Campaign Standard](https://docs.adobe.com/content/help/pt-BR/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) e do [Campaign Classic](https://docs.adobe.com/content/help/pt-BR/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles).

## Monitoramento de perfis ativos {#monitoring-active-profiles}

O Painel de controle do Campaign permite monitorar a utilização de perfis ativos para cada uma das instâncias do Campaign.

Para fazer isso, siga estes passos:

1. Abra o **[!UICONTROL Performance Monitoring]** cartão e selecione a **[!UICONTROL Active Profiles]** guia.

1. Selecione a instância desejada em **[!UICONTROL Instance List]**.

1. O número de perfis ativos usados pela instância é exibido, bem como a última vez que o workflow de cobrança foi executado em sua instância.

![](assets/active-profiles-graph.png)

>[!NOTE]
>
>Os perfis ativos são contados com base em workflows técnicos dedicados que são executados diariamente em suas instâncias:
>
>* O workflow [&quot;Faturamento&quot;](https://docs.adobe.com/help/pt-BR/campaign-standard/using/administrating/application-settings/technical-workflows.html) para o Campaign Standard,
>* O workflow [&quot;Número de perfis de faturamento ativos&quot;](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html) para o Campaign Classic.


A área inferior fornece uma representação gráfica do uso de perfis ativos nos últimos 30 dias. Você pode alterar o período exibido para 1 ano usando os filtros disponíveis no canto superior direito.

Você pode obter o número exato de perfis ativos usados no período selecionado, passando o mouse sobre uma das barras de gráfico.
