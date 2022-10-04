---
product: campaign
solution: Campaign
title: Perguntas frequentes do Painel de Controle do Campaign
description: Questões comuns relacionadas ao Painel de Controle do Campaign
feature: Control Panel
role: Architect
level: Intermediate
exl-id: 4f329764-ed8b-4939-affc-ed994fd6101d
source-git-commit: c834ae7226ed9dd1f78d4f4511b52cb5f04abfae
workflow-type: tm+mt
source-wordcount: '783'
ht-degree: 78%

---

# Perguntas frequentes {#faq}

## Painel de controle do Campaign {#control-panel}

### O que é o Painel de controle do Campaign?

O painel de Controle do Campaign permite que os administradores de produtos gerenciem diretamente várias configurações e monitorem a capacidade dos servidores SFTP conectados ao Adobe Campaign.

### Quais são alguns dos recursos atuais do Painel de controle do Campaign?

O Painel de controle do Campaign permite rastrear armazenamentos, adicionar IPs à lista de permissões e gerenciar chaves SSH de servidores SFTP por conta própria, com base em suas necessidades e outras ações.

Para obter mais informações, consulte a documentação de ações compatíveis com o Painel de controle do Campaign.

### Há recursos que ainda não estão disponíveis no Campaign v8, mas estão disponíveis no Campaign Classic v7?{#v8-restrictions}

Não. Todos os recursos disponíveis no Campaign v7 agora também estão disponíveis através do Painel de controle do Campaign v8, incluindo funções relacionadas ao Subdomínio e Gerenciamento de certificados.

### O Painel de controle do Campaign é apenas para o Adobe Campaign?

Sim, você só poderá gerenciar as configurações para o Adobe Campaign no Painel de controle do Campaign.

### Posso usar o Painel de controle do Campaign?

O Painel de controle do Campaign está aberto somente para administradores de produtos de nossos clientes atuais que têm o Adobe Campaign hospedado no AWS.

O Painel de controle do Campaign permite que clientes com o modelo de hospedagem híbrida aproveitem seus recursos específicos. Para fazer isso, é necessário fornecer o URL da instância MID/RT configurado em sua instância de marketing do Painel de controle do Campaign. [Saiba mais](instances-settings/using/external-accounts.md)

Se você não for administrador, mas quiser acessá-lo, entre em contato com o administrador do produto para ser adicionado como administrador.

### Como usuário do Campaign Classic v7, quais são as condições para acessar o Painel de controle do Campaign? {#v7-restrictions}

O Painel de controle do Campaign é restrito aos usuários administradores. [Saiba mais](discover/using/managing-permissions.md).

Para o Campaign v7, observe que sua instância deve estar hospedada no Amazon Web Services (AWS) e atualizada para a [build estável do Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=pt-BR#rn-statuses) mais recente ou para a build 9032 ou superior. Saiba como verificar a versão do Campaign Classic v7 [nesta seção](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=pt-BR#getting-your-campaign-version). Para verificar se sua instância do Campaign Classic está hospedada no AWS, siga as etapas detalhadas [nesta seção](#hosted-aws).

### Como posso acessar o Painel de controle do Campaign?

Siga as instruções detalhadas na documentação Acesso ao Painel de controle do Campaign.

### Há uma taxa extra para usar o Painel de controle do Campaign?

Não, não há custo extra se você for cliente do Adobe Campaign.

## ID da organização {#ims-org-id}

### O que é uma ID da organização?

É uma ID exclusiva fornecida para sua instância quando você faz logon pela primeira vez na Adobe Experience Cloud. Ela deve estar no formato: xxx@AdobeOrg.

Para obter mais informações, consulte a [documentação da Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=pt-BR).

### Onde encontro minha ID da organização?

Uma maneira é navegar até a [página inicial da Adobe Experience Cloud](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]**. Você encontrará a ID da organização na parte inferior da Administração **[!UICONTROL Quick Access]** seção. Você pode encontrar informações mais detalhadas na [documentação da Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).

Outra maneira é iniciar o **Admin Console**. A ID da organização estará visível no URL. Deve ser semelhante a: https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

### Por que preciso saber minha ID da organização?

Para gerenciar as configurações da sua instância, queremos garantir que você esteja obtendo as informações corretas para a instância certa, caso esteja usando várias instâncias para a sua empresa.

### E se eu tiver várias IDs de organização?

Você pode ter mais de uma ID de empresa se tiver acesso a várias soluções do Adobe. Nesse caso, a ID correta da organização que você deve usar é aquela que você vê na instância do Adobe Campaign.

>[!NOTE]
>
>Se você tiver a mesma ID da organização para Adobe Campaign e Adobe Analytics, está ótimo. Ter uma ID de empresa entre o Analytics e o Campaign é um requisito caso você planeje integrar as soluções para aproveitar os casos de uso complexos, como abandono de carrinho de compras (para AA + AC).
>
>Se você tiver IDs de organização diferentes para Adobe Campaign e Adobe Analytics, entre em contato com o Atendimento ao cliente para alinhá-las.

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
