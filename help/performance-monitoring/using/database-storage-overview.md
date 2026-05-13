---
product: campaign
solution: Campaign
title: Visão geral do armazenamento
description: Saiba como usar o Painel de controle para monitorar os diferentes recursos do Campaign que estão consumindo espaço no banco de dados das suas instâncias.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
TQID: https://experienceleague.adobe.com/3zcScy61C5LHsWM86WWWuy0uic-pdNQGKc0qY7ewwOQ
product_v2: id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 06babfad697fb874f2b77c5204e30580c55cd0d1
workflow-type: tm+mt
source-wordcount: 180
ht-degree: 100%

---

# Visão geral do armazenamento {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="Sobre a visão geral do armazenamento"
>abstract="Nesta guia, você pode obter informações detalhadas sobre os diferentes recursos do Campaign que estão consumindo espaço no banco de dados."

A área **[!UICONTROL Visão geral do armazenamento]** fornece uma representação gráfica do espaço ocupado por:

* **[!UICONTROL Recursos do sistema]**

  Observe que, se os recursos do sistema estiverem consumindo uma grande parte do espaço do banco de dados, recomendamos entrar em contato com o Atendimento ao cliente.

* **[!UICONTROL Tabelas prontas para uso]** fornecidas por padrão com as instâncias do Campaign,
* **[!UICONTROL Tabelas temporárias]** criadas por fluxos de trabalho e entregas,
* **[!UICONTROL Tabelas que não são prontas para uso]** geradas após a criação de recursos personalizados.

![](assets/database-storage-overview.png)

Clique no botão **[!UICONTROL Exibir detalhes]** para mais detalhes sobre os diferentes ativos que estão consumindo espaço no banco de dados.

É possível usar a lista suspensa para refinar a pesquisa e exibir as tabelas com apenas um tipo de ativo específico (workflows, entregas, destinatários).

![](assets/database-storage-details.png)

Observe que essa tela também permite monitorar os parâmetros dos fluxos de trabalho que podem exigir atenção específica para evitar problemas nas suas instâncias. Saiba mais [nesta página](workflow-monitoring.md).
