---
product: campaign
solution: Campaign
title: Versões do Painel de Controle do Campaign
description: Notas de versão mais recentes do Painel de controle do Campaign.
feature: Painel de controle do Campaign
role: Architect
level: Beginner
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
translation-type: tm+mt
source-git-commit: 4c8347f7b0f4a776ea726f02029ea1c92a83406a
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 95%

---

# Versões do Painel de Controle do Campaign {#control-panel-releases}

Aqui você encontrará informações sobre as versões mais recentes do Painel de Controle do Campaign.

>[!NOTE]
>
>O Painel de controle do Campaign é acessível a todos os usuários administradores. As etapas para conceder acesso de Administrador a um usuário estão detalhadas [nesta seção](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=pt-BR#discover-control-panel).
>
>Para o Campaign Classic, observe que sua instância deve ser hospedada no AWS e atualizada com a compilação mais recente do [Gold Standard](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/gs-release/gs-overview.html?lang=pt-BR#release-notes) ou a compilação mais recente do GA (21.1)](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/latest-release.html?lang=pt-BR#release-notes). [ Saiba como verificar sua versão [nesta seção](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=pt-BR#getting-your-campaign-version). Para verificar se sua instância está hospedada no AWS, siga as etapas detalhadas [nesta página](faq.md).

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
