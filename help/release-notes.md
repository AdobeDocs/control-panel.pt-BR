---
title: Versões do Painel de Controle do Campaign
translation-type: tm+mt
source-git-commit: 5b7e8126789690662e72e72c885700b971362004
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 70%

---


# Versões do Painel de Controle do Campaign {#control-panel-releases}

Aqui você encontrará informações sobre as versões mais recentes do Painel de controle do Campaign.

>[!NOTE]
>
>Observe que o Painel de controle do Campaign está disponível somente para clientes hospedados no AWS, exceto para ambientes híbridos que ainda não são compatíveis. Nenhuma atualização é necessária para acessar o Painel de controle do Campaign. Você deve ser um usuário administrador para acessá-lo.

## June 2020 {#june-2020}

**Auditoria de entrega do subdomínio**

Depois de delegar um novo subdomínio, o Painel de controle agora permite que você rastreie a auditoria realizada pela equipe de Disponibilidade. [Leia mais](subdomains-certificates/using/setting-up-new-subdomain.md)

**Gerenciamento de chaves GPG**

O Painel de controle do campaign agora permite gerar um par de chaves GPG para que você possa decodificar facilmente os dados externos que chegam ao Campaign. Além disso, adicionamos um recurso para que você possa instalar uma chave GPG pública para criptografar os dados ao deixar o Campaign. [Leia mais](instances-settings/using/gpg-keys-management.md)

**Remoção de &#39;Lista branca&#39; / &#39;Lista negra&#39;**

Os termos &quot;lista branca&quot; e &quot;lista negra&quot; foram removidos da documentação do Adobe Campaign. Algumas ocorrências desses termos ainda podem existir na interface do usuário do produto, nomes de opções e código interno, mas serão substituídas em versões futuras da Campanha por &quot;blocklist&quot; e &quot;allowlist&quot;.

**Monitoramento de perfis ativos**

O Painel de controle agora permite que você monitore o número de perfis ativos usados por suas instâncias e contados para fins de cobrança. [Leia mais](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>O monitoramento de perfis ativos pelo Painel de controle está disponível em beta e sujeito a atualizações e modificações frequentes sem aviso prévio.
>
>O recurso está disponível para clientes hospedados no AWS a partir da compilação do Campaign Standard 10368 e da compilação do Campaign Classic 8931. Se estiver usando uma versão anterior, é necessário atualizar para usar esse recurso.

## Maio de 2020 {#may-2020}

**Gerenciamento de certificados para subdomínios CNAME**

O Painel de controle do Campaign agora permite renovar os certificados SSL de seus subdomínios que foram delegados com o método CNAME. [Leia mais](subdomains-certificates/using/renewing-subdomain-certificate.md)

## Abril de 2020 {#april-2020}

**Gerenciamento de registros TXT do Google**

Adicione o registro de verificação do site Google TXT a todos os seus subdomínios usados para enviar emails para endereços Gmail por meio do Painel de controle do Campaign. [Leia mais](subdomains-certificates/using/managing-txt-records.md)

**Monitoramento de espaço de banco de dados**

O Painel de controle do Campaign está equipado com recursos de monitoramento de banco de dados, permitindo visualizar a utilização do espaço do banco de dados sob demanda e ao longo do tempo. [Leia mais](performance-monitoring/using/database-monitoring.md)

**Alerta por email**

O Painel de controle do Campaign está equipado com recursos de email de alerta em tempo real, permitindo que você faça logon no Painel de controle do Campaign e se inscreva para receber alertas quando o sistema estiver em risco de deterioração do desempenho, ou quando uma ação for necessária para garantir alto desempenho no futuro. [Leia mais](performance-monitoring/using/email-alerting.md)

## Janeiro de 2020 {#january-2020}

*22 de janeiro de 2020*

Adicionamos novos recursos para usuários administradores delegarem subdomínios e renovarem certificados SSL pelo Painel de controle do Campaign.

Para obter mais informações, consulte estas páginas:
* [Configurar um novo subdomínio](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Renovar um certificado SSL de subdomínio](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Esses recursos estarão disponíveis na versão beta e estão sujeitos a atualizações e modificações frequentes sem aviso prévio.

## Setembro de 2019 {#september-2019}

*16 de setembro de 2019*

Adicionamos novos recursos para que os usuários administradores adicionem endereços IP à lista de permissões para se conectarem às instâncias de Campaign Classic.
Além disso, os usuários administradores agora podem exibir a lista de instâncias do Campaign Classic e a qualificação para atualizações de builds.

Para obter mais informações, consulte a [documentação específica](instances-settings/using/ip-whitelisting-instance-access.md).

## Agosto de 2019 {#august-2019}

Adicionamos novos recursos para que os usuários administradores recebam notificações antes que os certificados SSL de seus domínios expirem. Para obter mais informações, consulte a [documentação detalhada](subdomains-certificates/using/monitoring-ssl-certificates.md).

Além disso, agora os usuários administradores podem excluir chaves SSH que foram adicionadas para acessar os servidores SFTP.

## Julho de 2019 {#july-2019}

Adicionamos novos recursos para potencializar os usuários administradores para que tenham mais controle das configurações de instâncias do Campaign Classic. Os novos recursos do Painel de controle do Campaign incluem a habilidade de adicionar URLs aos quais o Adobe Campaign se conecta para transferir dados/arquivos.

Para obter mais informações, consulte a [documentação detalhada](instances-settings/using/url-permissions.md).
