---
title: Permissões de URL
description: Saiba como gerenciar permissões de URL no Painel de controle
translation-type: tm+mt
source-git-commit: a2c19296894ff893987290cb287dc7002ab999e5

---


# Permissões de URL {#url-permissions}

>[!CONTEXTUALHELP]
>id=&quot;cp_instancesets_urlpermissions&quot;
>title=&quot;Sobre permissões de URL&quot;
>abstract=&quot;Gerencie os URLs aos quais as instâncias de Adobe Campaign podem se conectar.&quot;
>additional-url=&quot;https://images-tv.adobe.com/mpcv3/91206a19-d9af-4b6a-8197-0d2810a78941_1563488165.1920x1080at3000_h264.mp4&quot; text=&quot;Assista ao vídeo de demonstração&quot;

>[!IMPORTANT]
>
>Esse recurso está disponível apenas para instâncias de Campaign Classic.

## Sobre permissões de URL {#about-url-permissions}

A lista padrão de URLs que podem ser chamados por códigos JavaScript (workflows etc.) pelas instâncias de Campaign Classic é limitado. Esses são URLs que permitem que suas instâncias funcionem corretamente.

Por padrão, as instâncias não têm permissão para se conectar a URLs externos. O Painel de controle permite que você adicione URLs externos à lista de URLs autorizados, para que sua instância possa se conectar a eles. Isso permite que você conecte as instâncias de Campanha a sistemas externos, como, por exemplo, servidores SFTP ou sites, para habilitar a transferência de arquivos e/ou dados.

Depois que um URL é adicionado, ele é referenciado no arquivo de configuração da instância (serverConf.xml).

**Tópicos relacionados:**

* [Configuração do servidor de Campanha](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html)
* [Proteção de conexão de saída](https://docs.campaign.adobe.com/doc/AC/en/INS_Additional_configurations_Configuring_Campaign_server.html#Outgoing_connection_protection)
* [Adicionar permissões de URL (vídeo tutorial)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/adding-url-permissions.html)

## Práticas recomendadas {#best-practices}

* Não conecte sua instância de Campanha a sites/servidores aos quais você não pretende se conectar.
* Exclua URLs com os quais você não está mais trabalhando. No entanto, lembre-se de que, se outra seção da sua empresa ainda estiver se conectando ao URL excluído, ninguém poderá usá-lo novamente.
* O Painel de controle oferece suporte aos protocolos **http**, **https** e **sftp** . A inserção de URLs ou protocolos inválidos resultará em erros.

## Gerenciamento de permissões de URL {#managing-url-permissions}

>[!CONTEXTUALHELP]
>id=&quot;cp_instancesets_url_add&quot;
>title=&quot;Adicionar novo URL&quot;
>abstract=&quot;Adicione URLs para permitir conexões com sua instância de Campanha.&quot;

Para adicionar um URL ao qual sua instância pode se conectar, siga estas etapas:

1. Abra o **[!UICONTROL Instances Settings]** cartão para acessar a **[!UICONTROL URL Permissions]** guia.

   >[!NOTE]
   >
   >Se o cartão Configurações da instância não estiver visível na página inicial do Painel de controle, isso significa que a ID ORG IMS não está associada a nenhuma instância do Adobe Campaign Classic
   >
   >A guia de permissões <b><span class="uicontrol">de</span></b> URL lista todos os URLs externos aos quais sua instância pode se conectar. Essa lista não inclui URLs necessários para que a Campanha funcione (por exemplo, conexões entre peças de infraestrutura).

1. Selecione no painel esquerdo a instância desejada e clique no **[!UICONTROL Add new URL]** botão.

   ![](assets/add_url1.png)

   >[!NOTE]
   >
   >Todas as ocorrências de Campanha são exibidas na lista do painel esquerdo.
   >
   >Como o gerenciamento de permissões de URL é dedicado apenas a instâncias Campaign Classic, a mensagem &quot;Instância não aplicável&quot; é exibida se você selecionar uma instância Campaign Standard.

1. Digite o URL a ser autorizado, com seu protocolo associado (http, https ou sftp).

   >[!NOTE]
   >
   >É possível autorizar várias instâncias para se conectar ao URL. Para fazer isso, adicione-os diretamente do campo Instâncias digitando sua primeira letra.

   ![](assets/add_url2.png)

1. O URL é adicionado à lista, agora você pode se conectar a ele.

   >[!NOTE]
   >
   >O &quot;/.*&quot; são adicionados automaticamente ao final do URL inserido depois de ele ter sido validado, para abranger todas as subpáginas da página inserida.

   ![](assets/add_url_listnew.png)

Você pode excluir um URL a qualquer momento selecionando-o e clicando no **[!UICONTROL Delete URL]** botão.

Lembre-se de que, se você excluir um URL, sua instância não poderá chamá-lo novamente.

## Perguntas comuns {#common-questions}

**Eu adicionei um novo URL, mas minha instância ainda não consegue se conectar a esse URL. Por que isso?**

Em alguns casos, os URLs que você tenta conectar exigem a lista de permissões, a entrada de senha ou outra forma de autenticação. O Painel de controle não gerencia autenticação adicional.
