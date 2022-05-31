---
product: campaign
solution: Campaign
title: Monitoramento de taxas de transferência e latência
description: Saiba como monitorar as taxas de transferência e a latência das instâncias do Campaign no Painel de controle.
feature: Control Panel
role: Architect
level: Experienced
exl-id: eddef17f-0667-4b43-bc56-2b1aeeae61bb
source-git-commit: a5bd04c4659ae18c4f05934f42e071b209a58fff
workflow-type: ht
source-wordcount: '425'
ht-degree: 100%

---

# Monitoramento de taxas de transferência e latência {#throughputs-latency-monitoring}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_throughputslatencies"
>title="Sobre monitoramento de taxas de transferência e latência "
>abstract="Nesta guia, é possível monitorar a tendência das taxas de transferência e latência de entrega ao longo de um período em suas instâncias. Para obter informações sobre entregas que contribuem para a taxa de transferência, alterne para a exibição em tabelas."

O Painel de controle do Campaign permite monitorar a taxa de transferência e a latência da entrega de cada uma de suas instâncias.

>[!IMPORTANT]
>
>Esse recurso está disponível para todos os clientes do Campaign Standard e v8, bem como para clientes do Campaign V7 com builds de número 9032, 9330, 9346 ou 9349 que têm implantações [autônomas](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/deployment-types-/standalone-deployment.html?lang=pt-BR) (sem qualquer instância mid).

Monitorar a tendência das taxas de transferência e da latência da entrega ao longo de um período é essencial para entender o uso de suas instâncias e garantir elas estejam apresentando um bom desempenho.

Essas informações são disponibilizadas no painel de controle para cada uma das instâncias do Campaign no cartão **[!UICONTROL Performance Monitoring]**, na guia **[!UICONTROL Throughputs & Latency]** (observe que o painel de controle pode levar até 1 hora para exibir os números).

>[!NOTE]
>
>Todos os valores apresentados nesta área são aproximados e meramente informativos.

![](assets/throughput-latencies-overview.png)

Por padrão, os dados são exibidos para o dia atual. Você pode alterar o período exibido usando os botões **[!UICONTROL 6 months]**, **[!UICONTROL 30 days]** e **[!UICONTROL 7 days]**. Os dados serão apresentados:
* Por hora, para visualizações de 1 dia e 7 dias,
* A cada 6 horas, para uma visualização de 30 dias,
* Diariamente, para uma visualização de 6 meses.

Também é possível visualizar essas informações em formato tabular com colunas classificáveis, em vez de em um gráfico. Para fazer isso, clique no botão **[!UICONTROL Visualization settings]** e selecione **[!UICONTROL Table]**.

![](assets/throughput-latencies-table.png)

## Monitorar taxa de transferência {#throughput}

A área **[!UICONTROL Throughput]** fornece informações sobre o número de mensagens enviadas por hora desde a instância selecionada do Campaign para todos os canais de comunicação aos quais você está habilitado.

>[!NOTE]
>
>Para o Campaign v7/v8, o número de taxa de transferência exibido é a taxa de transferência obtida das instâncias MID (mid-sourcing). Para implantações de marketing (MKT) autônomas (sem qualquer instância MID), a taxa de transferência da instância MKT é exibida.

Além disso, o Painel de controle do Campaign permite identificar as IDs das 5 principais entregas que estão contribuindo para a taxa de transferência do período selecionado. Essas informações estão disponíveis somente na exibição em tabelas:

![](assets/throughput-latencies-top5.png)

## Monitorar latência {#latency}

A área **[!UICONTROL Latency]** fornece informações sobre a latência encontrada na instância selecionada ao enviar comunicações transacionais em tempo real.

>[!NOTE]
>
>Observe que as informações relacionadas à **Latência do perfil** também estão disponíveis somente para instâncias do [!DNL Campaign Standard].

As latências são capturadas e visualizadas nos percentis 95 e 99, o que significa que 95% e 99% das solicitações devem ser mais rápidas do que a latência fornecida.

![](assets/throughput-latencies-latency.png)

Por padrão, a latência é mostrada para todos os canais. É possível visualizar a latência de um canal específico usando a lista suspensa.

![](assets/throughput-latencies-filter.png)

>[!NOTE]
>
>O filtro de canal está disponível somente para instâncias do Campaign Classic v7/v8.
