---
product: campaign
solution: Campaign
title: Monitoramento de taxas de transferência e latência
description: Saiba como monitorar as taxas de transferência e a latência das instâncias do Campaign no Painel de controle.
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: cbc068c921d0d16b49c881693e44e1ba2a90d015
workflow-type: ht
source-wordcount: '218'
ht-degree: 100%

---

# Monitoramento de taxas de transferência e latência {#throughputs-latency-monitoring}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_throughputslatencies"
>title="Sobre monitoramento de taxas de transferência e latência "
>abstract="Nesta guia, é possível monitorar a tendência das taxas de transferência e latência de entrega ao longo de um período em suas instâncias."

Monitorar a tendência das taxas de transferência e da latência de entrega ao longo de um período é essencial para entender o uso de suas instâncias e garantir elas estejam apresentando um bom desempenho.

Essas informações são disponibilizadas no Painel de controle do Campaign para cada uma das instâncias no cartão **[!UICONTROL Performance Monitoring]**, na guia **[!UICONTROL Throughputs & Latencies]**.

>[!NOTE]
>
>Todos os valores apresentados nesta área são aproximados e meramente informativos.

![](assets/throughput-latencies-overview.png)

Por padrão, os dados são exibidos para o dia atual. Você pode alterar o período exibido usando os botões **[!UICONTROL 6 months]**, **[!UICONTROL 30 days]** e **[!UICONTROL 7 days]**.

A área **[!UICONTROL Throughput]** fornece informações sobre o número de mensagens enviadas por hora desde a instância selecionada do Campaign para todos os canais de comunicação aos quais você está habilitado.

Também é possível visualizar essas informações em formato tabular com colunas classificáveis em vez de um gráfico. Para fazer isso, clique no botão **[!UICONTROL Visualization settings]** e selecione **[!UICONTROL Table]**.

![](assets/throughput-latencies-table.png)

A área **[!UICONTROL Latency]** fornece informações sobre a latência encontrada na instância selecionada ao enviar comunicações transacionais em tempo real. As latências são capturadas e visualizadas nos percentis 95 e 99, o que significa que 95% e 99% das solicitações devem ser mais rápidas do que a latência fornecida.

![](assets/throughput-latencies-latency.png)
