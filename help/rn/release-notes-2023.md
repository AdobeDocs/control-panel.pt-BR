---
title: Notas de versão de 2023
description: Esta página lista todas as versões de 2023 do Painel de controle do Campaign.
exl-id: 9a83e32a-4c11-4784-a6fe-341ce9ebc7a7
source-git-commit: 2a1119022af2ced06052cf48b50d6ff7be2d1faa
workflow-type: ht
source-wordcount: '270'
ht-degree: 100%

---

# Notas de versão de 2023 {#rn-2023}

## Junho de 2023 {#june-2023}

* Agora é possível delegar os certificados SSL de subdomínios já delegados para a Adobe diretamente da lista de subdomínios. [Saiba mais](../subdomains-certificates/using/delegate-ssl.md)

* O remetente dos emails de alerta foi alterado para `"alert@notifications.campaign.adobe.com"`.

## Melhorias de maio de 2023 {#may-2023}

**Delegação de certificados SSL de subdomínios para a Adobe**

Agora, é possível ter os certificados SSL dos subdomínios gerenciados pela Adobe. Se estiver usando CNAMEs para configurar o subdomínio, os registros de certificados serão gerados e fornecidos automaticamente para gerar um certificado na sua solução de hospedagem de domínio.

Observe que esse recurso só está disponível ao configurar um novo subdomínio. Não é possível delegar certificados para subdomínios já delegados. [Saiba mais](../subdomains-certificates/using/setting-up-new-subdomain.md)

>[!NOTE]
>
>O SSL gerenciado pela Adobe é um recurso gratuito que está disponível para os usuários.

## Março de 2023 {#march-2023}

**Remoção de delegação de subdomínio para CNAMEs**

Agora é possível remover a delegação de subdomínios que foram configurados usando CNAMEs. [Saiba mais](../subdomains-certificates/using/remove-delegated-subdomains.md)

## Fevereiro de 2023 {#february-2023}

**Remoção de delegação para subdomínios delegados à Adobe**

Agora é possível remover a delegação de um subdomínio que está totalmente delegado à Adobe. [Saiba mais](../subdomains-certificates/using/remove-delegated-subdomains.md)

>[!NOTE]
>
>A remoção de delegação não está disponível no momento para subdomínios que foram configurados usando CNAMEs.

**Calendário de serviço**

O calendário de serviço agora fornece uma visualização de calendário para rastrear eventos importantes que ocorrem em suas instâncias. Além disso, foram adicionadas informações sobre as notificações enviadas aos usuários que se inscreveram nos alertas do Painel de controle. [Saiba mais](../service-events/service-events.md)

![](assets/do-not-localize/gif-calendar.gif)

## Janeiro de 2023 {#january-2023}

**Novo recurso de modelo de hospedagem híbrida**

Os clientes que utilizam o modelo de hospedagem híbrida agora podem adicionar endereços IP à lista de permissões de acesso às instâncias MID. [Saiba mais](../instances-settings/using/ip-allow-listing-instance-access.md)

**Aprimoramento da solicitação de assinatura de certificado (CSR)**

O campo Cidade/Localidade agora é opcional durante a geração da solicitação de assinatura de certificado.
