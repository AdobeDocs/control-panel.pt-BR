---
title: Sobre subdomínios
description: Saiba mais sobre subdomínios
translation-type: tm+mt
source-git-commit: c2ef995d49118943bdd77e6d3c14ef7ec643e672

---


# Sobre subdomínio {#about-subdomains}

## Por que configurar subdomínios? {#why-setting-up-subdomains}

Um subdomínio é uma divisão do seu domínio que pode ser usada para isolar vários tipos de tráfego (corporativo, informações de marketing etc.).

Vejamos o exemplo do domínio &quot;mybrand.com&quot;, usado para enviar comunicações informativas e de marketing:

* info.mybrand.com para suas comunicações internas
* marketing.mybrand.com para seus emails de prospecção.

Nessa situação, você pode delegar o subdomínio &quot;marketing.mybrand.com&quot; para o Adobe Campaign. Ao fazer isso, você ajudará a preservar a reputação do seu domínio e de outros subdomínios. Por exemplo, se os subdomínios &quot;marketing.mybrand.com&quot; acabassem sendo adicionados à lista negra por provedores de serviços de Internet devido a uma entrega incorreta, isso impediria que todo o domínio &quot;mybrand.com&quot; e o subdomínio &quot;info.mybrand.com&quot; fossem bloqueados.

## Métodos de delegação de subdomínios {#subdomain-delegation-methods}

A delegação de subdomínio permite que você delegue uma subseção do seu domínio (tecnicamente uma &quot;zona DNS&quot;) para uso com o Adobe Campaign. Os métodos de configuração disponíveis são:

* **Delegação completa de subdomínio ao Adobe Campaign** (recomendado)

   O subdomínio é totalmente delegado à Adobe. A Adobe pode fornecer a Campanha como um serviço gerenciado controlando e mantendo todos os aspectos do DNS necessários para fornecer, renderizar e rastrear campanhas por email.

* **Uso de CNAMEs** (não recomendado e não suportado pelo Painel de controle):

   Crie um subdomínio e use CNAMEs para apontar para registros específicos da Adobe. Usando essa configuração, a Adobe e o cliente compartilham a responsabilidade pela manutenção do DNS.

Para obter mais informações sobre cada um desses métodos (responsabilidade implícita, requisitos etc.), consulte [esta documentação](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).
