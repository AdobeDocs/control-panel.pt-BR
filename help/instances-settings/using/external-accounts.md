---
product: campaign
solution: Campaign
title: Adicionar instâncias MID/RT (modelo híbrido)
description: Saiba como adicionar instâncias MID/RT ao Painel de controle com o modelo de hospedagem híbrida.
feature: Control Panel
role: Architect
level: Intermediate
exl-id: ff64acbe-d8cb-499b-b20f-b0934fb0f695
source-git-commit: 96d18b56f70a6a8bf0270a5c94f5ba16923d0e9f
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 100%

---

# Adicionar instâncias MID/RT (modelo híbrido){#add-mid-rt-instances-hybrid-model}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts"
>title="Contas externas"
>abstract="Nesta tela, os clientes com modelo de hospedagem híbrida podem fornecer o URL da instância MID/RT configurado na instância de marketing do Painel de controle para aproveitar seus recursos."

O Painel de controle permite que clientes com o modelo de hospedagem híbrida aproveitem seus recursos específicos. Para fazer isso, você precisa:

* [Fornecer o URL da instância MID/RT](#add) configurado na sua instância de marketing no Painel de controle,
* [Adicionar o endereço IP da instância MID/RT à lista de permissões](#ip) para permitir que a instância de marketing se conecte a ela.

Para obter mais informações sobre modelos de hospedagem, consulte a [Documentação do Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/architecture-and-hosting-models/hosting-models-lp/hosting-models.html?lang=pt-BR).

## Adicionar uma instância MID/RT {#add}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_url"
>title="URL"
>abstract="O URL da instância, que pode ser encontrado no Console do cliente do Campaign, no menu Administração > Plataforma > Contas externas."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_operator"
>title="Operador"
>abstract="ID do operador fornecida após o provisionamento inicial pelo administrador da Adobe."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_password"
>title="Senha"
>abstract="Senha do operador fornecida após o provisionamento inicial pelo administrador da Adobe."

Os clientes híbridos devem se conectar ao Painel de controle por meio da Experience Cloud. Ao acessar o Painel de controle pela primeira vez, somente dois cartões serão exibidos na página inicial.

![](assets/hybrid-homepage.png)

>[!NOTE]
>
>Caso tenha problemas para acessar o Painel de controle, é provável que sua instância de marketing ainda não esteja mapeada com a [ID da sua organização](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=pt-BR). Entre em contato com o Atendimento ao cliente para concluir a configuração e prosseguir. Após uma conexão bem-sucedida, você verá a página inicial do Painel de controle.

Para acessar os recursos do Painel de controle, é preciso inserir as informações da instância MID/RT no cartão **[!UICONTROL Instances Settings]**. Para fazer isso, siga as etapas abaixo.

1. No cartão **[!UICONTROL Instances Settings]**, selecione a guia **[!UICONTROL External Accounts]**. 

1. Selecione a instância de marketing desejada na lista suspensa e clique em **[!UICONTROL Add new URL]**.

   ![](assets/external-account-addbutton.png)

1. Forneça informações sobre a instância MID/RT que será adicionada.

   ![](assets/external-account-add.png)

   * **[!UICONTROL URL]**: o URL da instância, que pode ser encontrado no Console do cliente do Campaign, no menu **[!UICONTROL Administration]** > **[!UICONTROL Platform]** > **[!UICONTROL External Accounts]**.

     ![](assets/external-account-url.png)

   * **[!UICONTROL Operator]** / **[!UICONTROL Password]**: credenciais do operador fornecidas após o provisionamento inicial pelo administrador da Adobe.

     >[!NOTE]
     >
     >Se esses detalhes não estiverem disponíveis, entre em contato com o Atendimento ao cliente.

1. Clique em **[!UICONTROL Save]** para confirmar.

Ao adicionar o URL de MID/RT, um processo assíncrono é acionado para validar a exatidão dos URLs. Esse processo pode levar alguns minutos. Até que o URL da instância MID/RT seja validado, o processo permanecerá pendente. Somente após a conclusão da validação será possível acessar os principais recursos do Painel de controle.

![](assets/external-account-pending.png)

Você pode remover ou desativar um URL de instância MID/RT a qualquer momento, selecionando-o na lista.

![](assets/external-account-edit.png)

Observe que é possível monitorar qualquer ação executada na guia **[!UICONTROL External Accounts]** em um URL de instância MID/RT a partir do **[!UICONTROL Job Logs]**:

![](assets/external-account-logs.png)

## Adicionar o endereço IP à lista de permissões {#ip}

Depois que a instância MID/RT for adicionada, será necessário adicionar seu endereço IP à lista de permissões para que sua instância de marketing possa se conectar a ela.

Isso pode ser feito a partir da guia **[!UICONTROL IP Allow Listing]** no cartão **[!UICONTROL Instances Settings]**. [Saiba como adicionar endereços IP à lista de permissões](ip-allow-listing-instance-access.md)

Após concluído, será possível usar os recursos do Painel de controle com sua instância MID/RT.

## Recursos disponíveis para clientes híbridos {#capabilities}

Depois que uma instância MID/RT for adicionada ao Painel de controle, você poderá aproveitar os recursos listados abaixo:

* [Monitorar contatos importantes e eventos](../../service-events/service-events.md)
* [Exibir detalhes da instância](../../instances-settings/using/instance-details.md),
* [Adicionar endereços IP à lista de permissões](../../instances-settings/using/ip-allow-listing-instance-access.md),
* [Configurar novos subdomínios](../../subdomains-certificates/using/setting-up-new-subdomain.md),
* [Renovar certificados SSL de subdomínios](../../subdomains-certificates/using/renewing-subdomain-certificate.md).
