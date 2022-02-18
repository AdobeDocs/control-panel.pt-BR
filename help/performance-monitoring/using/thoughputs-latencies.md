---
product: campaign
solution: Campaign
title: Monitoramento de taxas de transferência e latência
description: Saiba como monitorar as taxas de transferência e a latência das instâncias do Campaign no Painel de controle.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 9d3064515b8001207d1edd20c371facca01c7b5d
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 100%

---

# Monitoramento de taxas de transferência e latência {#throughputs-latency-monitoring}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_throughputslatencies"
>title="Sobre monitoramento de taxas de transferência e latência "
>abstract="Nesta guia, é possível monitorar a tendência das taxas de transferência e latência de entrega ao longo de um período em suas instâncias."

Monitorar a tendência das taxas de transferência e da latência de entrega ao longo de um período é essencial para entender o uso de suas instâncias e garantir elas estejam apresentando um bom desempenho.

Essas informações são disponibilizadas no painel de controle para cada uma das instâncias do Campaign no cartão **[!UICONTROL Performance Monitoring]**, na guia **[!UICONTROL Throughputs & Latency]** (observe que o painel de controle pode levar até 1 hora para exibir os números).

* A área **[!UICONTROL Throughput]** fornece informações sobre o número de mensagens enviadas por hora desde a instância selecionada do Campaign para todos os canais de comunicação aos quais você está habilitado.

* A área **[!UICONTROL Latency]** fornece informações sobre a latência encontrada na instância selecionada ao enviar comunicações transacionais em tempo real. As latências são capturadas e visualizadas nos percentis 95 e 99, o que significa que 95% e 99% das solicitações devem ser mais rápidas do que a latência fornecida.

![](assets/throughput-latencies-overview.png)

>[!NOTE]
>
>Todos os valores apresentados nesta área são aproximados e meramente informativos.

Por padrão, os dados são exibidos para o dia atual. Você pode alterar o período exibido usando os botões **[!UICONTROL 6 months]**, **[!UICONTROL 30 days]** e **[!UICONTROL 7 days]**.

Também é possível visualizar essas informações em formato tabular com colunas classificáveis, em vez de em um gráfico. Para fazer isso, clique no botão **[!UICONTROL Visualization settings]** e selecione **[!UICONTROL Table]**.

![](assets/throughput-latencies-table.png)
