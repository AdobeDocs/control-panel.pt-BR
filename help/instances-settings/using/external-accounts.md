---
product: campaign
solution: Campaign
title: Conectar instâncias MID/RT
description: Saiba como conectar instâncias MID/RT ao Painel de controle do Campaign.
feature: Control Panel
role: Architect
level: Intermediate
source-git-commit: 1b712300bd7a1ef8dc784fa977f938bacc4c5e5b
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 7%

---


# Conectar instâncias MID/RT

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_url"
>title="Detalhes do subdomínio"
>abstract="Nesta tela, os clientes com um modelo de hospedagem híbrido podem fornecer suas instâncias de MID/RT presentes em suas instâncias de marketing para executar ações específicas no Painel de controle do Campaign."

O Painel de controle do Campaign permite que os clientes com um modelo de hospedagem híbrida executem uma ação específica no Painel de controle do Campaign fornecendo suas instâncias de MID/RT presentes em suas instâncias de marketing. Para obter mais informações sobre modelos de hospedagem, consulte [Documentação do Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/architecture-and-hosting-models/hosting-models-lp/hosting-models.html).

## Conectar uma instância MID/RT {#connect}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_operator"
>title="Detalhes do subdomínio"
>abstract="ID do operador usado no Console do cliente para adicionar a instância MID/RT na instância de marketing."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_password"
>title="Detalhes do subdomínio"
>abstract="Senha do operador usado no Console do cliente para adicionar a instância MID/RT na instância de marketing."

Para fornecer uma instância MID/RT no Painel de controle do Campaign, siga estas etapas:

1. No **[!UICONTROL Instances Settings]** , selecione o **[!UICONTROL External Accounts]** guia .

1. Selecione a instância de marketing na lista suspensa e clique em **[!UICONTROL Add new URL]**.

   ![](assets/external-account-addbutton.png)

1. Forneça informações sobre a instância MID/RT para conexão:
   * **[!UICONTROL URL]**: URL da instância,
   * **[!UICONTROL Operator]** / **[!UICONTROL Password]**: Credenciais do operador usado no Console do Cliente para adicionar a instância MID/RT na instância de marketing.

   ![](assets/external-account-add.png)

1. Clique em **[!UICONTROL Save]** para confirmar.

Sua instância agora está conectada ao Painel de controle do Campaign. Você pode remover ou desativar uma conexão a qualquer momento selecionando-a na lista.

![](assets/external-account-edit.png)

## Recursos disponíveis para instâncias MID/RT {#capabilities}

Depois que uma instância MID/RT é conectada ao Painel de controle do Campaign, você pode aproveitar os recursos listados abaixo para monitorá-la:

* [Exibir detalhes da instância](../../instances-settings/using/instance-details.md),
* [Adicione endereços IP à lista de permissões para acessar suas instâncias](../../instances-settings/using/ip-allow-listing-instance-access.md),
* [Exibir informações sobre subdomínios delegados](../../subdomains-certificates/using/setting-up-new-subdomain.md),
* [Exibir informações sobre certificados SSL](../../subdomains-certificates/using/monitoring-ssl-certificates.md).
