---
product: campaign
solution: Campaign
title: Acesso ao Painel de controle
description: Saiba como acessar o Painel de controle
feature: Control Panel, Access Management
role: Admin
level: Experienced
exl-id: eb67af6e-a64e-49a7-9656-782f91bc1d67
TQID: https://experienceleague.adobe.com/Ug0vHjgyTK-BRO4IMdCwSQuiwO--XagzjW-MFTPcZrY
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 57345245341bf2d04b9b01611d502532ba8f175b
workflow-type: ht
source-wordcount: 353
ht-degree: 100%

---

# Acesso ao Painel de controle {#accessing-control-panel}

O painel de controle está disponível diretamente na Experience Cloud ou no próprio produto.

## Pré-requisitos {#prerequisites}

No caso do Campaign v7, observe que a sua instância deve estar hospedada no Amazon Web Services (AWS) e atualizada para a [build estável do Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=pt-BR#rn-statuses) mais recente ou para a build 9032 ou superior. Saiba como verificar a versão [nesta seção](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=pt-BR#getting-your-campaign-version). Para verificar se sua instância está hospedada no AWS, siga as etapas detalhadas [nesta página](../../faq.md#hosted-aws).

As instâncias do Campaign v8 hospedadas no Microsoft Azure também têm acesso a um subconjunto de recursos do Painel de Controle: [Lista de permissões de IP para acesso à instância](../../instances-settings/using/ip-allow-listing-instance-access.md), [Lista de permissões de IP para servidores SFTP](../../sftp/using/ip-range-allow-listing.md) e [Gerenciamento de certificados SSL gerenciado pelo cliente](../../subdomains-certificates/using/renewing-subdomain-certificate.md).

>[!IMPORTANT]
>
>Por padrão, o Painel de controle do Campaign é acessível aos usuários administradores que pertencem ao Perfil de produto “Administradores”. De acordo com a configuração da sua organização, o Perfil de produto pode ter um nome diferente (“admin”, “admins”, “administrador de aprovação” etc.). **Qualquer Perfil de produto que contenha a palavra “admin” no nome concederá acesso automaticamente ao Painel de controle**. Analise cuidadosamente o nome do seu Perfil de produto para garantir que somente usuários autorizados tenham acesso ao Painel de controle do Campaign. [Saiba como gerenciar permissões para acessar o Painel de controle](../../discover/using/managing-permissions.md).

## Acesso a partir da Experience Cloud Platform {#access-experience-cloud-platform}

Para acessar o painel de controle a partir da Adobe Experience Cloud Platform, siga as etapas abaixo.

1. Navegue até a [página inicial da Experience Cloud](https://experiencecloud.adobe.com/){target="_blank"}.

1. Clique no link dedicado, na seção **Acesso rápido**.

   ![](assets/do-not-localize/quickaccess.png)

O Painel de controle também pode ser acessado a partir do **seletor de soluções** da Experience Cloud Platform:

1. Na [página inicial da Adobe Experience Cloud](https://experiencecloud.adobe.com/){target="_blank"}, selecione **Campanha** na seção **Acesso rápido** ou no menu superior à direita.

   ![](assets/do-not-localize/control_panel_access1.png)

1. A lista das instâncias do Campaign será exibida. Clique no cartão **Painel de controle** para abri-lo.

   ![](assets/do-not-localize/control_panel_access2.png)

## Acesso a partir do produto {#access-product}

>[!NOTE]
>
>O acesso a partir do produto está disponível apenas no [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/campaign-standard-home.html?lang=pt-BR){target="_blank"}.

1. Abra o produto do Campaign Standard.

1. Selecione o menu **[!UICONTROL Administração]** no painel **Navegação**.

   ![](assets/control_panel_access3.png)

1. Clique no ícone **[!UICONTROL Painel de controle]**.

   ![](assets/control_panel_access4.png)
