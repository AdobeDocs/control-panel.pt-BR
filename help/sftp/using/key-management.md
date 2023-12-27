---
product: campaign
solution: Campaign
title: Gerenciamento de chaves
description: Saiba como gerenciar chaves para conexão com servidores SFTP
feature: Control Panel, SFTP Management
role: Admin
level: Experienced
exl-id: 03815e01-6371-4e1c-b4b8-7abe25957cee
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '1058'
ht-degree: 100%

---

# Gerenciamento de chaves {#key-management}

>[!CONTEXTUALHELP]
>id="cp_key_management"
>title="Sobre o gerenciamento de chaves públicas"
>abstract="Nessa guia, crie, gerencie e edite suas chaves públicas."
>additional-url="https://images-tv.adobe.com/mpcv3/8a977e03-d76c-44d3-853c-95d0b799c870_1560205338.1920x1080at3000_h264.mp4#t=166" text="Assista ao vídeo de demonstração"

A Adobe recomenda que todos os clientes estabeleçam conexão com os servidores SFTP usando um **par de chaves públicas e privadas**.

As etapas para gerar uma chave pública SSH e adicioná-la para acessar o servidor SFTP são descritas abaixo, bem como recomendações relacionadas à autenticação.

Quando o acesso ao servidor estiver configurado, lembre-se de **adicionar os endereços IP que exigirão acesso ao servidor para a lista de permissões** para que você possa se conectar a ele. Para obter mais informações, consulte [esta seção](../../instances-settings/using/ip-allow-listing-instance-access.md).

![](assets/do-not-localize/how-to-video.png) Conheça este recurso no vídeo usando o [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/sftp-management/generate-ssh-key.html?lang=pt-BR#sftp-management) ou o [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/sftp-management/generate-ssh-key.html?lang=pt-BR#sftp-management)

## Práticas recomendadas {#best-practices}

**Sobre a chave pública SSH**

Use sempre a mesma autenticação para se conectar ao servidor e use um formato compatível para a chave.

**Integração da API com nome de usuário e senha**

Em casos muito raros, a autenticação com senha está habilitada para alguns servidores SFTP. A Adobe recomenda usar a autenticação com chave, pois esse método é mais eficiente e seguro. Para solicitar a autenticação com chave, entre em contato com o Atendimento ao cliente.

>[!IMPORTANT]
>
>Se a senha expirar, mesmo se houver chaves instaladas no sistema, não será possível fazer logon em suas contas SFTP.

## Instalação da chave SSH {#installing-ssh-key}

>[!CONTEXTUALHELP]
>id="cp_sftp_publickey_add"
>title="Adição de chave pública"
>abstract="Gere uma chave SSH pública para uma instância e adicione-a ao Painel de controle do Campaign para acessar o servidor SFTP."

>[!IMPORTANT]
>
>É necessário sempre seguir as diretrizes da organização em relação às chaves SSH. As etapas abaixo são apenas um exemplo de como a criação de chaves SSH pode ser realizada, sendo que as chaves servem como um ponto de referência útil para informar os requisitos à sua equipe ou grupo na rede interna.

1. Navegue até a guia **[!UICONTROL Gerenciamento de chaves]** e clique no botão **[!UICONTROL Adicionar nova chave pública]**.

   ![](assets/key0.png)

1. Na caixa de diálogo que é exibida, selecione o nome de usuário para o qual deseja criar a chave pública e o servidor para o qual deseja ativar a chave.

   ![](assets/key1.png)

   >[!NOTE]
   >
   >O Painel de controle verificará se um determinado nome de usuário está ativo em uma certa instância e dará a opção de ativar a chave em uma ou várias instâncias.
   >
   >Uma ou mais chaves públicas SSH podem ser adicionadas para cada usuário.

1. Para gerenciar melhor as suas chaves públicas, é possível definir uma duração para a disponibilidade de cada chave. Para isso, selecione uma unidade na lista suspensa **[!UICONTROL Tipo]** e defina uma duração no campo correspondente. Para mais informações sobre a expiração de chaves públicas, consulte [esta seção](#expiry).

   ![](assets/key_expiry.png)

   >[!NOTE]
   >
   >Por padrão, o campo **[!UICONTROL Tipo]** é definido como **[!UICONTROL Ilimitado]**, o que significa que a chave pública nunca vencerá.

1. No campo **[!UICONTROL Comentário]**, você pode indicar um motivo para adicionar essa chave pública (por quê, para quem etc.).

1. Para preencher o campo **[!UICONTROL Chave pública]**, é necessário gerar uma chave pública SSH. Siga as etapas abaixo de acordo com o seu sistema operacional.

   **Linux e Mac:**

   Use o Terminal para gerar um par de chaves públicas e privadas:
   1. Digite este comando: `ssh-keygen -m pem -t rsa -b 2048 -C "your_email@example.com"`.
   1. Quando solicitado, forneça um nome para a chave. Se o diretório .ssh não existir, o sistema criará um para você.
   1. Digite, e em seguida insira novamente, uma senha quando solicitado. Esse campo também pode ser deixado em branco.
   1. Um par de chaves &quot;name&quot; e &quot;name.pub&quot; é criado pelo sistema. Procure o arquivo &quot;name.pub&quot; e abra-o. Ele deve ter uma string alfanumérica terminando com o endereço de email especificado.

   **Windows:**

   Talvez seja necessário instalar uma ferramenta de terceiros para ajudar a gerar um par de chaves privada/pública no mesmo formato “nome.pub”.

1. Abra o arquivo .pub e copie e cole a string inteira começando por “ssh...” no Painel de controle.

   ![](assets/publickey.png)

   >[!NOTE]
   >
   >O campo **[!UICONTROL Chave pública]** só aceita o formato OpenSSH. O tamanho da chave pública SSH deve ser de **2048 bits**.

1. Clique no botão **[!UICONTROL Salvar]** para criar a chave. O Painel de controle salvará a chave pública e sua impressão digital associada, criptografada com o formato SHA256.

>[!IMPORTANT]
>
>Se a chave criada for usada para estabelecer uma conexão com um sistema que nunca foi conectado ao servidor SFTP selecionado, será necessário adicionar um IP público desse sistema à lista de permissões antes de poder usar esse sistema com o servidor SFTP. Consulte [esta seção](ip-range-allow-listing.md).

É possível utilizar as impressões digitais para corresponder as chaves privadas salvas no computador às respectivas chaves públicas salvas no Painel de controle.

![](assets/fingerprint_compare.png)

O botão “**...**” permite excluir uma chave já existente ou copiar sua impressão digital associada para a área de transferência.

![](assets/key_options.png)

## Gerenciamento de chaves públicas {#managing-public-keys}

As chaves públicas criadas são exibidas na guia **[!UICONTROL Gerenciamento de chaves]**.

É possível classificar os itens com base na data de criação ou de edição, no usuário que os criou ou editou e na expiração do intervalo de IP.

Você também pode pesquisar uma chave pública, começando a digitar um nome ou um comentário.

![](assets/control_panel_key_management_sort.png)

Para editar um ou mais intervalos de IP, consulte [esta seção](#editing-public-keys).

Para excluir uma ou mais chaves públicas da lista, selecione-as e clique no botão **[!UICONTROL Excluir chave pública]**.

![](assets/control_panel_delete_key.png)

### Expiração {#expiry}

A coluna **[!UICONTROL Expira em]** mostra quantos dias restam até que a chave pública vença.

Se tiver se inscrito nos [alertas por email](../../performance-monitoring/using/email-alerting.md), você receberá notificações por email 10 e 5 dias antes do vencimento de uma chave pública, bem como no dia em que ela vencer. Ao receber o alerta, será possível [editar a chave pública](#editing-public-keys) para prorrogar seu período de validade, se necessário.

Uma chave pública vencida será excluída automaticamente após sete dias. Ela será mostrada como **[!UICONTROL Expirada]** na coluna **[!UICONTROL Expira em]**. Nesse período de 7 dias:

* Uma chave pública vencida não pode mais ser usada para se conectar ao servidor SFTP.

* É possível [editar](#editing-public-keys) uma chave pública vencida e atualizar sua duração para disponibilizá-la novamente.

* Você pode excluí-la da lista.

## Edição de chaves públicas {#editing-public-keys}

>[!CONTEXTUALHELP]
>id="cp_sftp_publickey_update"
>title="Editar chaves públicas"
>abstract="Atualize as chaves públicas selecionadas para acessar o servidor SFTP."

Para editar chaves públicas, siga as etapas abaixo.

>[!NOTE]
>
>Você só pode editar chaves públicas criadas a partir da versão de outubro de 2021 do painel de controle.

1. Selecione um ou mais itens na lista **[!UICONTROL Gerenciamento de chaves]**.
1. Clique no botão **[!UICONTROL Atualizar chave pública]**.

   ![](assets/control_panel_edit_key.png)

1. Só é possível editar a expiração da chave pública e/ou adicionar um novo comentário.

   >[!NOTE]
   >
   >Para modificar o nome de usuário, a instância e a chave pública no formato OpenSSH, exclua a chave pública e crie uma nova que corresponda às suas necessidades.

1. Salve as alterações.
