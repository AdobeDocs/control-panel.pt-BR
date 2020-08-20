---
title: Gerenciamento de chaves GPG
description: Saiba como gerenciar chaves GPG para criptografar e descriptografar dados no Adobe Campaign.
translation-type: tm+mt
source-git-commit: 1fe1bf8cd90218c54076988780b53819e9fad304
workflow-type: tm+mt
source-wordcount: '1112'
ht-degree: 12%

---


# Gerenciamento de chaves GPG {#gpg-keys-management}

## Sobre criptografia GPG {#about-gpg-encryption}

A criptografia GPG permite proteger seus dados usando um sistema de pares de chaves públicas-privadas que seguem a especificação do [OpenPGP](https://www.openpgp.org/about/standard/) .

Depois de implementados, você pode ter os dados de entrada descriptografados e os dados de saída criptografados antes da transferência, para garantir que eles não sejam acessados por ninguém sem um par de chaves correspondente válido.

Para implementar a criptografia GPG com o Campaign, as chaves GPG devem ser instaladas e/ou geradas em uma instância de marketing por um usuário administrador no Painel de controle do Campaign.

Depois será possível:

* **Criptografar dados** enviados: A Adobe Campaign envia os dados após criptografá-los com a chave pública instalada.

* **Descriptografar dados** recebidos: A Adobe Campaign recebe dados que foram criptografados de um sistema externo usando uma chave pública baixada do Painel de controle do Campaign. A Adobe Campaign descriptografa os dados usando uma chave privada gerada a partir do Painel de controle do Campaign.

**Tópicos relacionados:**

* [Vídeos de tutoriais do Campaign Standard](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/administrating/control-panel/gpg-key-management/gpg-key-management-overview.html)
* [Vídeos de tutoriais do Campaign Classic](https://docs.adobe.com/content/help/en/campaign-classic-learn/tutorials/administrating/control-panel-acc/gpg-key-management/gpg-key-management-overview.html)

## Criptografar dados {#encrypting-data}

O Painel de controle do Campaign permite criptografar dados provenientes da instância do Adobe Campaign.

Para fazer isso, você precisa gerar um par de chaves GPG a partir de uma ferramenta de criptografia PGP e instalar a chave pública no Painel de controle do Campaign. Você poderá criptografar os dados antes de enviá-los da sua instância. Para fazer isso, siga estes passos:

1. Gere um par de chaves públicas/privadas usando uma ferramenta de criptografia PGP após a especificação [](https://www.openpgp.org/about/standard/)OpenPGP. Para fazer isso, instale um utilitário GPG ou software GNuGP.

   >[!NOTE]
   >
   >O software livre de código aberto para gerar chaves está disponível. No entanto, siga as diretrizes de sua organização e use o utilitário GPG recomendado por sua organização de TI/Segurança.

1. Depois que o utilitário estiver instalado, execute o comando abaixo, no Mac Terminal ou no comando do Windows.

   `gpg --full-generate-key`

1. Quando solicitado, especifique os parâmetros desejados para sua chave. Os parâmetros obrigatórios são:

   * **tipo** de chave: RSA
   * **comprimento** da chave: 1024 - 4096 bits
   * **nome** real e endereço **de** email: Permite rastrear quem criou o par de chaves. Insira um nome e endereço de email vinculados à sua organização ou departamento.
   * **comentário**: adicionar um rótulo ao campo de comentário ajudará você a identificar facilmente a chave a ser usada para criptografar seus dados.
   * **expiração**: Data ou &quot;0&quot; para nenhuma data de expiração.
   * **senha**

   ![](assets/do-not-localize/gpg_command.png)

1. Depois de confirmado, o script gerará uma chave com sua impressão digital associada, que poderá ser exportada para um arquivo ou colada diretamente no Painel de controle do Campaign. Para exportar o arquivo, execute esse comando seguido da impressão digital da chave que você gerou.

   `gpg -a --export <fingerprint>`

1. Para instalar a chave pública no Painel de controle do Campaign, abra o **[!UICONTROL Instance settings]** cartão e selecione a guia **[!UICONTROL GPG keys]** e a instância desejada.

1. Clique no botão **[!UICONTROL Install Key]**.

   ![](assets/gpg_install_button.png)

1. Cole a chave pública gerada pela ferramenta de criptografia PGP. Também é possível arrastar e soltar diretamente o arquivo de chave pública que você exportou.

   >[!NOTE]
   >
   >A chave pública deve estar no formato OpenPGP.

   ![](assets/gpg_install_paste.png)

1. Clique no botão **[!UICONTROL Install Key]**.

Quando a chave pública estiver instalada, ela será exibida na lista. Você pode usar o **...** para baixá-lo ou copiar sua impressão digital.

![](assets/gpg_install_download.png)

A chave está disponível para uso em workflows Adobe Campaign. Você pode usá-lo para criptografar dados ao usar atividades de extração de dados.

Para obter mais informações, consulte a documentação da Adobe Campaign:

**Campaign Classic:**

* [Compactação ou criptografia de um arquivo](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/how-to-use-workflow-data.html#zipping-or-encrypting-a-file)
* [Caso de uso: criptografar e exportar dados usando uma chave instalada no Painel de controle do Campaign](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/how-to-use-workflow-data.html#use-case-gpg-encrypt)

**Campaign Standard:**

* [Gerenciamento de dados criptografados](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [Caso de uso: criptografar e exportar dados usando uma chave instalada no Painel de controle do Campaign](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-encrypt)

## Descriptografar dados {#decrypting-data}

O Painel de controle do Campaign permite descriptografar dados externos que entram em suas instâncias do Adobe Campaign.

Para fazer isso, você precisa gerar um par de chaves GPG diretamente do Painel de controle do Campaign.

* The **public key** will be shared with the external system, which will use it to encrypt the data to send to Campaign.
* The **private key** will be used by Campaign to decrypt the incoming encrypted data.

Para gerar um par de chaves no Painel de controle do Campaign, siga estas etapas:

1. Abra o **[!UICONTROL Instance settings]** cartão e selecione a guia **[!UICONTROL GPG keys]** e a instância do Adobe Campaign desejada.

1. Clique no botão **[!UICONTROL Generate Key]**.

   ![](assets/gpg_generate.png)

1. Especifique o nome da chave e clique em **[!UICONTROL Generate Key]**. Este nome o ajudará a identificar a chave a ser usada para descriptografia em Workflows da campanha

   ![](assets/gpg_generate_name.png)

Depois que o par de chaves é gerado, a chave pública é exibida na lista. Observe que os pares de chaves de descriptografia são gerados sem data de expiração.

Você pode usar o **...** para baixar a chave pública ou copiar sua impressão digital.

![](assets/gpg_generate_list.png)

A chave pública está disponível para ser compartilhada com qualquer sistema externo. A Adobe Campaign poderá usar a chave privada nas atividades de carregamento de dados para descriptografar dados que foram criptografados com a chave pública.

Para obter mais informações, consulte a documentação da Adobe Campaign:

**Campaign Classic:**

* [Descompactação ou descriptografia de um arquivo antes do processamento](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/importing-data.html#unzipping-or-decrypting-a-file-before-processing)
* [Caso de uso: importação de dados criptografados usando uma chave gerada pelo Painel de controle do Campaign](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/importing-data.html#use-case-gpg-decrypt)

**Campaign Standard:**

* [Gerenciamento de dados criptografados](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [Caso de uso: importação de dados criptografados usando uma chave gerada pelo Painel de controle do Campaign](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-decrypt)

## Monitorando teclas GPG

Para acessar chaves GPG instaladas e geradas para suas instâncias, abra o **[!UICONTROL Instance settings]** cartão e selecione a **[!UICONTROL GPG keys]** guia.

![](assets/gpg_list.png)

A lista exibe todas as chaves GPG de criptografia e descriptografia que foram instaladas e geradas para suas instâncias com informações detalhadas sobre cada chave:

* **[!UICONTROL Name]**: O nome que foi definido ao instalar ou gerar a chave.
* **[!UICONTROL Use case]**: Esta coluna especifica o caso de uso da chave:

   ![](assets/gpg_icon_encrypt.png): A chave foi instalada para criptografia de dados.

   ![](assets/gpg_icon_decrypt.png): A chave foi gerada para permitir a descriptografia de dados.

* **[!UICONTROL Fingerprint]**: a impressão digital da chave.
* **[!UICONTROL Expires]**: A data de expiração da chave. Observe que o Painel de controle do Campaign fornecerá indicações visuais à medida que a chave se aproxima da data de expiração:

   * Urgente (vermelho) é mostrado 30 dias antes.
   * A advertência (amarela) é mostrada 60 dias antes.
   * Um banner vermelho &quot;Expirado&quot; será exibido assim que uma tecla expirar.

   >[!NOTE]
   >
   >Observe que nenhuma notificação por email será enviada pelo Painel de controle do Campaign.

Como prática recomendada, recomendamos que você remova qualquer chave que não precise mais. To do this, click the **...** button then select **[!UICONTROL Delete Key].**.

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>Antes de remover uma chave, verifique se ela não é usada em nenhum fluxo de trabalho do Adobe Campaign para evitar que ela falhe.
