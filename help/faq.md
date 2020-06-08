---
title: Perguntas frequentes do Painel de Controle do Campaign
description: Questões comuns relacionadas ao Painel de Controle do Campaign
translation-type: ht
source-git-commit: 7bde86a86fbd128f4eb7bf029e58b0f95964390b
workflow-type: ht
source-wordcount: '625'
ht-degree: 100%

---


# Perguntas frequentes {#faq}

## ID organizacional IMS {#ims-org-id}

**O que é uma ID organizacional IMS?**

É uma ID exclusiva fornecida para sua instância quando você faz logon pela primeira vez na Adobe Experience Cloud. Ela deve estar no formato: xxx@AdobeOrg.

Para obter mais informações, consulte a [documentação da Adobe Experience Cloud](https://marketing.adobe.com/resources/help/pt_BR/mcloud/organizations.html).

**Onde encontro minha ID organizacional IMS?**

Uma maneira é navegar até a [página inicial da Adobe Experience Cloud](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]**. Você encontrará a ID organizacional IMS na parte inferior da seção **[!UICONTROL Quick Access]** Administração. Você pode encontrar informações mais detalhadas na [documentação da Adobe Experience Cloud](https://marketing.adobe.com/resources/help/pt_BR/mcloud/organizations.html).

Outra maneira é iniciar o **Admin Console**. A ID organizacional IMS estará visível no URL. Deve ser semelhante a: https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

**Por que preciso saber minha ID organizacional IMS?**

Para gerenciar as configurações da sua instância, queremos garantir que você esteja obtendo as informações corretas para a instância certa caso esteja usando várias instâncias para a sua empresa.

**E se eu tiver várias IDs organizacionais IMS?**

Você pode ter mais de uma ID organizacional IMS se tiver acesso a várias soluções da Adobe. Nesse caso, a ID organizacional IMS correta que você deve usar é aquela que você vê na instância do Adobe Campaign.

>[!NOTE]
>
>Caso você tenha a mesma ID organizacional IMS para o Adobe Campaign e o Adobe Analytics, está ótimo. Ter a mesma ID organizacional IMS para o Analytics e o Campaign é um requisito se você planeja integrar as soluções para aproveitar os casos de uso complexo, como abandono de carrinho de compras (para AA + AC).
>
>Se você tiver IDs organizacionais IMS diferentes para o Adobe Campaign e o Adobe Analytics, entre em contato com o Atendimento ao cliente para alinhá-las.

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

O Painel de controle do Campaign permite rastrear armazenamentos, listas de permissões de IPs e gerenciar chaves SSH de servidores SFTP por conta própria, com base em suas necessidades e outras ações.

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
