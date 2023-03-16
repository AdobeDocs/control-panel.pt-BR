---
product: campaign
solution: Campaign
title: Visão geral de armazenamento
description: Saiba como monitorar no Painel de controle do Campaign os diferentes recursos do Campaign que estão consumindo espaço no banco de dados em suas instâncias.
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: c52094b8145bdd84aa9e71430a811b8a7b32354d
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 59%

---

# Visão geral de armazenamento {#storage-overview}

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

Você pode usar a lista suspensa para refinar suas tabelas de pesquisa e exibição somente de um tipo de ativo específico (fluxos de trabalho, deliveries, recipients).

![](assets/database-storage-details.png)

Observe que essa tela também permite monitorar parâmetros de fluxo de trabalho que podem exigir atenção específica para evitar problemas em suas instâncias. Saiba mais [nesta página](workflow-monitoring.md).
