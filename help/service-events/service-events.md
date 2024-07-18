---
product: campaign
solution: Campaign
title: Identificar contatos importantes e eventos
description: Saiba como identificar eventos que ocorrem em suas instâncias e contatos importantes na Adobe.
feature: Control Panel, Monitoring
role: Admin
level: Intermediate
exl-id: d230aae6-4f0e-4201-bb3c-0e3f83a7c1b8
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 100%

---

# Identificar contatos importantes e eventos {#keycontacts-events}

>[!CONTEXTUALHELP]
>id="cp_servicecalendar_serviceevents"
>title="Calendário de serviço"
>abstract="A seção Contatos importantes lista as pessoas na Adobe a serem contatadas para qualquer solicitação ou problema em suas instâncias. Na seção Calendário de eventos de serviço, você pode identificar versões e alertas anteriores/futuros para a instância selecionada, bem como configurar lembretes para um determinado evento."

>[!IMPORTANT]
>
>O Calendário de serviço está disponível na versão beta e está sujeito a atualizações e modificações frequentes sem aviso prévio.

Para monitorar com eficiência as instâncias do Campaign, é crucial acompanhar eventos importantes que tenham potencial para afetar sua(s) instância(s). O Painel de controle permite identificar eventos como novas versões, atualizações, correções, correções rápidas etc., e fornece uma lista de contatos importantes da Adobe para qualquer solicitação ou problema.

Essas informações podem ser acessadas a partir do cartão **[!UICONTROL Calendário de serviços]** na página inicial do Painel de controle.

## Contatos importantes {#key-contacts}

A seção **[!UICONTROL Contatos importantes]** lista as pessoas da Adobe que você pode contatar para qualquer solicitação ou problema nas suas instâncias.

>[!NOTE]
>
>Esta seção mostra informações apenas para Contas do Managed Services.

![](assets/service-events-contacts.png)

Os contatos importantes incluem as seguintes funções:

* **[!UICONTROL TAM]**: Gerente Técnico de Contas,
* **[!UICONTROL CSM]**: Gerente de Sucesso do Cliente,
* **[!UICONTROL Capacidade de entrega]**: ponto de contato para operações de capacidade de entrega,
* **[!UICONTROL Gerente de transição]**: gerente de transição do Managed Services (somente para contas do Managed Services),
* **[!UICONTROL Especialista em integração]**: especialista atribuído à conta para auxiliar na integração ao Campaign Classic (somente para contas do Managed Services).

## Acompanhe eventos importantes {#events}

A seção **[!UICONTROL Calendário de eventos de serviço]** mostra todas as versões anteriores e futuras, bem como os alertas nos quais as pessoas se inscreveram, nos alertas por email do Painel de controle. Além disso, o Painel de controle permite que os usuários definam lembretes e sinalizem eventos relevantes para a instância selecionada para que eles sejam mais bem organizados e eficientes.

Os eventos são exibidos em um calendário ou em uma lista. É possível alternar entre as duas exibições, usando os botões **[!UICONTROL Calendário]** e **[!UICONTROL Lista]** no canto superior direito da seção.

![](assets/service-events-calendar.png)

<table><tr style="border: 0;">
<td><img src="assets/do-not-localize/nav-buttons.png">
</td><td>Na exibição de calendário, os botões de navegação estão disponíveis no canto superior direito para ajudá-lo a navegar pelos eventos. Use as <b>setas duplas</b> para navegar até o primeiro evento presente após/antes do mês selecionado e <b>setas simples</b> para navegar de um mês para outro. Clique em <b>botão de círculo</b> para voltar à exibição de hoje.</td>
</tr></table>

Três tipos de eventos são exibidos:

* **Lembretes** são definidos por usuários para serem notificados antes da ocorrência de um evento. Eles são mostrados em verde na exibição de calendário. [Saiba como definir um lembrete](#reminders)
* **Alertas** são enviados por email pelo Painel de controle para notificar usuários sobre problemas em suas instâncias, como sobrecarga de armazenamento ou expiração de certificado SSL. Eles são exibidos em laranja na exibição de calendário. A descrição do evento especifica se o alerta é enviado para o usuário conectado, dependendo de sua assinatura de alertas de email. [Saiba mais sobre os recursos de alerta por email do Painel de controle](../performance-monitoring/using/email-alerting.md)

* **Versões** indica as implantações anteriores e futuras da instância, mostradas respectivamente em cinza e azul na exibição de calendário. Os detalhes do evento especificam o tipo de versão associado a cada implantação:

   * **[!UICONTROL Disponibilidade geral]**: build estável mais recente disponível.
   * **[!UICONTROL Disponibilidade limitada]**: somente implantação sob demanda.
   * **[!UICONTROL Candidato a lançamento]**: validado pela engenharia. Aguardando prova de produção.
   * **[!UICONTROL Pré-lançamento]**: disponibilidade antecipada para necessidades específicas de clientes.
   * **[!UICONTROL Não está mais disponível]**: a build não contém nenhum problema importante, mas uma versão mais recente está disponível com correções de bugs adicionais. É necessária uma atualização.
   * **[!UICONTROL Obsoleto]**: um build que incorpora regressões conhecidas. A build não tem mais suporte. Uma atualização é obrigatória.

É possível atribuir um sinalizador a um ou vários eventos futuros para rastreá-los. Para fazer isso, clique no botão de reticências ao lado do nome do evento.

![](assets/service-events-flag.png)

## Definir lembretes {#reminders}

Com o Calendário de serviço, você pode definir lembretes para ser notificado por email antes que um evento ocorra.

>[!NOTE]
>
>Para ser notificado sobre eventos futuros, inscreva-se no sistema de alertas de email do Painel de controle. [Saiba mais](../performance-monitoring/using/email-alerting.md)

Para definir um alerta para um evento, siga estas etapas:

1. Passe o cursor do mouse sobre o evento do qual você deseja ser lembrado ou clique no botão de reticências na exibição de lista e selecione **[!UICONTROL Definir lembrete]**.

1. Forneça um título para o lembrete e selecione a data em que deseja ser notificado antes que o evento ocorra.

   ![](assets/service-events-set-reminder.png)

   >[!NOTE]
   >
   >Se você não se inscreveu nos alertas do Painel de controle, uma mensagem será exibida e permitirá que você se inscreva para receber notificações por email.

1. O lembrete agora está definido para o evento selecionado. Você pode passar o mouse sobre ele a qualquer momento para exibir seu título.

   ![](assets/service-events-reminder.png)

   >[!NOTE]
   >
   >Você pode configurar até dois lembretes para o mesmo evento.

1. Na data especificada no lembrete, um email será enviado para notificar sobre o evento futuro, e o lembrete será removido automaticamente da contagem de **[!UICONTROL Lembretes]** no menu do Calendário de serviço.
