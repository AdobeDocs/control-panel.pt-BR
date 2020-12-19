---
product: campaign
solution: Campaign
title: Fazer logon no servidor SFTP
description: Saiba como fazer logon no servidor SFTP
translation-type: tm+mt
source-git-commit: 54d3239a566491c854e5d46c297e72afeff83792
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 6%

---


# Fazer logon no servidor SFTP {#logging-into-sft-server}

As etapas abaixo detalham como conectar seu servidor SFTP por meio do aplicativo cliente SFTP.

![](assets/do-not-localize/how-to-video.png)[ Descubra este recurso no vídeo](https://video.tv.adobe.com/v/27263?quality=12&captions=por_br)

Antes de fazer logon no servidor, verifique se:

* Seu servidor SFTP é **hospedado por Adobe**.
* Seu **nome de usuário** foi configurado para o servidor. Você pode verificar essas informações diretamente no Painel de controle do Campaign, na guia **Gerenciamento de chaves** do Cartão SFTP.
* Você tem um **par de chaves privadas e públicas** para fazer logon no servidor SFTP. Consulte [esta seção](../../sftp/using/key-management.md) para obter mais informações sobre como adicionar a chave SSH.
* Seu **endereço IP público foi adicionado à lista de permissões** no servidor SFTP. Caso contrário, consulte [esta seção](../../sftp/using/ip-range-allow-listing.md) para obter mais informações sobre como adicionar seu intervalo IP à lista de permissões.
* Você tem acesso a um **software cliente SFTP**. Você pode consultar seu departamento de TI para obter o aplicativo cliente SFTP que eles recomendam usar ou procurar um na Internet se isso for permitido pelas políticas de empresa.

Para se conectar ao servidor SFTP, siga estas etapas:

1. Inicie o Painel de controle do Campaign e selecione a guia **[!UICONTROL Key Management]** no cartão **[!UICONTROL SFTP]**.

   ![](assets/sftp_card.png)

1. Inicie seu aplicativo cliente SFTP, copie e cole o endereço do servidor do Painel de controle do Campaign, seguido por &quot;campanha.adobe.com&quot; e preencha seu nome de usuário.

   ![](assets/do-not-localize/connect1.png)

1. No campo **[!UICONTROL SSH Private Key]**, selecione o arquivo de chave privada armazenado em seu computador. Corresponde a um arquivo de texto que tem o mesmo nome da sua chave pública, sem a extensão &quot;.pub&quot; (por exemplo, &quot;enable&quot;).

   ![](assets/do-not-localize/connect2.png)

   O campo **[!UICONTROL Password]** é automaticamente preenchido com a chave privada do arquivo.

   ![](assets/do-not-localize/connect3.png)

   Você pode verificar se a chave que está tentando usar está salva no Painel de controle do Campaign comparando a impressão digital da chave privada ou pública com a impressão digital das chaves que aparecem na guia Gerenciamento de chaves da placa SFTP.

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >Se estiver usando um computador Mac, você pode visualização a impressão digital da chave privada armazenada em seu computador executando este comando:
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. Depois que todas as informações forem preenchidas, clique em **[!UICONTROL Connect]** para fazer logon no servidor SFTP.

   ![](assets/do-not-localize/sftpconnected.png)
