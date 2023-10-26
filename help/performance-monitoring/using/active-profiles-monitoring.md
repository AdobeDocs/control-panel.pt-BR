---
product: campaign
solution: Campaign
title: Monitoramento de perfis ativos
description: Saiba como obter informações em tempo real sobre a utilização e evolução mais recente e histórica dos Perfis ativos para cada uma de suas instâncias do Campaign.
feature: Control Panel
role: Architect
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: cb18dbcbb3a575d88d3c13fe3f22a657caea1e7e
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 41%

---

# Monitorar perfis ativos {#active-profiles-monitoring}

## Sobre perfis ativos {#about-active-profiles}

>[!IMPORTANT]
>
>O monitoramento de perfis ativos pelo Painel de controle está disponível em beta e está sujeito a atualizações e modificações frequentes sem aviso prévio. Ele está disponível na build Campaign Standard 10368.

De acordo com seu contrato, cada uma das instâncias do Campaign é provisionada com uma quantidade específica de perfis ativos que são contados para fins de faturamento. Consulte seu contrato mais recente para obter uma referência sobre o número de perfis ativos adquiridos.

“Perfil” significa um registro de informações (por exemplo: um registro na tabela nmsRecipient ou uma tabela externa contendo um cookie de identificação, uma identificação do cliente, um identificador para dispositivos móveis ou outras informações relevantes para um canal específico) representando um cliente final, um prospecto ou um cliente potencial.

Os perfis são considerados ativos se tiverem sido direcionados ou comunicados nos últimos 12 meses por meio de qualquer canal.

>[!NOTE]
>
>Os canais Facebook e Twitter não são considerados.

Para obter mais informações sobre perfis ativos, consulte [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) e [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles) documentações.

## Monitorar o uso de perfis ativos {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="Sobre o monitoramento de perfis ativos"
>abstract="Nesta guia, você pode obter informações em tempo real sobre a utilização e evolução mais recente e histórica dos perfis ativos para cada um nas instâncias do Campaign e em sua organização."

As informações relacionadas ao uso de perfis ativos são atualizadas no Painel de controle com base em perfis dedicados [!DNL Campaign] workflows técnicos que são executados diariamente em suas instâncias:
* O workflow [&quot;Faturamento&quot;](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=pt-BR) para o Campaign Standard,
* A variável [&quot;Número de perfis de faturamento ativos&quot;](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html?lang=pt-BR) fluxo de trabalho do Campaign v7/v8.


Para monitorar o uso do perfil ativo no Painel de controle do Campaign, navegue até o **[!UICONTROL Performance Monitoring]** cartão > **[!UICONTROL Active Profiles]** e selecione a instância desejada na guia **[!UICONTROL Instance List]**.

São exibidas informações sobre o uso de perfis ativos.

![](assets/active-profiles-graph.png)

A seção superior exibe as seguintes informações:

* A contagem de perfis ativos usados atualmente na instância selecionada, juntamente com o carimbo de data e hora da execução mais recente do fluxo de trabalho de faturamento da instância.

* A contagem total de perfis ativos usados em sua organização em todas as instâncias.

  >[!NOTE]
  >
  >Essa seção estará visível somente se você tiver várias instâncias associadas à sua organização.

* A contagem total de perfis ativos alocados para sua organização.

A seção inferior fornece uma representação visual do uso do perfil ativo nos últimos 30 dias. É possível alterar esse intervalo de tempo para 1 ano usando o filtro localizado no canto superior direito. Passar o mouse sobre o gráfico permite obter o número exato de perfis ativos usados no período selecionado.
