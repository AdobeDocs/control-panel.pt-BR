---
title: Fazer logon no servidor SFTP
description: Saiba como fazer logon no servidor SFTP
translation-type: tm+mt
source-git-commit: 8ee999b89af88a1a59956838d5722ce8fc6b3955

---


# Fazer logon no servidor SFTP {#logging-into-sft-server}

As etapas abaixo detalham como conectar seu servidor SFTP por meio do aplicativo cliente SFTP.

Antes de fazer logon no servidor, verifique se:

* Seu servidor SFTP é **hospedado pela Adobe**.
* Seu **nome de usuário** foi configurado para o servidor. You can check this information directly in the Control Panel, in the **Key management** tab from the SFTP Card.
* Você tem um par **de chaves** privadas e públicas para fazer logon no servidor SFTP. Consulte [esta seção](../../sftp/using/key-management.md) para obter mais informações sobre como adicionar a chave SSH.
* Seu endereço IP **público foi incluído na lista de permissões** no servidor SFTP. Caso contrário, consulte [esta seção](../../sftp/using/ip-range-whitelisting.md) para obter mais informações sobre como adicionar o intervalo IP à lista de permissões.
* Você tem acesso a um software **cliente** SFTP. Você pode consultar seu departamento de TI para obter o aplicativo cliente SFTP que eles recomendam usar ou procurar um na Internet se isso for permitido pelas políticas da sua empresa.

Para se conectar ao servidor SFTP, siga estas etapas:

1. Launch the Control Panel, then select the **[!UICONTROL Key Management]** tab from the **[!UICONTROL SFTP]** card.

   ![](assets/fingerprintNEW2.png)

1. Inicie seu aplicativo cliente SFTP, copie e cole o endereço do servidor do Painel de controle, seguido por "campaign.adobe.com" e preencha seu nome de usuário.

   ![](assets/connect1.png)

1. No **[!UICONTROL SSH Private Key]** campo, selecione o arquivo de chave privada armazenado em seu computador. Corresponde a um arquivo de texto que tem o mesmo nome da sua chave pública, sem a extensão ".pub" (por exemplo, "enable").

   ![](assets/connect2.png)

   O **[!UICONTROL Password]** campo é preenchido automaticamente com a chave privada do arquivo.

   ![](assets/connect3.png)

   Você pode verificar se a chave que está tentando usar está salva no Painel de controle ao comparar a impressão digital da chave privada ou pública com a impressão digital das chaves que aparecem na guia Gerenciamento de chaves da placa SFTP.

   ![](assets/fingerprint3.png)

   >[!NOTE]
   >
   >Se você estiver usando um computador Mac, poderá exibir a impressão digital da chave privada armazenada no computador executando este comando:
   >
   >`ssh-keygen -lf <path of the privatekey>`

1. Depois que todas as informações forem preenchidas, clique em **[!UICONTROL Connect]** para fazer logon no servidor SFTP.

   ![](assets/sftpconnected.png)