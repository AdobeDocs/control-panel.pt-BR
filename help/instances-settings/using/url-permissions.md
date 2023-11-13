---
product: campaign
solution: Campaign
title: Permissões de URL
description: Saiba como gerenciar permissões de URL no Painel de controle
feature: Control Panel, Access Management
role: Admin
level: Intermediate
exl-id: a7df90da-a2ce-409f-9bc3-c7d4fa3024c8
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '612'
ht-degree: 100%

---

# Permissões de URL {#url-permissions}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_urlpermissions"
>title="Sobre permissões de URL"
>abstract="Gerencie os URLs aos quais as instâncias do Adobe Campaign podem se conectar."
>additional-url="https://images-tv.adobe.com/mpcv3/91206a19-d9af-4b6a-8197-0d2810a78941_1563488165.1920x1080at3000_h264.mp4" text="Assista ao vídeo de demonstração"

## Sobre permissões de URL {#about-url-permissions}

>[!IMPORTANT]
>
>Este recurso está disponível apenas para instâncias do Campaign v7/v8, a partir da build 8850. Se você estiver usando uma build com versão anterior, será necessário uma atualização para usar esse recurso.

A lista padrão de URLs que podem ser chamados por códigos JavaScript (workflows, etc.) pelas instâncias do Campaign é limitada. Esses são os URLs que permitem que as instâncias funcionem corretamente.

Por padrão, as instâncias não têm permissão para se conectar a URLs externos. O Painel de controle permite adicionar URLs externos à lista de URLs autorizados para que sua instância possa se conectar a eles. Dessa forma, você pode conectar as instâncias do Campaign a sistemas externos, como servidores ou sites SFTP para habilitar a transferência de arquivos e/ou dados.

Depois de adicionado, o URL é referenciado no arquivo de configuração da instância (serverConf.xml).

![](assets/do-not-localize/how-to-video.png) [Conheça este recurso no vídeo](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/adding-url-permissions.html?lang=pt-BR#instance-settings)

**Tópicos relacionados:**

* [Configuração do servidor do Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/additional-configurations/configuring-campaign-server.html?lang=pt-BR)
* [Proteção de conexão de saída](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/security-privacy/server-configuration.html?lang=pt-BR#outgoing-connection-protection)

## Práticas recomendadas {#best-practices}

* Não conecte a instância do Campaign a sites/servidores aos quais você não pretende se conectar.
* Exclua URLs com os quais você não está mais trabalhando. No entanto, lembre-se de que, se outra seção da sua empresa ainda estiver se conectando ao URL excluído, ninguém poderá usá-lo novamente.
* O Painel de controle oferece suporte aos protocolos **http**, **https** e **sftp**. A inserção de URLs ou protocolos inválidos resultará em erros.

## Gerenciamento de permissões de URL {#managing-url-permissions}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_url_add"
>title="Definição de URL"
>abstract="Adicione URLs para permitir conexões com sua instância do Campaign."

Para adicionar um URL ao qual sua instância pode se conectar, siga estas etapas:

1. Abra o cartão **[!UICONTROL Configurações de instâncias]** para acessar a guia **[!UICONTROL Permissões de URL]**.

   >[!NOTE]
   >
   >Se o cartão de configurações de instâncias não estiver visível na página inicial do Painel de controle, isso significa que a [ID da organização](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=pt-BR) não está associada a nenhuma instância do Adobe Campaign
   >
   >A guia de <b><span class="uicontrol">permissões de URL</span></b> lista todos os URLs externos aos quais sua instância pode se conectar. Essa lista não inclui URLs necessários para que o Campaign funcione (por exemplo, conexões entre peças de infraestrutura).

1. Selecione a instância desejada no painel esquerdo e clique no botão **[!UICONTROL Adicionar novo URL]**.

   ![](assets/add_url1.png)

   >[!NOTE]
   >
   >Todas as instâncias do Campaign são exibidas na lista do painel esquerdo.
   >
   >Como o gerenciamento de permissões de URL é dedicado apenas a instâncias do Campaign v7/v8, se você selecionar uma instância do Campaign Standard, a mensagem “Instância não aplicável” será exibida.

1. Digite o URL a ser autorizado com seu protocolo associado (http, https ou sftp).

   >[!NOTE]
   >
   >É possível autorizar várias instâncias para se conectar ao URL. Para fazer isso, adicione-os diretamente no campo Instâncias digitando sua primeira letra.

   ![](assets/add_url2.png)

1. O URL é adicionado à lista; agora você pode se conectar a ele.

   >[!NOTE]
   >
   >Os &quot;/.*&quot; caracteres são adicionados automaticamente ao final do URL inserido após a validação para abranger todas as subpáginas da página inserida.

   ![](assets/add_url_listnew.png)

Você pode excluir um URL a qualquer momento, selecionando-o e clicando no botão **[!UICONTROL Excluir URL]**.

Lembre-se de que se você excluir um URL, sua instância não poderá chamá-lo novamente.

## Perguntas comuns {#common-questions}

**Adicionei um novo URL, mas minha instância ainda não consegue se conectar a esse URL. Por que isso ocorre?**

Em alguns casos, os URLs que você tenta conectar exigem uma lista de permissão, uma senha ou outra forma de autenticação. O Painel de controle não gerencia autenticação adicional.
