---
product: campaign
solution: Campaign
title: Versões do Painel de Controle do Campaign
description: Notas de versão mais recentes do Painel de controle do Campaign.
feature: Control Panel
role: Architect
level: Beginner
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: 8c604e9b1f657be938b04d096ac22efed99e1cbe
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 73%

---

# Versões do Painel de Controle do Campaign {#control-panel-releases}

Aqui você encontrará informações sobre as versões mais recentes do Painel de Controle do Campaign.

>[!NOTE]
>
>O Painel de controle do Campaign é acessível a todos os usuários administradores. As etapas para conceder acesso de Administrador a um usuário estão detalhadas [nesta seção](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=pt-BR#discover-control-panel).
>
>Para o Campaign Classic v7, observe que sua instância deve ser hospedada no AWS e atualizada com o [construção estável](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/gs-release/rn-overview.html). Saiba como verificar a versão [nesta seção](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=pt-BR#getting-your-campaign-version). Para verificar se sua instância está hospedada no AWS, siga as etapas detalhadas [nesta página](faq.md).

## Outubro de 2021 {#october-2021}

**Intervalo IP e período de validade da chave pública**

Agora é possível definir uma duração para a disponibilidade de intervalos IP e chaves públicas. Leia mais na [Lista de permissões de intervalo IP](sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list) e [Gerenciamento de chaves](sftp/using/key-management.md#installing-ssh-key) seções.

**Intervalo IP e edição de chave pública**

Agora é possível editar a variável [Intervalos de IP](sftp/using/ip-range-allow-listing.md#editing-ip-ranges) e [chaves públicas](sftp/using/key-management.md#editing-public-keys) que você criar. Observe que esse recurso não está disponível para os itens criados antes da versão atual do Painel de controle do Campaign.

**Alertas no intervalo IP SFTP e expiração da chave pública**

A funcionalidade de alerta por email agora inclui alertas sobre IP SFTP, permitindo listar a expiração e a expiração da chave pública SFTP. [Leia mais](performance-monitoring/using/email-alerting.md)

**Suporte total com o Campaign v8**

O **Subdomínio** e **Certificado** Os recursos de gerenciamento agora são suportados pelo Painel de controle do Campaign no Adobe Campaign v8.

## Agosto de 2021 {#august-2021}

**Suporte com o Campaign v8**

O Painel de controle do Campaign agora está disponível para Adobe Campaign v8, exceto o **Subdomínio** e **Certificado** recursos de gerenciamento, que ainda não são compatíveis. Saiba mais na [documentação do Campaign v8](https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html){target=&quot;_blank&quot;}

## Outubro de 2020 {#october-2020}

**Configuração de subdomínio usando CNAMEs**

Agora o Painel de Controle do Campaign permite configurar um subdomínio para funcionar com a Adobe usando CNAMEs diretamente da interface. [Leia mais](subdomains-certificates/using/setting-up-new-subdomain.md)

**Melhorias no monitoramento de banco de dados**

O monitoramento de banco de dados foi aprimorado com métricas adicionais que permitem obter informações detalhadas sobre os recursos que estão consumindo espaço no banco de dados. [Leia mais](performance-monitoring/using/database-monitoring.md)

## Junho de 2020 {#june-2020}

**Auditoria de entrega de subdomínio**

Após delegar um novo subdomínio, o Painel de controle do Campaign agora permite rastrear a auditoria feita pela equipe de avaliação do delivery. [Leia mais](subdomains-certificates/using/setting-up-new-subdomain.md)

**Gerenciamento de chaves GPG**

O Painel de controle do campaign agora permite gerar um par de chaves GPG para que você possa decodificar facilmente os dados externos que chegam ao Campaign. Além disso, adicionamos um recurso para que você possa instalar uma chave GPG pública para criptografar os dados ao deixar o Campaign. [Leia mais](instances-settings/using/gpg-keys-management.md)

**Monitoramento de perfis ativos**

O Painel de controle do Campaign agora permite monitorar o número de perfis ativos usados por suas instâncias e contados para fins de faturamento. [Leia mais](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>O monitoramento de perfis ativos pelo Painel de controle do Campaign está disponível em beta e está sujeito a atualizações e modificações frequentes sem aviso prévio.

## Maio de 2020 {#may-2020}

**Gerenciamento de certificados para subdomínios CNAME**

Agora o Painel de Controle do Campaign permite renovar os certificados SSL de seus subdomínios que foram delegados com o método CNAME. [Leia mais](subdomains-certificates/using/renewing-subdomain-certificate.md)

## Abril de 2020 {#april-2020}

**Gerenciamento de registros TXT do Google**

Adicione o registro de verificação do site Google TXT a todos os seus subdomínios usados para enviar emails para endereços Gmail por meio do Painel de controle do Campaign. [Leia mais](subdomains-certificates/using/managing-txt-records.md)

**Monitoramento de espaço de banco de dados**

O Painel de controle do Campaign está equipado com recursos de monitoramento de banco de dados, permitindo visualizar a utilização do espaço do banco de dados sob demanda e ao longo do tempo. [Leia mais](performance-monitoring/using/database-monitoring.md)

**Alerta por email**

O Painel de controle do Campaign está equipado com recursos de email de alerta em tempo real, permitindo que você faça logon no Painel de controle do Campaign e se inscreva para receber alertas quando o sistema estiver em risco de deterioração do desempenho, ou quando uma ação for necessária para garantir alto desempenho no futuro. [Leia mais](performance-monitoring/using/email-alerting.md)

## Janeiro de 2020 {#january-2020}

*22 de janeiro de 2020*

Adicionamos novos recursos para usuários administradores delegarem subdomínios e renovarem certificados SSL pelo Painel de Controle do Campaign.

Para obter mais informações, consulte estas páginas:
* [Configurar um novo subdomínio](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Renovar um certificado SSL de subdomínio](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Esses recursos estarão disponíveis na versão beta e estão sujeitos a atualizações e modificações frequentes sem aviso prévio.

## Setembro de 2019 {#september-2019}

*16 de setembro de 2019*

Adicionamos novos recursos para que os usuários administradores adicionem endereços IP à lista de permissões para se conectarem às instâncias do Campaign Classic.
Além disso, os usuários administradores agora podem exibir a lista de instâncias do Campaign Classic e a qualificação para atualizações de builds.

Para obter mais informações, consulte a [documentação específica](instances-settings/using/ip-allow-listing-instance-access.md).

## Agosto de 2019 {#august-2019}

Adicionamos novos recursos para que os usuários administradores recebam notificações antes que os certificados SSL de seus domínios expirem. Para obter mais informações, consulte a [documentação detalhada](subdomains-certificates/using/monitoring-ssl-certificates.md).

Além disso, agora os usuários administradores podem excluir chaves SSH que foram adicionadas para acessar os servidores SFTP.

## Julho de 2019 {#july-2019}

Adicionamos novos recursos para potencializar os usuários administradores para que tenham mais controle das configurações de instâncias do Campaign Classic. Os novos recursos do Painel de controle do Campaign incluem a habilidade de adicionar URLs aos quais o Adobe Campaign se conecta para transferir dados/arquivos.

Para obter mais informações, consulte a [documentação detalhada](instances-settings/using/url-permissions.md).
