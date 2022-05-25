---
product: campaign
solution: Campaign
title: Adicionar instâncias MID/RT (modelo híbrido)
description: Saiba como adicionar instâncias MID/RT ao Painel de controle do Campaign com modelo de hospedagem híbrida.
feature: Control Panel
role: Architect
level: Intermediate
source-git-commit: 2458263ef5981a16d983912b498e320501df7889
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 3%

---


# Adicionar instâncias MID/RT (modelo híbrido)

>[!CONTEXTUALHELP]
>id="cp_externalaccounts"
>title="Contas externas"
>abstract="Nesta tela, os clientes com modelo de hospedagem híbrida podem fornecer o URL da instância MID/RT configurado na instância de marketing no Painel de controle do Campaign para aproveitar os recursos do Painel de controle do Campaign."

O Painel de controle do Campaign permite que clientes com modelo de hospedagem híbrida aproveitem recursos específicos do Painel de controle do Campaign. Para fazer isso, é necessário fornecer o URL da instância MID/RT configurado em sua instância de marketing no Painel de controle do Campaign.

Para obter mais informações sobre modelos de hospedagem, consulte [Documentação do Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/architecture-and-hosting-models/hosting-models-lp/hosting-models.html).

## Adicionar uma instância MID/RT {#add}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_url"
>title="URL"
>abstract="O URL da instância, que pode ser encontrado no Console do cliente do Campaign no menu Administration > Platform > External Accounts ."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_operator"
>title="Operador"
>abstract="ID do operador fornecida após o provisionamento inicial pelo Adobe Admin."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_password"
>title="Senha"
>abstract="Senha do operador fornecida após o provisionamento inicial pelo Adobe Admin."

Os clientes híbridos devem se conectar ao Painel de controle do Campaign por meio do Experience Cloud. Ao acessar o Painel de controle pela primeira vez, somente dois cartões são exibidos na página inicial.

![](assets/hybrid-homepage.png)

>[!NOTE]
>
>Caso tenha problemas para acessar o Painel de controle do Campaign, é provável que sua instância de marketing ainda não esteja mapeada com a ID da organização. Entre em contato com o Atendimento ao cliente para concluir essa configuração e prosseguir. Ao se conectar com êxito, você verá a página inicial do Painel de controle do Campaign.

Para acessar os recursos do Painel de controle do Campaign, você precisa fornecer as informações da instância MID/RT no **[!UICONTROL Instances Settings]** cartão. Para fazer isso, siga as etapas abaixo.

1. No **[!UICONTROL Instances Settings]** , selecione o **[!UICONTROL External Accounts]** guia .

1. Selecione a instância de marketing desejada na lista suspensa e clique em **[!UICONTROL Add new URL]**.

   ![](assets/external-account-addbutton.png)

1. Forneça informações sobre a instância MID/RT a ser adicionada.

   ![](assets/external-account-add.png)

   * **[!UICONTROL URL]**: O URL da instância, que pode ser encontrado no Console do Cliente do Campaign no **[!UICONTROL Administration]** > **[!UICONTROL Platform]** > **[!UICONTROL External Accounts]** menu.

      ![](assets/external-account-url.png)

   * **[!UICONTROL Operator]** / **[!UICONTROL Password]**: Credenciais do operador fornecidas após o provisionamento inicial pelo Adobe Admin.

      >[!NOTE]
      >
      >Se esses detalhes não estiverem disponíveis, entre em contato com o Atendimento ao cliente.

1. Clique em **[!UICONTROL Save]** para confirmar.

Ao adicionar o URL de MID/RT, um processo assíncrono é acionado para validar a exatidão dos URLs. Esse processo pode levar alguns minutos. Até que o URL da instância MID/RT seja validado, o trabalho estará pendente. Somente após a conclusão da validação é possível acessar os principais recursos do Painel de controle do Campaign.

![](assets/external-account-pending.png)

Você pode remover ou desativar um URL de instância MID/RT a qualquer momento, selecionando-o na lista.

![](assets/external-account-edit.png)

Observe que você pode monitorar qualquer ação executada na **[!UICONTROL External Accounts]** em um URL de instância MID/RT do **[!UICONTROL Job Logs]**:

![](assets/external-account-logs.png)

## Recursos disponíveis para clientes híbridos {#capabilities}

Depois que uma instância MID/RT é adicionada ao Painel de controle do Campaign, você pode aproveitar os recursos listados abaixo:

* [Monitorar contatos importantes e eventos](../../service-events/service-events.md)
* [Exibir detalhes da instância](../../instances-settings/using/instance-details.md),
* [Adicionar endereços IP à lista de permissões](../../instances-settings/using/ip-allow-listing-instance-access.md) (para instâncias de RT),
* [Exibir informações sobre subdomínios delegados](../../subdomains-certificates/using/monitoring-subdomains.md),
* [Exibir informações sobre certificados SSL](../../subdomains-certificates/using/monitoring-ssl-certificates.md).