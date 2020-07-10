---
title: Perguntas frequentes do Painel de Controle do Campaign
description: Questões comuns relacionadas ao Painel de Controle do Campaign
translation-type: tm+mt
source-git-commit: 35723590195ef54df42d1d1df5b37490787f8836
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 66%

---


# Perguntas frequentes {#faq}

## IMS Organization ID {#ims-org-id}

**O que é uma ID da organização IMS?**

É uma ID exclusiva fornecida para sua instância quando você faz logon pela primeira vez na Adobe Experience Cloud. Ela deve estar no formato: xxx@AdobeOrg.

Para obter mais informações, consulte a [documentação da Adobe Experience Cloud](https://marketing.adobe.com/resources/help/pt_BR/mcloud/organizations.html).

**Onde posso encontrar minha ID de empresa IMS?**

Uma maneira é navegar até a [página inicial da Adobe Experience Cloud](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]**. You will find your IMS Organization ID at the bottom of Administration **[!UICONTROL Quick Access]** section. Você pode encontrar informações mais detalhadas na [documentação da Adobe Experience Cloud](https://marketing.adobe.com/resources/help/pt_BR/mcloud/organizations.html).

Outra maneira é iniciar o **Admin Console**. A ID de empresa do IMS estará visível no URL, mas deve ser semelhante a: https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

**Por que preciso saber minha ID de empresa IMS?**

Para gerenciar as configurações da sua instância, queremos garantir que você esteja obtendo as informações corretas para a instância certa caso esteja usando várias instâncias para a sua empresa.

**E se eu tiver várias IDs de organização IMS?**

Você pode ter mais de uma ID de empresa do IMS se tiver acesso a várias soluções da Adobe. Nesse caso, a ID de empresa IMS correta que você deve usar é aquela que você vê na instância do Adobe Campaign.

>[!NOTE]
>
>Se você tiver a mesma ID de organização IMS para Adobe Campaign e Adobe Analytics, isso é ótimo. Ter uma ID de empresa IMS entre a Analytics e a Campanha é uma exigência se você planeja integrar as soluções para aproveitar os casos de uso complexo, como abandono do carrinho de compras (para AA + AC).
>
>Se você tiver IDs de organização IMS diferentes para Adobe Campaign e Adobe Analytics, entre em contato com o Atendimento ao cliente para alinhá-las.

**Como posso saber se minha instância do Adobe Campaign está hospedada no AWS ou não?**

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

## Painel de controle do Campaign {#control-panel}

**O que é o Painel de controle do Campaign?**

O Painel de Controle do Campaign permite que os administradores de produtos gerenciem diretamente várias configurações e monitorem a capacidade dos servidores SFTP conectados ao Adobe Campaign.

**Quais são alguns dos recursos atuais do Painel de controle do Campaign?**

O Painel de controle permite que você rastreie armazenamentos, adicione IPs à lista de permissões e gerencie chaves SSH para seus servidores SFTP por conta própria, com base em suas necessidades e outras ações.

Para obter mais informações, consulte a documentação de ações compatíveis com o Painel de controle do Campaign.

**O Painel de controle é apenas para o Adobe Campaign?**

Sim, você só poderá gerenciar as configurações para o Adobe Campaign no Painel de controle.

**Posso usar o Painel de controle do Campaign?**

O Painel de controle do Campaign está aberto somente para administradores de produtos de nossos clientes atuais que têm o Adobe Campaign hospedado no AWS. Observe que ambientes híbridos ainda não são compatíveis.

Se você não for administrador, mas quiser acessá-lo, entre em contato com o administrador do produto para ser adicionado como administrador.

**Como posso acessar o Painel de controle do Campaign?**

Siga as instruções detalhadas na documentação Acesso ao painel de controle do Campaign.

**Há uma taxa extra para usar o Painel de controle do Campaign?**

Não, não há custo extra se você for cliente do Adobe Campaign.
