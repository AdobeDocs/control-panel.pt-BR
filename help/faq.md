---
product: campaign
solution: Campaign
title: Perguntas frequentes do Painel de Controle do Campaign
description: Questões comuns relacionadas ao Painel de Controle do Campaign
feature: Control Panel
role: Admin
level: Intermediate
exl-id: 4f329764-ed8b-4939-affc-ed994fd6101d
source-git-commit: e8bffd8e7f571fd85c725adf837c2997f7615fcd
workflow-type: ht
source-wordcount: '786'
ht-degree: 100%

---

# Perguntas frequentes {#faq}

## Painel de controle {#control-panel}

### O que é o Painel de controle?

O painel de Controle do Campaign permite que os administradores de produtos gerenciem diretamente várias configurações e monitorem a capacidade dos servidores SFTP conectados ao Adobe Campaign.

### Quais são alguns dos recursos atuais do Painel de controle?

O Painel de controle permite rastrear armazenamentos, adicionar IPs à lista de permissões e gerenciar chaves SSH de servidores SFTP por conta própria, com base em suas necessidades e outras ações.

Para obter mais informações, consulte a documentação de ações compatíveis com o Painel de controle.

### Há recursos que ainda não estão disponíveis no Campaign v8, mas estão disponíveis no Campaign Classic v7?{#v8-restrictions}

Não. Todos os recursos disponíveis no Campaign v7 agora também estão disponíveis através do Painel de controle v8, incluindo funções relacionadas ao Subdomínio e Gerenciamento de certificados.

### O Painel de controle é apenas para o Adobe Campaign?

Sim, você só poderá gerenciar as configurações para o Adobe Campaign no Painel de controle.

### Posso usar o Painel de controle?

O Painel de controle está aberto somente para administradores de produtos de nossos clientes atuais que têm o Adobe Campaign hospedado no AWS.

O Painel de controle permite que clientes com o modelo de hospedagem híbrida aproveitem seus recursos específicos. Para fazer isso, é necessário fornecer o URL da instância MID/RT configurado em sua instância de marketing do Painel de controle. [Saiba mais](instances-settings/using/external-accounts.md)

Se você não for administrador, mas quiser acessá-lo, entre em contato com o administrador do produto para ser adicionado como administrador.

### Como usuário do Campaign Classic v7, quais são as condições para acessar o Painel de controle? {#v7-restrictions}

O Painel de controle é restrito aos usuários administradores. [Saiba mais](discover/using/managing-permissions.md).

Para o Campaign v7, observe que sua instância deve estar hospedada no Amazon Web Services (AWS) e atualizada para a [build estável do Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=pt-BR#rn-statuses) mais recente ou para a build 9032 ou superior. Saiba como verificar a versão do Campaign Classic v7 [nesta seção](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=pt-BR#getting-your-campaign-version). Para verificar se sua instância do Campaign Classic está hospedada no AWS, siga as etapas detalhadas [nesta seção](#hosted-aws).

### Como posso acessar o Painel de controle?

Siga as instruções detalhadas na documentação Acesso ao Painel de controle.

### Há uma taxa extra para usar o Painel de controle?

Não, não há custo extra se você for cliente do Adobe Campaign.

## ID da organização {#ims-org-id}

### O que é a ID da organização?

É uma ID exclusiva fornecida para sua instância quando você faz logon pela primeira vez na Adobe Experience Cloud. Ela deve estar no formato: xxx@AdobeOrg.

Para obter mais informações, consulte a [documentação da Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=pt-BR).

### Onde encontro minha ID da organização?

Uma maneira é navegar até [página inicial da Adobe Experience Cloud](https://experiencecloud.adobe.com/) > **[!UICONTROL Administração]**. Você encontrará a ID da organização na parte inferior da seção **[!UICONTROL Acesso rápido]** em Administração. Você pode encontrar informações mais detalhadas na [documentação da Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=pt-BR).

Outra maneira é iniciar o **Admin Console**. A ID da organização estará visível no URL e será semelhante a: https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

### Por que preciso saber minha ID da organização?

Para gerenciar as configurações da sua instância, queremos garantir que você esteja obtendo as informações corretas para a instância certa, caso esteja usando várias instâncias para a sua empresa.

### E se eu tiver várias IDs de organização?

Você pode ter mais de uma ID de organização caso tenha acesso a várias soluções da Adobe. Nesse caso, a ID de organização correta que deve ser usada é aquela que você vê na instância do Adobe Campaign.

>[!NOTE]
>
>Caso você tenha a mesma ID de organização para o Adobe Campaign e o Adobe Analytics, isso é ótimo. Ter a mesma ID de organização para o Analytics e o Campaign é um requisito caso você planeje integrar as soluções para aproveitar os casos de uso complexos, como abandono de carrinho de compras (para o AA + AC).
>
>Se suas IDs de organização forem diferentes para o Adobe Campaign e o Adobe Analytics, entre em contato com o Atendimento ao cliente para alinhá-las.

### Como posso saber se minha instância do Adobe Campaign está hospedada no AWS ou não?{#hosted-aws}

Para verificar se sua instância está hospedada no AWS, siga estas etapas:

1. Recupere o URL de logon. É o URL que você usa para fazer logon na instância do Campaign, que geralmente termina com &quot;.campaign.adobe.com&quot; ou &quot;.neolane.net&quot;.
1. Abra o terminal e execute uma operação **[!DNL nslookup]** no URL de logon.

   `doe-macOS% nslookup myinstance.campaign.adobe.com`

1. A resposta retorna informações sobre sua instância.

   ```
   doe-macOS% nslookup myinstance.campaign.adobe.com
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   myinstance.campaign.adobe.com
   canonical name = myinstance-mkt-prod1.campaign.adobe.com.
   myinstance-mkt-prod1.campaign.adobe.com
   canonical name = myinstance-mkt-prod1-1.campaign.adobe.com.
   Name: myinstance-mkt-prod1-1.campaign.adobe.com
   Address: 12.34.567.89
   ```

1. Execute uma operação **nslookup** no endereço IP retornado.

   `doe-macOS% nslookup 12.34.567.89`

1. Verifique o valor &quot;name&quot; no resultado retornado. Se tiver &quot;amazonaws.com&quot;, significa que a instância está hospedada no AWS.

   ```
   doe-macOS% nslookup 12.34.567.89
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   89.567.34.12.in-addr.arpa   name = ec2-12-34-567-89.address.amazonaws.com.
   ```

>[!NOTE]
>
>Se você quiser migrar para o AWS, inicie o processo entrando em contato com o Gerente de Sucesso do Cliente.
