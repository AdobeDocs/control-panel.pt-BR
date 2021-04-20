---
product: campaign
solution: Campaign
title: Gerenciamento de chaves
description: Saiba como gerenciar chaves para conexão com servidores SFTP
feature: Control Panel
role: Architect
level: Experienced
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 94%

---


# Gerenciamento de chaves {#key-management}

>[!CONTEXTUALHELP]
>id="cp_key_management"
>title="Sobre o Gerenciamento de chaves"
>abstract="Nesta guia você pode gerenciar chaves públicas."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=166" text="Assista ao vídeo de demonstração"

A Adobe recomenda que todos os clientes estabeleçam conexão com os servidores SFTP usando um **par de chaves públicas e privadas**.

As etapas para gerar uma chave SSH pública e adicioná-la ao servidor SFTP são descritas abaixo, bem como recomendações relacionadas à autenticação.

Quando o acesso ao servidor estiver configurado, lembre-se de **adicionar os endereços IP que exigirão acesso ao servidor para a lista de permissões** para que você possa se conectar a ele. Para obter mais informações, consulte [esta seção](../../instances-settings/using/ip-allow-listing-instance-access.md).

>[!NOTE]
>
>Atualmente não é possível excluir uma chave pública SSH.

![](assets/do-not-localize/how-to-video.png) Descubra este recurso no vídeo usando o  [Campaign ](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/generate-ssh-key.html?lang=en#sftp-management) Classic ou o  [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/generate-ssh-key.html?lang=en#sftp-management)

## Práticas recomendadas {#best-practices}

**Sobre a chave pública SSH**

Use sempre a mesma autenticação para se conectar ao servidor e use um formato compatível para a chave.

**Integração da API com nome de usuário e senha**

Em casos muito raros, a autenticação com senha é ativada em alguns servidores SFTP. A Adobe recomenda usar a autenticação com chave, pois esse método é mais eficiente e seguro. Você pode solicitar a autenticação com chave entrando em contato com o Atendimento ao cliente.

>[!IMPORTANT]
>
>Se a senha expirar, mesmo se houver chaves instaladas no sistema, você não poderá fazer login em suas contas SFTP.

## Instalação da chave SSH {#installing-ssh-key}

>[!CONTEXTUALHELP]
>id="cp_sftp_publickey_add"
>title="Adicionar nova chave pública"
>abstract="Adicione uma nova chave pública para uma instância."

>[!IMPORTANT]
>
>As etapas abaixo são apenas um exemplo de criação de chave SSH. Siga as diretrizes da organização em relação às chaves SSH. O exemplo abaixo mostra como isso pode ser feito e serve como um ponto de referência útil para informar os requisitos à sua equipe ou grupo de rede interno.

1. Navegue até a guia **[!UICONTROL Key Management]** e clique no botão **[!UICONTROL Add new public key]**.

   ![](assets/key0.png)

1. Na caixa de diálogo que é exibida, selecione o nome de usuário para o qual deseja criar a chave pública e o servidor para o qual deseja ativar a chave.

   >[!NOTE]
   >
   >A interface verificará se um determinado nome de usuário está ativo em uma certa instância e dará a você a opção de ativar a chave em uma ou várias instâncias.
   >
   >Uma ou mais chaves SSH públicas podem ser adicionadas para cada usuário.

   ![](assets/key1.png)

1. Copie e cole a chave SSH pública. Para gerar uma chave pública, siga as etapas abaixo correspondentes ao seu sistema operacional:

   >[!NOTE]
   >
   >O tamanho da chave pública SSH deve ser de **2048 bits**.

   **Linux e Mac:**

   Use o Terminal para gerar um par de chaves públicas e privadas:
   1. Digite este comando: `ssh-keygen -m pem -t rsa -b 2048 -C "your_email@example.com"`.
   1. Quando solicitado, forneça um nome para a chave. Se o diretório .ssh não existir, o sistema criará um para você.
   1. Digite, e em seguida insira novamente, uma senha quando solicitado. Esse campo também pode ser deixado em branco.
   1. Um par de chaves &quot;name&quot; e &quot;name.pub&quot; é criado pelo sistema. Procure o arquivo &quot;name.pub&quot; e abra-o. Ele deve ter uma sequência alfanumérica terminando com o endereço de email especificado.

   **Windows:**

   Talvez seja necessário instalar uma ferramenta de terceiros que ajudará você a gerar um par de chaves privadas/públicas no mesmo formato &quot;name.pub&quot;.

1. Abra o arquivo .pub e copie e cole a sequência inteira começando por &quot;ssh...&quot; no Painel de controle do Campaign.

   ![](assets/publickey.png)

1. Clique no botão **[!UICONTROL Save]** para criar a chave. O Painel de controle do Campaign salva a chave pública e sua impressão digital associada, criptografada com o formato SHA256.

Você pode utilizar a impressão digital como um equivalente às chaves privadas salvas no computador com as chaves públicas correspondentes salvas no Painel de controle do Campaign.

![](assets/fingerprint_compare.png)

O botão &quot;**...**&quot; permite excluir uma chave existente ou copiar sua impressão digital associada na área de transferência.

![](assets/key_options.png)
