---
title: Marca de subdomínios
description: Saiba mais sobre a marca de subdomínios
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Marca de subdomínios {#subdomains-branding}

## Por que configurar subdomínios? {#why-setting-up-subdomains}

Um subdomínio é uma divisão do seu domínio que pode ser usada para isolar suas marcas ou vários tipos de tráfego (mensagens transacionais, informações de marketing etc.).

Vejamos o exemplo do domínio &quot;mybrand.com&quot;, usado para enviar comunicações transacionais e de marketing. Nessa situação, você pode decidir configurar dois subdomínios:

* subdomínio &quot;info.mybrand.com&quot; para suas comunicações transacionais (confirmação de compras, redefinição de senha etc.),
* subdomínio &quot;marketing.mybrand.com&quot; para seus emails de prospecção.

Ao fazer isso, você ajudará a preservar a reputação do seu domínio e de outros subdomínios. Por exemplo, se os subdomínios &quot;marketing.mybrand.com&quot; acabassem sendo adicionados à lista negra por provedores de serviços de Internet devido a uma entrega incorreta, isso impediria que todo o domínio &quot;mybrand.com&quot; e o subdomínio &quot;info.mybrand.com&quot; fossem adicionados à lista negra.

## Métodos de delegação de subdomínios {#subdomain-delegation-methods}

A delegação de subdomínio permite que você delegue uma subseção do seu domínio (tecnicamente uma &quot;zona DNS&quot;) para uso com o Adobe Campaign. Os métodos de configuração disponíveis são:

* **Delegação completa de subdomínio ao Adobe Campaign** (recomendado): O subdomínio é totalmente delegado à Adobe. A Adobe pode fornecer a Campanha como um serviço gerenciado controlando e mantendo todos os aspectos do DNS necessários para fornecer, renderizar e rastrear campanhas por email.

* **Uso de CNAMEs** (não recomendado e não suportado pelo Painel de controle): Crie um subdomínio e use CNAMEs para apontar para registros específicos da Adobe. Usando essa configuração, a Adobe e o cliente compartilham a responsabilidade pela manutenção do DNS.

A tabela abaixo apresenta um resumo de como esses métodos funcionam, bem como o nível de esforço implícito:

| Método de delegação | Como funciona | Nível de esforço |
|---|---|---|
| **Delegação completa** | Crie o subdomínio e o registro de namespace. A Adobe configurará todos os registros DNS necessários para o Adobe Campaign.<br/><br/>Nesta configuração, a Adobe é totalmente responsável por gerenciar o subdomínio e todos os registros de DNS. | Baixo |
| **CNAME, método personalizado** | Crie o subdomínio e o registro de namespace. A Adobe fornecerá os registros a serem colocados em seus servidores DNS e configurará os valores correspondentes nos servidores DNS do Adobe Campaign.<br/><br/>Nesta configuração, você e a Adobe compartilham a responsabilidade pela manutenção do DNS. | Alto |

Informações adicionais sobre a delegação de domínio estão disponíveis[nesta documentação](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).
