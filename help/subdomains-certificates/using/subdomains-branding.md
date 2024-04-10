---
product: campaign
solution: Campaign
title: Marca de subdomínios
description: Saiba mais sobre marca de subdomínios
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Intermediate
exl-id: a489d051-fb95-45cf-bb6d-33aef10b7795
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 100%

---

# Marca de subdomínios {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="Sobre subdomínios e certificados SSL"
>abstract="Monitore subdomínios e os certificados SSL associados."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html?lang=pt-BR" text="Monitorar certificados SSL"

## Por que configurar subdomínios? {#why-setting-up-subdomains}

Um subdomínio é uma divisão do seu domínio que pode ser usada para isolar suas marcas ou vários tipos de tráfego (mensagens transacionais, informações de marketing etc.).

Vamos ver o exemplo do domínio &quot;mybrand.com&quot;, usado para enviar comunicações transacionais e de marketing. Nessa situação, você pode optar por configurar dois subdomínios:

* subdomínio &quot;info.mybrand.com&quot; para comunicações transacionais (confirmação de compras, redefinição de senha etc.),
* subdomínio &quot;marketing.mybrand.com&quot; para emails de prospecção.

Ao fazer isso, você ajudará a preservar a reputação do seu domínio e de outros subdomínios. Por exemplo, se os subdomínios &quot;marketing.mybrand.com&quot; acabassem sendo incluídos na lista de bloqueios por provedores de serviço de internet devido a uma entrega incorreta, isso evitaria que todo o domínio &quot;mybrand.com&quot; e o subdomínio &quot;info.mybrand.com&quot; fossem incluídos na lista de bloqueios.

## Métodos de configuração de subdomínios {#subdomain-delegation-methods}

A configuração de subdomínios permite definir uma subseção do seu domínio (tecnicamente, uma “zona DNS”) para uso com o Adobe Campaign. Os métodos de configuração disponíveis são:

* **Delegação completa do subdomínio para o Adobe Campaign** (recomendado): o subdomínio é totalmente delegado à Adobe. A Adobe pode disponibilizar o Campaign como um serviço gerenciado controlando e mantendo todos os aspectos do DNS necessários para fornecer, renderizar e rastrear campanhas de email.

* **Uso de CNAMEs**: crie um subdomínio e use CNAMEs para apontar para os registros específicos da Adobe. Usando essa configuração, a Adobe e o cliente compartilham a responsabilidade pela manutenção do DNS.

A tabela abaixo apresenta um resumo de como esses métodos funcionam, bem como o nível de esforço necessário:

| Método de configuração | Como funciona | Nível de esforço |
|---|---|---|
| **Delegação completa** | Crie o subdomínio e o registro de namespace. A Adobe irá configurar todos os registros DNS necessários para o Adobe Campaign.<br/><br/>Nesta configuração, a Adobe é totalmente responsável pelo gerenciamento do subdomínio e de todos os registros DNS. | Baixo |
| **CNAME, método personalizado** | Crie o subdomínio e o registro de namespace. A Adobe fornecerá os registros que serão colocados em seus servidores DNS e configurará os valores correspondentes em servidores DNS do Adobe Campaign.<br/><br/>Nessa configuração, você e a Adobe compartilham a responsabilidade pela manutenção do DNS. | Alto |

Outras informações sobre a delegação de domínios estão disponíveis [nesta documentação](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=pt-BR).

Em caso de dúvida sobre os métodos de configuração de subdomínios, entre em contato com a equipe de capacidade de entrega da Adobe ou o atendimento ao cliente para solicitar consultoria sobre capacidade de entrega.

## Casos de uso de subdomínios (Campaign v7/v8){#subdomains-use-cases}

>[!CONTEXTUALHELP]
>id="cp_add_subdomain_usecase_selection"
>title="Selecionar o caso de uso para seu subdomínio"
>abstract="Separar os subdomínios por casos de uso é uma prática recomendada de entregabilidade. Assim, a reputação de cada subdomínio é isolada e protegida."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=pt-BR" text="Configurar um novo subdomínio"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/subdomains-branding.html?lang=pt-BR" text="Marca de subdomínios"

Ao configurar subdomínios para instâncias do Campaign v7/v8, é necessário selecionar o caso de uso para o qual o subdomínio será usado (consulte [Configuração de um novo subdomínio](../../subdomains-certificates/using/setting-up-new-subdomain.md)).

Os possíveis casos de uso são:

* **Comunicações de marketing**: comunicações destinadas a fins comerciais. Exemplo: campanha de email de vendas.

* **Comunicações transacionais e operacionais**: as comunicações transacionais contêm informações destinadas a concluir um processo que o destinatário iniciou com você. Exemplo: confirmação de compra, email de redefinição de senha. As comunicações organizacionais estão relacionadas com o intercâmbio de informações, ideias e visualizações dentro e fora da organização, sem fins comerciais.

**Separar os subdomínios de acordo com os casos de uso é uma prática recomendada para a entrega**. Assim, a reputação de cada subdomínio é isolada e protegida. Por exemplo, se o subdomínio para comunicações de marketing acabar sendo incluído na lista de bloqueios por provedores de serviço de internet, o subdomínio de comunicações transacionais não será afetado e continuará sendo capaz de enviar comunicações.

**É possível configurar subdomínios para casos de uso de marketing e transacionais**:

* Para casos de uso de Marketing, os subdomínios serão configurados em instâncias **MID** (Mid sourcing).
* Para casos de uso transacional, os subdomínios serão configurados em TODAS as instâncias **RT** (Centro de mensagens/Mensagens em tempo real) para garantir a conectividade. Os subdomínios operarão, portanto, com todas as instâncias de RT.

>[!NOTE]
>
>Se você estiver usando o Campaign v7/v8, o Painel de controle permitirá ver quais instâncias de RT/MID estão conectadas à instância de marketing com a qual você está trabalhando. Para obter mais informações, consulte a seção [Detalhes da instância](../../instances-settings/using/instance-details.md).

**Tópicos relacionados:**

* [Configurar um novo subdomínio](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Monitoramento de subdomínios](../../subdomains-certificates/using/monitoring-subdomains.md)
