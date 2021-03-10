---
product: campaign
solution: Campaign
title: Gerenciamento de chaves GPG
description: Saiba como gerenciar chaves GPG para criptografar e descriptografar dados no Adobe Campaign.
feature: 'Painel de controle do Campaign   '
role: Arquiteto
level: Experienciado
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 14%

---


# Gerenciamento de chaves GPG {#gpg-keys-management}

## Sobre a criptografia GPG {#about-gpg-encryption}

A criptografia GPG permite proteger seus dados usando um sistema de pares de chaves públicas-privadas que seguem a especificação [OpenPGP](https://www.openpgp.org/about/standard/).

Depois de implementados, é possível descriptografar os dados recebidos e os dados de saída criptografados antes da transferência, para garantir que eles não sejam acessados por ninguém sem um par de chaves correspondente válido.

Para implementar a criptografia GPG com o Campaign, as chaves GPG devem ser instaladas e/ou geradas em uma instância de marketing por um usuário administrador no Painel de controle do Campaign.

Depois será possível:

* **Criptografar dados** enviados: O Adobe Campaign envia dados após criptografá-los com a chave pública instalada.

* **Descriptografar dados** de entrada: O Adobe Campaign recebe dados que foram criptografados de um sistema externo usando uma chave pública baixada pelo Painel de controle do Campaign. O Adobe Campaign descriptografa os dados usando uma chave privada gerada pelo Painel de controle do Campaign.

## Criptografar dados {#encrypting-data}

O Painel de controle do Campaign permite criptografar dados provenientes da instância do Adobe Campaign.

Para fazer isso, você precisa gerar um par de chaves GPG de uma ferramenta de criptografia PGP e, em seguida, instalar a chave pública no Painel de controle do Campaign. É possível criptografar dados antes de enviá-los da instância. Para fazer isso, siga as etapas abaixo.

![](assets/do-not-localize/how-to-video.png)[ Descubra este recurso no vídeo](#video)

1. Gere um par de chaves públicas/privadas usando uma ferramenta de criptografia PGP seguindo a [especificação OpenPGP](https://www.openpgp.org/about/standard/). Para fazer isso, instale um utilitário GPG ou software GNuGP.

   >[!NOTE]
   >
   >O software livre de código aberto para gerar chaves está disponível. No entanto, siga as diretrizes de sua organização e use o utilitário GPG recomendado por sua organização de TI/segurança.

1. Depois que o utilitário estiver instalado, execute o comando abaixo, no Mac Terminal ou no comando do Windows.

   `gpg --full-generate-key`

1. Quando solicitado, especifique os parâmetros desejados para sua chave. Os parâmetros obrigatórios são:

   * **tipo** de chave: RSA
   * **comprimento** da chave: 1024 - 4096 bits
   * **nome real** e endereço de  **email**: Permite rastrear quem criou o par de chaves. Insira um nome e endereço de email vinculado à sua organização ou departamento.
   * **comentário**: adicionar um rótulo ao campo de comentário ajudará você a identificar facilmente a chave que será usada para criptografar seus dados.
   * **expiração**: Data ou &quot;0&quot; para nenhuma data de expiração.
   * **senha**

   ![](assets/do-not-localize/gpg_command.png)

1. Depois de confirmado, o script gerará uma chave com sua impressão digital associada, que poderá ser exportada para um arquivo ou colada diretamente no Painel de controle do Campaign. Para exportar o arquivo, execute este comando seguido da impressão digital da chave gerada.

   `gpg -a --export <fingerprint>`

1. Para instalar a chave pública no Painel de controle do Campaign, abra o cartão **[!UICONTROL Instance settings]** e selecione a guia **[!UICONTROL GPG keys]** e a instância desejada.

1. Clique no botão **[!UICONTROL Install Key]**.

   ![](assets/gpg_install_button.png)

1. Cole a chave pública gerada a partir da ferramenta de criptografia PGP. Você também pode arrastar e soltar diretamente o arquivo de chave pública que exportou.

   >[!NOTE]
   >
   >A chave pública deve estar no formato OpenPGP.

   ![](assets/gpg_install_paste.png)

1. Clique no botão **[!UICONTROL Install Key]**.

Quando a chave pública estiver instalada, ela será exibida na lista. Você pode usar o **...Botão** para baixá-lo ou copiar sua impressão digital.

![](assets/gpg_install_download.png)

A chave fica disponível para uso em workflows do Adobe Campaign. Você pode usá-los para criptografar dados ao usar atividades de extração de dados.

![](assets/do-not-localize/how-to-video.png)[ Descubra este recurso no vídeo](#video)

Para obter mais informações sobre esse tópico, consulte a documentação do Adobe Campaign:

**Campaign Classic:**

* [Compactação ou criptografia de um arquivo](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/how-to-use-workflow-data.html#zipping-or-encrypting-a-file)
* [Caso de uso: criptografar e exportar dados usando uma chave instalada no Painel de controle do Campaign](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/how-to-use-workflow-data.html#use-case-gpg-encrypt)

**Campaign Standard:**

* [Gerenciamento de dados criptografados](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [Caso de uso: criptografar e exportar dados usando uma chave instalada no Painel de controle do Campaign](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-encrypt)

## Descriptografar dados {#decrypting-data}

O Painel de controle do Campaign permite descriptografar dados externos que entram em suas instâncias do Adobe Campaign.

Para fazer isso, você precisa gerar um par de chaves GPG diretamente do Painel de controle do Campaign.

* A **chave pública** será compartilhada com o sistema externo, que a usará para criptografar os dados que serão enviados para o Campaign.
* A **chave privada** será usada pelo Campaign para descriptografar os dados criptografados recebidos.

![](assets/do-not-localize/how-to-video.png)[ Descubra este recurso no vídeo](#video)

Para gerar um par de chaves no Painel de controle do Campaign, siga estas etapas:

1. Abra o cartão **[!UICONTROL Instance settings]** e selecione a guia **[!UICONTROL GPG keys]** e a instância desejada do Adobe Campaign.

1. Clique no botão **[!UICONTROL Generate Key]**.

   ![](assets/gpg_generate.png)

1. Especifique o nome da chave e clique em **[!UICONTROL Generate Key]**. Esse nome ajudará você a identificar a chave a ser usada para descriptografia nos workflows do Campaign

   ![](assets/gpg_generate_name.png)

Depois que o par de chaves é gerado, a chave pública é exibida na lista. Observe que os pares de chaves de descriptografia são gerados sem data de expiração.

Você pode usar o **...Botão** para baixar a chave pública ou copiar sua impressão digital.

![](assets/gpg_generate_list.png)

A chave pública estará disponível para ser compartilhada com qualquer sistema externo. O Adobe Campaign poderá usar a chave privada nas atividades de carregamento de dados para descriptografar dados que foram criptografados com a chave pública.

Para obter mais informações, consulte a documentação da Adobe Campaign:

**Campaign Classic:**

* [Descompactação ou descriptografia de um arquivo antes do processamento](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/importing-data.html#unzipping-or-decrypting-a-file-before-processing)
* [Caso de uso: importação de dados criptografados usando uma chave gerada pelo Painel de controle do Campaign](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/general-operation/importing-data.html#use-case-gpg-decrypt)

**Campaign Standard:**

* [Gerenciamento de dados criptografados](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html)
* [Caso de uso: importação de dados criptografados usando uma chave gerada pelo Painel de controle do Campaign](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html#use-case-gpg-decrypt)

## Monitoramento de chaves GPG

Para acessar as chaves GPG instaladas e geradas para suas instâncias, abra o cartão **[!UICONTROL Instance settings]** e selecione a guia **[!UICONTROL GPG keys]**.

![](assets/gpg_list.png)

A lista exibe todas as chaves GPG de criptografia e descriptografia que foram instaladas e geradas para suas instâncias com informações detalhadas sobre cada chave:

* **[!UICONTROL Name]**: O nome que foi definido ao instalar ou gerar a chave.
* **[!UICONTROL Use case]**: Essa coluna especifica o caso de uso da chave:

   ![](assets/gpg_icon_encrypt.png): A chave foi instalada para criptografia de dados.

   ![](assets/gpg_icon_decrypt.png): A chave foi gerada para permitir a descriptografia de dados.

* **[!UICONTROL Fingerprint]**: a impressão digital da chave.
* **[!UICONTROL Expires]**: A data de expiração da chave. Observe que o Painel de controle do Campaign fornecerá indicações visuais à medida que a chave se aproximar da data de expiração:

   * Urgente (vermelho) é mostrado 30 dias antes.
   * O aviso (amarelo) é mostrado 60 dias antes.
   * Um banner vermelho &quot;Expirado&quot; será exibido assim que uma tecla expirar.

   >[!NOTE]
   >
   >Observe que nenhuma notificação por email será enviada pelo Painel de controle do Campaign.

Como prática recomendada, recomendamos que você remova qualquer chave que não seja mais necessária. Para fazer isso, clique no **...**, em seguida, selecione **[!UICONTROL Delete Key].**.

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>Antes de remover uma chave, verifique se ela não é usada em nenhum fluxo de trabalho do Adobe Campaign para evitar sua falha.

## Vídeo tutorial {#video}

O vídeo abaixo mostra como gerar e instalar chaves GPG para criptografia de dados.

Vídeos tutoriais adicionais relacionados ao gerenciamento de chaves GPG estão disponíveis nas páginas de tutoriais do [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=en#instance-settings) e do [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=en#instance-settings).

>[!VIDEO](https://video.tv.adobe.com/v/36386?quality=12)

