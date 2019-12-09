---
title: Detalhes da instância
description: Saiba como monitorar os detalhes da sua instância no Painel de controle
translation-type: tm+mt
source-git-commit: 8ee999b89af88a1a59956838d5722ce8fc6b3955

---


# Detalhes da instância {#instance-details}

>[!CAUTION]
>
>Esse recurso está disponível somente para instâncias do Campaign Classic.

## Sobre detalhes da instância {#about-instance-details}

Sua arquitetura de instância do Adobe Campaign Classic pode conter vários servidores para permitir a flexibilidade das atividades de marketing. Por exemplo, você pode ter servidores de Marketing, Tempo real (ou Centro de mensagens) e Sourcing para dar suporte à sua instância.

A funcionalidade Detalhes da instância permite que você visualize uma arquitetura simples da sua instância. Além das informações do servidor, também permite saber se a compilação da instância está ou não atualizada, além de recomendar atualizações quando necessário.

>[!NOTE]
>
>Recomendamos que suas instâncias sejam atualizadas pelo menos uma vez por ano para evitar a degradação do desempenho e aproveitem os recursos e as correções mais recentes que o Adobe Campaign Classic tem para oferecer.

**Tópicos relacionados:**

* [Execução de uma atualização de compilação](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html)
* [Atualização do Adobe Campaign](https://docs.campaign.adobe.com/doc/AC/en/PRO_Updating_Adobe_Campaign_Introduction.html)

## Recuperando informações sobre suas instâncias {#retrieving-information-about-instances}

Para obter informações sobre os servidores conectados às suas instâncias, siga estas etapas:

1. Abra o **[!UICONTROL Instances Settings]** cartão para acessar a **[!UICONTROL Instance Details]** guia.

   >[!NOTE]
   >
   >Se o cartão Configurações da instância não estiver visível na página inicial do Painel de controle, isso significa que a ID ORG IMS não está associada a nenhuma instância do Adobe Campaign Classic

1. Selecione no painel esquerdo a instância desejada do Campaign Classic.

   >[!NOTE]
   >
   >Todas as instâncias da Campanha são exibidas na lista do painel esquerdo. Como o recurso Detalhes da instância é dedicado somente às instâncias do Campaign Classic, a mensagem "Instância não aplicável" é exibida se você selecionar uma instância do Campaign Standard.

1. Os servidores conectados à instância são exibidos.

   ![](assets/instance_details.png)

As informações disponíveis são:

* **[!UICONTROL Type]**: o tipo do servidor. Os valores possíveis são MKT (Marketing), MID (Meid sourcing) e RT (Message Center / Real-time messaging).
* **[!UICONTROL Name]**: o nome do servidor.
* **[!UICONTROL Build:]** a versão de build instalada no servidor.
* **[!UICONTROL Upgrade info]**: esta coluna informa se alguma atualização é necessária para o servidor.
   * Verde: seu servidor está atual, nenhuma atualização é necessária.
   * Amarelo: você deve considerar atualizar. Faltam os recursos e as correções mais recentes.
   * Vermelho: atualize assim que possível. Faltam novos recursos e o desempenho do servidor pode não ser o ideal.

Se um de seus servidores precisar ser atualizado, consulte [esta documentação](https://docs.campaign.adobe.com/doc/AC/getting_started/EN/buildUpgrade.html) para obter mais detalhes sobre como proceder.

## Perguntas comuns {#common-questions}

**Não vejo o servidor MID na arquitetura da minha instância, isso significa que minhas instâncias não estão funcionando corretamente? Preciso da instância do RT para algo que não posso fazer hoje?**

Sua própria instância pode parecer muito diferente, e pode não ter todos os tipos de servidores, ou pode ter vários do mesmo servidor. Não ter um tipo de servidor ou outro não significa que não é possível enviar uma mensagem em tempo real ou executar outros tipos de atividades. Você pode solicitar capacidade adicional do servidor, taxas adicionais serão aplicadas.

Entre em contato com o Atendimento ao cliente se você achar que alguns servidores não estão sendo exibidos na página "Detalhes da instância". Certifique-se de anotar o URL da instância específica em sua mensagem.