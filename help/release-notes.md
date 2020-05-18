---
title: Versões do Painel de controle
translation-type: tm+mt
source-git-commit: 49d84c42446ed1fc996b9d57005565b15ca24e77
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 29%

---


# Control Panel releases {#control-panel-releases}

Aqui você encontrará informações sobre as versões mais recentes do Painel de controle.

>[!NOTE]
>
>Observe que o Painel de controle está disponível somente para clientes hospedados no AWS, exceto para ambientes híbridos que ainda não são suportados. Nenhuma atualização é necessária para acessar o Painel de controle. Você deve ser um usuário administrador para acessá-la.

## Maio de 2020 (#may-2020)

**Gerenciamento de chaves GPG**

O Painel de controle agora permite que você gere um par de chaves GPG, para que você possa decodificar facilmente os dados que chegam à Campanha de fora. Além disso, adicionamos um recurso para que você possa instalar uma chave GPG pública para criptografar dados deixando a Campanha. [Leia mais](instances-settings/using/gpg-keys-management.md)

**Gerenciamento de certificados para subdomínios CNAME**

O Painel de controle agora permite que você renove os certificados SSL de seus subdomínios que foram delegados com o método CNAME. [Leia mais](subdomains-certificates/using/renewing-subdomain-certificate.md)

## Abril de 2020 {#april-2020}

**Gerenciamento de registros TXT do Google**

Adicione o registro de verificação do site Google TXT a todos os seus subdomínios usados para enviar emails para endereços Gmail por meio do Painel de controle de Campanha. [Leia mais](subdomains-certificates/using/managing-txt-records.md)

**Monitoramento do espaço do banco de dados**

O Painel de Controle de Campanha está equipado com recursos de monitoramento de banco de dados, permitindo que você visualização a utilização do espaço do banco de dados sob demanda e ao longo do tempo. [Leia mais](performance-monitoring/using/database-monitoring.md)

**Alerta por email**

O Painel de controle de Campanha está equipado com recursos de e-mail de alerta em tempo real, permitindo que você faça logon no Painel de controle e se inscreva para receber alertas quando o sistema estiver em risco de deterioração do desempenho, ou quando uma ação for necessária para garantir alto desempenho no futuro. [Leia mais](performance-monitoring/using/email-alerting.md)

## Janeiro de 2020 {#january-2020}

*22 de janeiro de 2020*

Adicionamos novos recursos para usuários administradores delegarem subdomínios e renovarem certificados SSL do Painel de controle.

Para obter mais informações, consulte estas páginas:
* [Configurar um novo subdomínio](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Renovando um certificado SSL de subdomínio](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Esses recursos estarão disponíveis na versão beta e estão sujeitos a atualizações e modificações frequentes sem aviso prévio.

## Setembro de 2019 {#september-2019}

*16 de setembro de 2019*

Adicionamos novos recursos para os usuários Administradores na lista de permissões de endereços IP para se conectar às instâncias do Campaign Classic.
Além disso, os usuários administradores agora podem visualização a lista de instâncias de Campaign Classic e a qualificação para atualizações de criação.

Para obter mais informações, consulte a [documentação dedicada](instances-settings/using/ip-whitelisting-instance-access.md).

## Agosto de 2019 {#august-2019}

Adicionamos novos recursos para que os usuários administradores recebam notificações antes que os certificados SSL de seus domínios expirem. Para obter mais informações, consulte a [documentação detalhada](subdomains-certificates/using/monitoring-ssl-certificates.md).

Além disso, agora os usuários administradores podem excluir chaves SSH que foram adicionadas para acessar os servidores SFTP.

## Julho de 2019 {#july-2019}

Adicionamos novos recursos para capacitar os usuários administradores a assumir maior controle das configurações de instância do Campaign Classic. Os novos recursos do Painel de controle incluem a habilidade de adicionar URLs aos quais o Adobe Campaign se conecta para transferência de dados/arquivos.

Para obter mais informações, consulte a [documentação detalhada](instances-settings/using/url-permissions.md).
