---
product: campaign
solution: Campaign
title: Logon no servidor SFTP
description: Saiba como fazer logon no seu servidor SFTP
feature: Control Panel, SFTP Management
role: Admin
level: Experienced
exl-id: 713f23bf-fa95-4b8a-b3ec-ca06a4592aa3
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '356'
ht-degree: 100%

---

# Logon no servidor SFTP {#logging-into-sft-server}

As etapas abaixo detalham como se conectar ao seu servidor SFTP por meio do aplicativo do cliente SFTP.

![](assets/do-not-localize/how-to-video.png) Conheça este recurso no [vídeo](https://video.tv.adobe.com/v/27263?quality=12)

Antes de fazer logon no servidor, certifique-se de que:

* O seu servidor SFTP está **hospedado pela Adobe**.
* Seu **nome de usuário** foi configurado para o servidor. É possível verificar essas informações diretamente no painel de controle, na guia **Gerenciamento de chaves** do cartão SFTP.
* Você conta com um **par de chaves privada e pública** para fazer logon no servidor SFTP. Consulte [esta seção](../../sftp/using/key-management.md) para mais informações sobre como adicionar a chave SSH.
* O seu **endereço IP público foi adicionado à lista de permissões** no servidor SFTP. Caso contrário, consulte [esta seção](../../sftp/using/ip-range-allow-listing.md) para mais informações sobre como adicionar o seu intervalo de IP à lista de permissões.
* Você tem acesso a um **software do cliente SFTP**. Você pode consultar o departamento de TI para obter o aplicativo do cliente SFTP recomendado ou procurar um aplicativo na internet, se isso for permitido pelas políticas da sua empresa.

Para conectar-se ao seu servidor SFTP, siga estas etapas:

1. Abra o Painel de controle e selecione a guia **[!UICONTROL Gerenciamento de chaves]** no cartão **[!UICONTROL SFTP]**.

   ![](assets/sftp_card.png)

1. Abra o aplicativo do cliente SFTP e, em seguida, copie e cole o endereço do servidor do Painel de controle, seguido de “campaign.adobe.com”, e preencha com o seu nome de usuário.

   ![](assets/do-not-localize/connect1.png)

1. No campo **[!UICONTROL Chave privada SSH]**, selecione o arquivo de chave privada armazenado no computador. Ele corresponde a um arquivo de texto que tem o mesmo nome que a sua chave pública, sem a extensão “.pub” (por exemplo, “habilitar”).

   ![](assets/do-not-localize/connect2.png)

   O campo **[!UICONTROL Senha]** é preenchido automaticamente com a chave privada do arquivo.

   ![](assets/do-not-localize/connect3.png)

   É possível verificar se a chave que está tentando usar está salva no Painel de controle, comparando a impressão digital da chave privada ou pública com a impressão digital das chaves que aparecem na guia Gerenciamento de chaves do cartão SFTP.

   ![](assets/fingerprint_compare.png)

   >[!NOTE]
   >
   >Se estiver usando um computador Mac, você poderá exibir a impressão digital da chave privada armazenada no computador por meio deste comando:
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. Depois que todas as informações forem preenchidas, clique em **[!UICONTROL Conectar]** para fazer logon no servidor SFTP.

   ![](assets/do-not-localize/sftpconnected.png)
