---
product: campaign
solution: Campaign
title: Visão geral de armazenamento
description: Saiba como monitorar no Painel de controle os diferentes recursos do Campaign que estão consumindo espaço no banco de dados em suas instâncias.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 30%

---

# Visão geral de armazenamento {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="Sobre a visão geral do armazenamento"
>abstract="Nesta guia, você pode obter informações detalhadas sobre os diferentes recursos do Campaign que estão consumindo espaço no banco de dados."

A variável **[!UICONTROL Visão geral de armazenamento]** fornece uma representação gráfica do espaço ocupado por:

* **[!UICONTROL Recursos do sistema]**

  Observe que, se os recursos do sistema estiverem consumindo uma grande parte do espaço do banco de dados, recomendamos entrar em contato com o Atendimento ao cliente.

* **[!UICONTROL Tabelas prontas para uso]** fornecido por padrão com as instâncias do Campaign,
* **[!UICONTROL Tabelas temporários]** criados por workflows e deliveries,
* **[!UICONTROL Tabelas não prontas para uso]** gerado após a criação de recursos personalizados.

![](assets/database-storage-overview.png)

Clique em **[!UICONTROL Exibir detalhes]** botão para obter mais detalhes sobre os diferentes ativos que estão consumindo espaço no banco de dados.

Você pode usar a lista suspensa para refinar suas tabelas de pesquisa e exibição somente de um tipo de ativo específico (workflows, deliveries, recipients).

![](assets/database-storage-details.png)

Observe que essa tela também permite monitorar parâmetros de fluxo de trabalho que podem exigir atenção específica para evitar problemas em suas instâncias. Saiba mais [nesta página](workflow-monitoring.md).
