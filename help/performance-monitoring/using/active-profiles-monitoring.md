---
product: campaign
solution: Campaign
title: Monitoramento de perfis ativos
description: Saiba como obter informações em tempo real sobre a utilização e evolução mais recente e histórica dos Perfis ativos para cada uma de suas instâncias do Campaign.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: 73cf3102c0926728595e975ee4c85bf110f2a23d
workflow-type: ht
source-wordcount: '418'
ht-degree: 100%

---

# Monitoramento de perfis ativos {#active-profiles-monitoring}

## Sobre perfis ativos {#about-active-profiles}

>[!IMPORTANT]
>
>O monitoramento de perfis ativos pelo Painel de controle está disponível em beta e está sujeito a atualizações e modificações frequentes sem aviso prévio. Está disponível na build Campaign Standard 10368.

De acordo com seu contrato, cada uma das instâncias do Campaign é provisionada com uma quantidade específica de perfis ativos que são contados para fins de faturamento. Consulte seu contrato mais recente para obter uma referência sobre o número de perfis ativos adquiridos.

“Perfil” significa um registro de informações (por exemplo: um registro na tabela nmsRecipient ou uma tabela externa contendo um cookie de identificação, uma identificação do cliente, um identificador para dispositivos móveis ou outras informações relevantes para um canal específico) representando um cliente final, um prospecto ou um cliente potencial.

Os perfis são considerados ativos se tiverem sido direcionados ou comunicados nos últimos 12 meses por meio de qualquer canal.

>[!NOTE]
>
>Os canais do Facebook e X (anteriormente conhecido como Twitter) não são considerados.

Para obter mais informações sobre perfis ativos, consulte as documentações do [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html?lang=pt-BR) e do [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html?lang=pt-BR#active-profiles).

## Monitoramento do uso de perfis ativos {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="Sobre o monitoramento de perfis ativos"
>abstract="Nessa guia, é possível obter informações em tempo real sobre a utilização e evolução dos perfis ativos mais recentes e históricos nas suas instâncias do Campaign e na organização."

Para monitorar o uso de perfis ativos no Painel de controle, navegue até o cartão **[!UICONTROL Monitoramento do desempenho]** > guia **[!UICONTROL Perfis ativos]** e selecione a instância desejada na **[!UICONTROL Lista de instâncias]**.

São exibidas informações sobre o uso de perfis ativos.

![](assets/active-profiles-graph.png)

A seção superior exibe as seguintes informações:

* A contagem de perfis ativos usados atualmente na instância selecionada, juntamente com o carimbo de data e hora da execução mais recente do workflow de faturamento da instância.

* A contagem total de perfis ativos usados pela organização em todas as instâncias.

  >[!NOTE]
  >
  >Essa seção estará visível somente se você possuir várias instâncias associadas à organização.

* A contagem total de perfis ativos alocados para a organização.

A seção inferior fornece uma representação visual do uso de perfis ativos nos últimos 30 dias. É possível alterar esse intervalo de tempo para 1 ano usando o filtro localizado no canto superior direito. Ao passar o mouse sobre o gráfico, é possível obter o número exato de perfis ativos usados no período selecionado.

As informações relacionadas ao uso de perfis ativos são atualizadas no Painel de controle com base em fluxos de trabalho técnicos dedicados ao “Faturamento” do [!DNL Campaign], os quais são executados em intervalos regulares nas suas instâncias.

| Versão do Campaign | Fluxo de trabalho técnico | Execuções |
|  ---  |  ---  |  ---  |
| Campaign Standard | [Faturamento](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=pt-BR) | Diariamente |
| Campaign v7/v8 | [Faturamento](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html?lang=pt-BR) | Mensal |

