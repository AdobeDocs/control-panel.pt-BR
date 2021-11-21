---
product: campaign
solution: Campaign
title: Fazer logon no servidor SFTP
description: Saiba como fazer logon no servidor SFTP
feature: Control Panel
role: Architect
level: Experienced
exl-id: 713f23bf-fa95-4b8a-b3ec-ca06a4592aa3
source-git-commit: 4fc34b07b497c743e2ca6c182e68d6ea5c180ac9
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 6%

---

# Fazer logon no servidor SFTP {#logging-into-sft-server}

As etapas abaixo detalham como conectar o servidor SFTP por meio do aplicativo cliente SFTP.

![](assets/do-not-localize/how-to-video.png)[ Descubra este recurso no vídeo](https://video.tv.adobe.com/v/27263?quality=12)

Antes de fazer logon no servidor, verifique se:

* Seu servidor SFTP é **hospedado pelo Adobe**.
* Seu **nome de usuário** foi configurado para o servidor. Você pode verificar essas informações diretamente no Painel de controle do Campaign, na **Gerenciamento de chaves** no cartão SFTP.
* Você tem um **par de chaves privadas e públicas** para fazer logon no servidor SFTP. Consulte [esta seção](../../sftp/using/key-management.md) para obter mais informações sobre como adicionar a chave SSH.
* Seu **o endereço IP público foi adicionado à lista de permissões** no servidor SFTP. Caso contrário, consulte [esta seção](../../sftp/using/ip-range-allow-listing.md) para obter mais informações sobre como adicionar o intervalo IP à lista de permissões.
* Você tem acesso a um **Software cliente SFTP**. Você pode consultar seu departamento de TI para obter o aplicativo cliente SFTP que eles recomendam usar ou pesquisar um na Internet, se isso for permitido pelas políticas de sua empresa.

Para se conectar ao servidor SFTP, siga estas etapas:

1. Inicie o Painel de controle e selecione o **[!UICONTROL Key Management]** na guia do **[!UICONTROL SFTP]** cartão.

   ![](assets/sftp_card.png)

1. Inicie seu aplicativo cliente SFTP e copie e cole o endereço do servidor do Painel de controle do Campaign, seguido por &quot;campaign.adobe.com&quot; e, em seguida, preencha seu nome de usuário.

   ![](assets/do-not-localize/connect1.png)

1. No **[!UICONTROL SSH Private Key]** selecione o arquivo de chave privada armazenado em seu computador. Corresponde a um arquivo de texto que tem o mesmo nome de sua chave pública, sem a extensão &quot;.pub&quot; (por exemplo, &quot;ativar&quot;).

   ![](assets/do-not-localize/connect2.png)

   O **[!UICONTROL Password]** é automaticamente preenchido com a chave privada do arquivo.

   ![](assets/do-not-localize/connect3.png)

   É possível verificar se a chave que você está tentando usar é salva no Painel de controle do Campaign, comparando a impressão digital da chave privada ou pública com a impressão digital das chaves que aparecem na guia Gerenciamento de chaves do cartão SFTP.

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >Se você estiver usando um computador Mac, poderá visualizar a impressão digital da chave privada armazenada em seu computador executando este comando:
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. Depois que todas as informações forem preenchidas, clique em **[!UICONTROL Connect]** para fazer logon no servidor SFTP.

   ![](assets/do-not-localize/sftpconnected.png)
