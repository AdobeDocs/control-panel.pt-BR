---
title: Detalhes da instância
description: Saiba como monitorar os detalhes da instância no Painel de controle do Campaign
translation-type: tm+mt
source-git-commit: 35723590195ef54df42d1d1df5b37490787f8836
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Detalhes da instância {#instance-details}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_instancedetails"
>title="Sobre detalhes da instância"
>abstract="Visualize os detalhes das instâncias do Adobe Campaign: tipos, nomes, informações de criação e possíveis recomendações de atualização."
>additional-url="https://docs.adobe.com/content/help/pt-BR/campaign-classic/using/release-notes/latest-release.html" text="Notas de versão do Campaign Classic"
>additional-url="https://docs.adobe.com/content/help/pt-BR/campaign-standard/using/release-notes/release-notes.html" text="Notas de versão do Campaign Standard"

>[!IMPORTANT]
>
>Esse recurso está disponível apenas para instâncias do Campaign Classic.

## Sobre detalhes da instância {#about-instance-details}

A arquitetura de instâncias do Adobe Campaign Classic pode conter vários servidores para permitir a flexibilidade das atividades de marketing. Por exemplo, você pode ter servidores de Marketing, Tempo real (ou Centro de mensagens) e Mid Sourcing para dar suporte à sua instância.

A funcionalidade Detalhes da instância permite a visualização de uma arquitetura simples da instância. Além das informações do servidor, ela também permite saber se a build da instância está ou não atualizada, além de recomendar atualizações quando necessário.

>[!NOTE]
>
>Recomendamos atualizar as instâncias pelo menos uma vez por ano para evitar a degradação do desempenho e aproveitar os recursos e as correções mais recentes que o Adobe Campaign Classic tem a oferecer.

**Tópicos relacionados:**

* [Atualização de uma build](https://helpx.adobe.com/br/campaign/kb/acc-build-upgrade.html)
* [Atualização do Adobe Campaign](https://docs.campaign.adobe.com/doc/AC/en/PRO_Updating_Adobe_Campaign_Introduction.html)

## Recuperar informações sobre instâncias {#retrieving-information-about-instances}

Para obter informações sobre os servidores conectados às suas instâncias, siga estas etapas:

1. Abra o cartão **[!UICONTROL Instances Settings]** para acessar a guia **[!UICONTROL Instance Details]**.

   >[!NOTE]
   >
   >Se o cartão Configurações de instância não estiver visível na página inicial do Painel de controle, isso significa que a ID de empresa do IMS não está associada a nenhuma instância do Adobe Campaign Classic

1. Selecione no painel esquerdo a instância desejada do Campaign Classic.

   >[!NOTE]
   >
   >Todas as instâncias do Campaign são exibidas na lista do painel esquerdo. Como o recurso Detalhes da instância é dedicado somente às instâncias do Campaign Classic, a mensagem &quot;Instância não aplicável&quot; é exibida ao selecionar uma instância do Campaign Standard.

1. Os servidores conectados à instância são exibidos.

   ![](assets/instance_details.png)

As informações disponíveis são:

* **[!UICONTROL Type]**: o tipo de servidor. Os valores possíveis são MKT (Marketing), MID (Mid sourcing) e RT (Centro de mensagens/Mensagens em tempo real).
* **[!UICONTROL Name]**: o nome do servidor.
* **[!UICONTROL Build:]** a versão da build instalada no servidor.
* **[!UICONTROL Upgrade info]**: esta coluna informa se alguma atualização é necessária para o servidor.
   * Verde: o servidor está atualizado, nenhuma atualização é necessária.
   * Amarelo: você deve pensar em atualizar. Faltam os recursos e as correções mais recentes.
   * Vermelho: atualize assim que possível. Faltam novos recursos e o desempenho do servidor pode não ser o ideal.

Se um dos seus servidores precisar ser atualizado, consulte [esta documentação](https://helpx.adobe.com/br/campaign/kb/acc-build-upgrade.html) para obter mais detalhes sobre como proceder.

## Perguntas comuns {#common-questions}

**Não vejo o servidor MID na arquitetura da minha instância. Isso significa que minhas instâncias não estão funcionando corretamente? Preciso da instância de RT para algo que não posso fazer hoje?**

Sua própria instância pode parecer muito diferente, e pode não ter todos os tipos de servidores, ou pode ter vários do mesmo servidor. Não ter um ou outro tipo de servidor não significa que você não possa enviar uma mensagem em tempo real ou executar outros tipos de atividades. Você pode solicitar capacidade adicional do servidor; taxas adicionais serão aplicadas.

Entre em contato com o Atendimento ao cliente se você achar que alguns servidores não estão sendo exibidos na página &quot;Detalhes da instância&quot;. Anote o URL da instância específica em sua mensagem.
