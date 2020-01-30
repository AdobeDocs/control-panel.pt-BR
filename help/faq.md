---
title: Perguntas frequentes do painel de controle
description: Questões comuns relacionadas com o Painel de Controlo
translation-type: tm+mt
source-git-commit: 9bd57cd6d4430cf2cae8575547f8e332f94940c1

---


# Perguntas frequentes {#faq}

## ID da Org. de IMS {#ims-org-id}

**O que é uma ID organizacional IMS?**

É uma ID exclusiva que é fornecida para sua instância quando você faz logon pela primeira vez na Adobe Experience Cloud. Deve estar no formato: xxx@AdobeOrg.

Para obter mais informações, consulte a documentação [da](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html)Adobe Experience Cloud.

**Onde posso encontrar minha ID organizacional IMS?**

One way is to navigate to [Adobe Experience Cloud Home](https://exc-login.experiencecloud.adobe.com/exc-content/login.html?prefixtenantid=amc) > **[!UICONTROL Administration]**. You will find your IMS Org ID at the bottom of Administration**[!UICONTROL Quick Access]** section. Você pode encontrar informações mais detalhadas na [documentação da Adobe Experience Cloud](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html).

A outra maneira é iniciar o **Admin Console**. A ID de organização do IMS estará visível no URL; ela deve ser semelhante a: https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

**Por que preciso saber minha ID organizacional IMS?**

Para que você gerencie as configurações da sua instância, queremos garantir que você esteja obtendo as informações corretas para a instância correta, caso esteja usando várias instâncias para a sua empresa.

**E se eu tiver várias IDs Org IMS?**

Você pode ter mais de uma ID de organização IMS se tiver acesso a várias soluções da Adobe. Nesse caso, a ID de organização IMS correta que você deve usar é a que você vê na instância do Adobe Campaign.

>[!NOTE]
>
>Se você tiver a mesma ID de organização IMS para o Adobe Campaign e o Adobe Analytics, isso é ótimo. Ter uma ID de organização IMS entre o Analytics e o Campaign é um requisito se você planeja integrar as soluções para aproveitar os casos de uso complexo, como abandono de carrinho de compras (para AA + AC).
>
>Se você tiver IDs de organização IMS diferentes para o Adobe Campaign e o Adobe Analytics, entre em contato com o Atendimento ao cliente para alinhá-las.

**Como posso saber se minha instância do Adobe Campaign está hospedada no AWS ou não?**

Para verificar se sua instância está hospedada no AWS, siga estas etapas:

1. Recupere seu URL de logon. É o URL que você usa para fazer logon na instância do Campaign, que geralmente termina com &quot;.campaign.adobe.com&quot; ou &quot;.neolane.net&quot;.
1. Abra o terminal e execute uma **[!DNL nslookup]**operação no URL de logon.

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

1. Execute uma operação **de pesquisa** no endereço IP retornado.

   `doe-macOS% nslookup 12.34.567.89`

1. Verifique o valor &quot;name&quot; no resultado retornado. Se contiver &quot;amazonaws.com&quot;, isso significa que sua instância está hospedada no AWS.

   ```
   doe-macOS% nslookup 12.34.567.89
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   89.567.34.12.in-addr.arpa   name = ec2-12-34-567-89.address.amazonaws.com.
   ```

>[!NOTE]
>
>Se você deseja migrar para o AWS, inicie o processo entrando em contato com seu Gerente de sucesso do cliente.

## Painel de controle {#control-panel}

**O que é o Painel de controle?**

O Painel de controle permite que os administradores de produtos gerenciem diretamente várias configurações e monitorem a capacidade dos servidores SFTP conectados ao Adobe Campaign.

**Quais são alguns dos recursos atuais do Painel de controle?**

O Painel de controle permite rastrear o armazenamento, a lista de permissões de IPs e gerenciar chaves SSH para seus servidores SFTP por conta própria, com base em suas necessidades e outras ações.

Para obter mais informações, consulte a documentação de ações suportadas pelo Painel de controle.

**O Painel de controle é somente para o Adobe Campaign?**

Sim, você só poderá gerenciar as configurações do Adobe Campaign no Painel de controle.

**Posso usar o Painel de controle?**

O Painel de controle está aberto somente para administradores de produtos de nossos clientes atuais que têm o Adobe Campaign hospedado no AWS.

Se você não é um administrador, mas deseja acessá-lo, entre em contato com o administrador do produto para ajudá-lo a adicioná-lo como administrador.

**Como posso acessar o Painel de controle?**

Siga as instruções detalhadas na documentação Acesso ao Painel de controle.

**Há uma taxa extra para usar o Painel de controle?**

Não, não há custo extra se você for um cliente atual do Adobe Campaign.
