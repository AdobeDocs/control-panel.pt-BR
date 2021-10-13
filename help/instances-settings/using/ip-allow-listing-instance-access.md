---
product: campaign
solution: Campaign
title: Lista de permissões de IP
description: Saiba como adicionar endereços IP à lista de permissões no Painel de controle do Campaign para obter acesso à instância
feature: Control Panel
role: Architect
level: Intermediate
exl-id: 1d1eeff8-969e-4529-b947-2a68defb8d13
source-git-commit: cca04cd965c00a9e2bc496de632ee41ce53a166a
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 89%

---

# Lista de permissões de IP {#ip-allow-listing}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange"
>title="Sobre a lista de permissões de IP"
>abstract="Adicione endereços IP à lista de permissões para acessar suas instâncias."
>additional-url="https://images-tv.adobe.com/mpcv3/045cac99-f948-478e-ae04-f8c161dcb9e2_1568132508.1920x1080at3000_h264.mp4" text="Assista ao vídeo de demonstração"

## Sobre a lista de permissões de IP {#about-ip-allow-listing}

>[!IMPORTANT]
>
>Esse recurso está disponível somente para instâncias do Campaign Classic v7 e Campaign v8.

Por padrão, a instância do Adobe Campaign não pode ser acessada de vários endereços IP.

Se seu endereço IP não tiver sido incluído na lista de permissões, você não poderá fazer logon na instância com esse endereço. Da mesma forma, talvez você não consiga conectar uma API ao seu Centro de mensagens ou à sua instância de marketing se o endereço IP não tiver sido explicitamente incluído na lista de permissões com a instância.

O Painel de controle do Campaign permite configurar novas conexões às suas instâncias ao adicionar intervalos de endereços IP à lista de permissões. Para fazer isso, siga as etapas descritas abaixo.

Depois que os endereços IP forem exibido na lista de permissões, você poderá criar e vincular operadores do Campaign a eles para que os usuários possam acessar a instância.

![](assets/do-not-localize/how-to-video.png) [Descubra este recurso no vídeo](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/ip-allow-listing.html#instance-settings)

## Práticas recomendadas {#best-practices}

Siga as recomendações e limitações abaixo ao adicionar endereços IP à lista de permissões no Painel de controle do Campaign.

* **Não ative o acesso IP a todos os tipos de acesso** se você não quiser que o endereço IP se conecte aos servidores RT ou à zona de segurança do AEM.
* **Se você ativou temporariamente o acesso à sua instância para um endereço IP**, remova os endereços IP da lista de permissões depois que não precisar mais se conectar à sua instância.
* **Não recomendamos adicionar endereços IP de locais públicos à lista de permissões** (aeroportos, hotéis, etc.). Use o endereço VPN da sua empresa para manter a instância sempre segura.

## Adicionar endereços IP à lista de permissões para acessar a instância {#adding-ip-addresses-allow-list}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_iprange_add"
>title="Configuração do intervalo IP"
>abstract="Defina o intervalo IP que deseja adicionar à lista de permissões para se conectar à sua instância."

Para adicionar endereços IP à lista de permissões, siga estas etapas:

1. Abra **[!UICONTROL Instances Settings card]** para acessar a guia da lista de permissões de IP e clique em **[!UICONTROL Add new IP Range]**.

   >[!NOTE]
   >
   >Se o cartão Configurações de instância não estiver visível na página inicial do Painel de controle do Campaign, significa que a ID da organização IMS não está associada a nenhuma instância do Adobe Campaign Classic

   ![](assets/ip_whitelist_list1.png)

1. Preencha as informações para o Intervalo IP que deseja incluir na lista de permissões, conforme descrito abaixo.

   ![](assets/ip_whitelist_add1.png)

   * **[!UICONTROL Instance(s)]**: as instâncias às quais os endereços IP poderão se conectar. Várias instâncias podem ser manipuladas ao mesmo tempo. Por exemplo, a lista de permissões de IP pode ser executada pela mesma etapa em instâncias de Produção e de Estágio.
   * **[!UICONTROL IP Range]**: O intervalo IP que você deseja adicionar à lista de permissões, no formato CIDR. Observe que um intervalo IP não pode sobrepor um intervalo existente na lista de permissões. Nesse caso, primeiro exclua o intervalo que contém o IP sobreposto.

   >[!NOTE]
   >
   >CIDR (Roteamento interdomínio sem classe) é o formato aceito ao adicionar intervalos IP com a interface do Painel de controle do Campaign. A sintaxe consiste em um endereço IP seguido por um caractere &#39;/&#39; e um número decimal. O formato e sua sintaxe são detalhados por completo [neste artigo](https://whatismyipaddress.com/cidr).
   >
   >Você pode procurar na Internet ferramentas online gratuitas que ajudarão você a converter o intervalo IP disponível para o formato CIDR.

   * **[!UICONTROL Label]**: o rótulo que será exibido na lista de permissões.
   * **[!UICONTROL Name]**: o nome deve ser exclusivo para o Tipo de acesso, Instância (no caso de conexão de API externa) e Endereço IP.


1. Especifique o tipo de acesso que deseja conceder aos endereços IP:

   * **[!UICONTROL Campaign Console Access]**: Os endereços IP poderão se conectar ao Console do Cliente do Campaign. Observe que o acesso ao Console é ativado apenas para instâncias de marketing. O acesso à instância MID e RT não é permitido e, portanto, não está habilitado.
   * **[!UICONTROL AEM connection]**: os endereços IP AEM especificados poderão se conectar à instância de marketing.
   * **[!UICONTROL External API connection]**: as APIs externas com os endereços IP especificados poderão se conectar à instância do Centro de mensagens e/ou Marketing (RT). Observe que a conexão com o console de instâncias de RT não está habilitada.

   ![](assets/ip_whitelist_acesstype.png)

1. Clique no botão **[!UICONTROL Save]**. O Intervalo IP é adicionado à lista de permissões.

   ![](assets/ip_whitelist_added.png)

Para excluir intervalos IP da lista de permissões, selecione-os e clique no botão **[!UICONTROL Delete IP range]** .

**Tópicos relacionados:**

* [Vincular uma zona de segurança a um operador](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Linking_a_security_zone_to_an_operator)
