---
product: campaign
solution: Campaign
title: Gerenciamento de chaves GPG
description: Saiba como gerenciar chaves GPG para criptografar e descriptografar dados no Adobe Campaign.
feature: Control Panel, Encryption
role: Admin
level: Experienced
exl-id: 366dd2ea-c6be-41a2-a4d6-4ffecb5f3d39
source-git-commit: de33a10a168358d0f38ca776fbcd88e0ccf63ce2
workflow-type: tm+mt
source-wordcount: '1146'
ht-degree: 100%

---

# Gerenciamento de chaves GPG {#gpg-keys-management}

>[!CONTEXTUALHELP]
>id="cp_instancesettings_gpg_management"
>title="Sobre chaves GPG"
>abstract="Nessa guia, você pode instalar e/ou gerar chaves GPG em uma instância de marketing para criptografar dados enviados do Campaign e descriptografar dados recebidos."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=pt-BR" text="Sobre o monitoramento de desempenho"

## Sobre a criptografia GPG {#about-gpg-encryption}

A criptografia GPG permite proteger os seus dados com base em um sistema de pares de chaves públicas e privadas que seguem a especificação [OpenPGP](https://www.openpgp.org/about/standard/).

Depois de implementada, os dados de entrada podem ser descriptografados e os dados de saída podem ser criptografados antes da transferência para garantir que não sejam acessados por ninguém sem um par de chaves correspondente válido.

Para implementar a criptografia GPG com o Campaign, as chaves GPG devem ser instaladas e/ou geradas em uma instância de marketing por um usuário(a) administrador(a) no Painel de controle.

Depois será possível:

* **Criptografar dados enviados**: o Adobe Campaign envia os dados após criptografá-los com a chave pública instalada.

* **Descriptografar dados recebidos**: o Adobe Campaign recebe os dados que foram criptografados de um sistema externo, usando uma chave pública baixada do Painel de controle. O Adobe Campaign, em seguida, descriptografa os dados, usando uma chave privada gerada no painel de controle.

## Criptografia de dados {#encrypting-data}

O Painel de controle permite criptografar dados originários de sua instância do Adobe Campaign.

Para isso, é necessário gerar um par de chaves GPG com uma ferramenta de criptografia PGP e, em seguida, instalar a chave pública no Painel de controle. Com isso, será possível criptografar dados antes de enviá-los da sua instância. Para fazer isso, siga as etapas abaixo.

>[!NOTE]
>
>É possível instalar até 60 chaves GPG no Painel de controle.

![](assets/do-not-localize/how-to-video.png)[ Conheça este recurso no vídeo](#video)

1. Gere um par de chaves pública/privada com uma ferramenta de criptografia PGP, seguindo a [especificação OpenPGP](https://www.openpgp.org/about/standard/). Para isso, instale um utilitário GPG ou software GNuGP.

   >[!NOTE]
   >
   >Um software gratuito de código aberto para gerar chaves está disponível. No entanto, siga as diretrizes da sua organização e use o utilitário GPG recomendado pelo departamento de TI/segurança da sua organização.

1. Depois que o utilitário estiver instalado, execute o comando abaixo no Terminal (Mac) ou na linha de comando (Windows).

   `gpg --full-generate-key`

1. Quando solicitado, especifique os parâmetros desejados para a sua chave. Os parâmetros obrigatórios são:

   * **tipo de chave**: RSA
   * **comprimento da chave**: 3.072 - 4.096 bits
   * **nome verdadeiro** e **endereço de email**: permitem rastrear quem criou o par de chaves. Insira um nome e um endereço de email vinculados à sua organização ou departamento.
   * **comentário**: adicionar um rótulo ao campo de comentário ajudará a identificar facilmente a chave a ser usada para criptografar os seus dados.
     >[!IMPORTANT]
     >
     >Certifique-se de que este campo não esteja em branco e um comentário tenha sido inserido.

   * **Expiração**: data ou “0”, no caso de não haver uma data de expiração.
   * **senha**

   ![](assets/do-not-localize/gpg_command.png)

1. Depois de confirmado, o script gerará uma chave com uma impressão digital associada, que você poderá exportar para um arquivo ou colar diretamente no Painel de controle. Para exportar o arquivo, execute este comando seguido da impressão digital da chave gerada.

   `gpg -a --export <fingerprint>`

1. Para instalar a chave pública no Painel de controle, abra o cartão **[!UICONTROL Configurações de instância]** e selecione a guia **[!UICONTROL Chaves GPG]** e a instância desejada.

1. Clique no botão **[!UICONTROL Instalar chave]**.

   ![](assets/gpg_install_button.png)

1. Cole a chave pública gerada pela sua ferramenta de criptografia PGP. Também é possível arrastar e soltar diretamente o arquivo da chave pública exportado.

   >[!NOTE]
   >
   >A chave pública deve estar no formato OpenPGP.

   ![](assets/gpg_install_paste.png)

1. Clique no botão **[!UICONTROL Instalar chave]**.

Uma vez instalada, a chave pública será exibida na lista. Você pode usar o botão **...** para baixá-la ou copiar sua impressão digital.

![](assets/gpg_install_download.png)

A chave ficará disponível para uso em workflows do Adobe Campaign. Você pode usá-la para criptografar dados ao realizar atividades de extração de dados.

![](assets/do-not-localize/how-to-video.png) Conheça este recurso no [vídeo](#video)

Para mais informações sobre esse tópico, consulte a documentação do Adobe Campaign:

**Campaign v7/v8:**

* [Compactação ou criptografia de um arquivo](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html?lang=pt-BR)
* [Caso de uso: criptografia e exportação de dados usando uma chave instalada no Painel de controle](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=pt-BR#use-case-gpg-encrypt)

**Campaign Standard:**

* [Gerenciamento de dados criptografados](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=pt-BR)
* [Caso de uso: criptografia e exportação de dados usando uma chave instalada no Painel de controle](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/zip-encrypt.html?lang=pt-BR#use-case-gpg-encrypt)

## Descriptografia de dados {#decrypting-data}

O Painel de controle permite descriptografar dados externos que entram nas suas instâncias do Adobe Campaign.

Para isso, é necessário gerar um par de chaves GPG diretamente no Painel de controle.

* A **chave pública** será compartilhada com o sistema externo, que a usará para criptografar os dados enviados ao Campaign.
* A **chave privada** será usada pelo Campaign para descriptografar os dados criptografados recebidos.

![](assets/do-not-localize/how-to-video.png) Conheça este recurso no [vídeo](#video)

Para gerar um par de chaves no Painel de controle, siga estas etapas:

1. Abra o cartão **[!UICONTROL Configurações de instância]** e selecione a guia **[!UICONTROL Chaves GPG]** e a instância desejada do Adobe Campaign.

1. Clique no botão **[!UICONTROL Gerar chave]**.

   ![](assets/gpg_generate.png)

1. Especifique o nome da chave e clique em **[!UICONTROL Gerar chave]**. Esse nome ajudará a identificar a chave a ser usada para descriptografia em workflows do Campaign

   ![](assets/gpg_generate_name.png)

Depois que o par de chaves é gerado, a chave pública é exibida na lista. Observe que os pares de chaves de descriptografia são gerados sem data de expiração.

É possível usar o botão **...** para baixar a chave pública ou copiar sua impressão digital.

![](assets/gpg_generate_list.png)

A chave pública ficará disponível para ser compartilhada com qualquer sistema externo. O Adobe Campaign poderá usar a chave privada nas atividades de carregamento de dados para descriptografar dados criptografados com a chave pública.

Para mais informações, consulte a documentação do Adobe Campaign:

**Campaign v7 e v8:**

* [Descompactação ou descriptografia de um arquivo antes do processamento](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html?lang=pt-BR)
* [Caso de uso: importação de dados criptografados usando uma chave gerada pelo Painel de controle](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/importing-and-exporting-data/managing-data-encryption-compression/unzip-decrypt.html?lang=pt-BR#use-case-gpg-decrypt)

**Campaign Standard:**

* [Gerenciamento de dados criptografados](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=pt-BR)
* [Caso de uso: importação de dados criptografados usando uma chave gerada pelo Painel de controle](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/importing-and-exporting-data/managing-encrypted-data.html?lang=pt-BR#use-case-gpg-decrypt)

## Monitoramento de chaves GPG

Para acessar as chaves GPG instaladas e geradas para as suas instâncias, abra o cartão **[!UICONTROL Configurações de instância]** e selecione a guia **[!UICONTROL Chaves GPG]**.

![](assets/gpg_list.png)

A lista exibe todas as chaves GPG de criptografia e descriptografia instaladas e geradas para as suas instâncias com informações detalhadas sobre cada chave:

* **[!UICONTROL Nome]**: o nome definido ao instalar ou gerar a chave.
* **[!UICONTROL Caso de uso]**: esta coluna especifica o caso de uso da chave:

  ![](assets/gpg_icon_encrypt.png): a chave foi instalada para criptografia de dados.

  ![](assets/gpg_icon_decrypt.png): a chave foi gerada para permitir a descriptografia de dados.

* **[!UICONTROL Impressão digital]**: a impressão digital da chave.
* **[!UICONTROL Expira em]**: a data de expiração da chave. Observe que o Painel de controle fornecerá indicações visuais, à medida que a chave for se aproximando da data de vencimento:

   * Urgente (vermelho) é mostrado 30 dias antes.
   * Aviso (amarelo) é exibido 60 dias antes.
   * Um banner vermelho de “Expirada” será exibido assim que uma chave vencer.

  >[!NOTE]
  >
  >Observe que nenhuma notificação por email será enviada pelo Painel de controle.

Como prática recomendada, remova qualquer chave que não seja mais necessária. Para isso, clique no botão **...** e selecione **[!UICONTROL Excluir chave].**

![](assets/gpg_delete.png)

>[!IMPORTANT]
>
>Antes de remover uma chave, certifique-se de que ela não esteja sendo usada em nenhum workflow do Adobe Campaign para evitar falhas.

## Tutorial em vídeo {#video}

O vídeo abaixo mostra como gerar e instalar chaves GPG para criptografia de dados.

Vídeos explicativos adicionais relacionados ao gerenciamento de chaves GPG estão disponíveis nas páginas de tutoriais do [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=pt-BR#instance-settings) e do [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/instance-settings/gpg-key-management/gpg-key-management-overview.html?lang=pt-BR#instance-settings).

>[!VIDEO](https://video.tv.adobe.com/v/327887?quality=12&captions=por_br)
