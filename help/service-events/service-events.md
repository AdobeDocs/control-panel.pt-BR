---
product: campaign
solution: Campaign
title: Monitorar contatos importantes e eventos
description: Saiba como identificar eventos que ocorrem em suas instâncias e contatos importantes na Adobe.
feature: Control Panel
role: Architect
level: Intermediate
exl-id: d230aae6-4f0e-4201-bb3c-0e3f83a7c1b8
source-git-commit: 8d1eda31cbe6ab915760d4894a03a4a0055a3130
workflow-type: ht
source-wordcount: '497'
ht-degree: 100%

---

# Monitorar contatos importantes e eventos {#keycontacts-events}

>[!CONTEXTUALHELP]
>id="cp_servicecalendar_serviceevents"
>title="Calendário de serviço"
>abstract="A seção Contatos importantes lista as pessoas na Adobe a serem contatadas para qualquer solicitação ou problema em suas instâncias. Na seção Calendário de evento do serviço, você pode identificar versões e revisões de serviço para a instância selecionada e configurar lembretes para eventos futuros."

>[!IMPORTANT]
>
>O Calendário de serviço está disponível na versão beta e está sujeito a atualizações e modificações frequentes sem aviso prévio.

Identificar eventos planejados em suas instâncias é essencial para monitorar as instâncias do Campaign.

Com o Painel de controle do Campaign, você pode monitorar versões e revisões de serviços que ocorrem em suas instâncias e acessar uma lista de contatos importantes na Adobe para qualquer solicitação ou problema.

Essas informações podem ser acessadas no cartão **[!UICONTROL Service Calendar]**, na página inicial do Painel de controle do Campaign.

## Contatos importantes {#key-contacts}

A seção **[!UICONTROL Key contacts]** lista as pessoas na Adobe que você pode contatar para qualquer solicitação ou problema em suas instâncias.

>[!NOTE]
>
>Esta seção mostrará informações somente para contas do Managed Services.

![](assets/service-events-contacts.png)

Os contatos importantes incluem as seguintes funções:

* **[!UICONTROL TAM]**: gerente técnico de contas,
* **[!UICONTROL CSM]**: gerente de sucesso do cliente,
* **[!UICONTROL Deliverability]**: ponto de contato para operações de capacidade de delivery,
* **[!UICONTROL Transition Manager]**: gerente de transição do Managed Services (somente para contas do Managed Services),
* **[!UICONTROL On-boarding Specialist]**: especialista atribuído à conta para ajudá-lo a começar no Campaign Classic (somente para contas do Managed Services).

## Eventos {#events}

### Monitorar eventos {#monitor-events}

A seção **[!UICONTROL Service Event Calendar]** mostra todas as versões e revisões de serviço anteriores e futuras da instância selecionada.

![](assets/service-events-calendar.png)

A coluna **[!UICONTROL Note]** fornece informações sobre o status de cada versão:

* **[!UICONTROL General availability]**: build estável disponível mais recente.
* **[!UICONTROL Limited availability]**: implantação somente sob demanda.
* **[!UICONTROL Release candidate]**: engenharia validada. Aguardando prova de produção.
* **[!UICONTROL Pre release]**: disponibilidade antecipada para necessidades específicas do cliente.
* **[!UICONTROL No longer available]**: a build não tem nenhum grande problema, mas uma nova versão está disponível com correções de erros adicionais. É necessária uma atualização.
* **[!UICONTROL Deprecated]**: a build incorpora regressões conhecidas.
A build não tem mais suporte. Uma atualização é obrigatória.

É possível atribuir um sinalizador a um ou vários eventos futuros para rastreá-los. Para fazer isso, clique no botão de elipse ao lado do nome do evento.

![](assets/service-events-flag.png)

### Definir lembretes {#reminders}

Com o Calendário de serviço, você pode definir lembretes para ser notificado por email antes que um evento ocorra.

>[!NOTE]
>
>Para ser notificado sobre eventos futuros, inscreva-se no sistema de alertas de email do Painel de controle do Campaign. [Saiba mais](../performance-monitoring/using/email-alerting.md)

Para definir um alerta para um evento, siga estas etapas:

1. Clique no botão de elipse ao lado do evento do qual você deseja ser lembrado e selecione **[!UICONTROL Set Reminder]**.

1. Forneça um título para o lembrete e selecione a data em que deseja ser notificado antes que o evento ocorra.

   ![](assets/service-events-set-reminder.png)

   >[!NOTE]
   >
   >Se você não se inscreveu nos alertas do Painel de controle do Campaign, uma mensagem será exibida e permitirá que você se inscreva para receber notificações por email.

1. O lembrete agora está definido para o evento selecionado. Você pode passar o mouse sobre ele a qualquer momento para exibir seu título.

   ![](assets/service-events-reminder.png)

   >[!NOTE]
   >
   >Você pode configurar até dois lembretes para o mesmo evento.

1. Na data especificada no lembrete, um email será enviado para notificá-lo sobre o evento futuro, e o lembrete será removido automaticamente da lista **[!UICONTROL Reminders]** do menu Calendário de serviço.
