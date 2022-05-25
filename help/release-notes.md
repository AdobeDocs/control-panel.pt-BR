---
product: campaign
solution: Campaign
title: Versões do Painel de Controle do Campaign
description: Esta página lista todos os novos recursos e melhorias do Painel de controle do Campaign
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: 87b28195ede08756d5084aad36bf1c95f621b5f5
workflow-type: tm+mt
source-wordcount: '1174'
ht-degree: 60%

---

# Versões do Painel de Controle do Campaign {#control-panel-releases}

Esta página lista todos os novos recursos e melhorias do Painel de controle do Campaign.

>[!NOTE]
>
>O Painel de controle do Campaign é acessível somente para usuários administradores. Saiba mais sobre permissões em [esta seção](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=pt-BR#discover-control-panel).
>
>Para o Campaign v7, sua instância deve ser hospedada no Amazon Web Services (AWS) e atualizada para a mais recente [Build estável da campanha](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=pt-BR#rn-statuses) (ou para build 9032 ou superior). Saiba como verificar a versão [nesta seção](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=pt-BR#getting-your-campaign-version). Para verificar se sua instância está hospedada no AWS, siga as etapas detalhadas [nesta página](faq.md#hosted-aws).

## Maio de 2022 {#may-2022}

<table>
<thead>
<tr>
<th><strong>Disponibilidade do Painel de controle do Campaign para o modelo de hospedagem híbrida</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Painel de controle do Campaign agora está disponível para clientes com modelo de hospedagem híbrida. Esses clientes podem aproveitar os recursos do Painel de controle do Campaign fornecendo o URL da instância MID/RT configurado em sua instância de marketing no Painel de controle do Campaign.</p><p>Para obter mais informações, consulte a <a href="instances-settings/using/external-accounts.md">documentação detalhada.</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Atualizações de monitoramento de throughs e latências</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os recursos de monitoramento de throughput e latências foram aprimorados:<ul><li>Agora é possível identificar as IDs dos 5 deliveries principais que estão contribuindo para a taxa de transferência da sua instância.</li><li>Clientes Campaign Classic v7/v8 agora podem visualizar a latência de um canal específico.</p></li><p>Para obter mais informações, consulte a <a href="performance-monitoring/using/thoughputs-latencies.md">documentação detalhada.</a></p>
</td>
</tr>
</tbody>
</table>


## Abril de 2022 {#april-2022}

<table>
<thead>
<tr>
<th><strong>Monitore contatos importantes e eventos em suas instâncias</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode monitorar versões e revisões de serviços anteriores e futuras em suas instâncias, bem como acessar uma lista de contatos importantes na Adobe para qualquer solicitação ou problema.</p><p>Para obter mais informações, consulte a <a href="service-events/service-events.md">documentação detalhada.</a></p>
</td>
</tr>
</tbody>
</table>

## Março de 2022 {#march-2022}

<table>
<thead>
<tr>
<th><strong>Throughput e disponibilidade de monitoramento de latência</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O monitoramento de throughput e latência agora está disponível para todos os clientes do Campaign Standard e v8, e para clientes do Campaign V7 com números de compilação 9032,9330, 9346 ou 9349 que têm implantações independentes (sem qualquer instância mid).</p><p>Para obter mais informações, consulte a <a href="performance-monitoring/using/thoughputs-latencies.md">documentação detalhada.</a></p>
</td>
</tr>
</tbody>
</table>

## Fevereiro de 2022 {#february-2022}

<table>
<thead>
<tr>
<th><strong>Monitoramento de parâmetros de fluxo de trabalho</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível monitorar parâmetros de fluxo de trabalho que podem exigir atenção específica para evitar problemas em suas instâncias. </p><p>Para obter mais informações, consulte a <a href="performance-monitoring/using/workflow-monitoring.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

## Janeiro de 2022 {#january-2022}

<table>
<thead>
<tr>
<th><strong>Monitoramento de consultas ativas</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Painel de controle do Campaign agora permite monitorar as consultas que estão sendo executadas há mais tempo em suas instâncias.</p><p>Para obter mais informações, consulte a <a href="performance-monitoring/using/database-active-queries.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoramento de taxas de transferência e latência</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora, é possível monitorar a tendência das taxas de transferência e latência de entrega ao longo de um período em suas instâncias.</p><p>Para obter mais informações, consulte a <a href="performance-monitoring/using/thoughputs-latencies.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Operações de certificados SSL em novos subdomínios</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As operações de certificados SSL agora podem ser executadas em um subdomínio recém-configurado, mesmo se a auditoria de deliverability ainda estiver em andamento.</p><p>Para obter mais informações, consulte a <a href="subdomains-certificates/using/renewing-subdomain-certificate.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

## Outubro de 2021 {#october-2021}

<table>
<thead>
<tr>
<th><strong>Intervalo IP e período de validade da chave pública</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível definir uma duração para a disponibilidade de intervalos IP e chaves públicas. </p><p>Para obter mais informações, consulte <a href="sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list">Lista de permissões de intervalo IP</a> e <a href="sftp/using/key-management.md#installing-ssh-key">Gerenciamento de chaves</a> seções.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Intervalo IP e edição de chave pública</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível editar a variável <a href="sftp/using/ip-range-allow-listing.md#editing-ip-ranges">Intervalos de IP</a> e <a href="sftp/using/key-management.md#editing-public-keys">chaves públicas</a> que você criar. Observe que esse recurso não está disponível para os itens criados antes da versão atual do Painel de controle do Campaign.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Alertas no intervalo IP SFTP e expiração da chave pública</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A funcionalidade de alerta por email agora inclui alertas sobre IP SFTP, permitindo listar a expiração e a expiração da chave pública SFTP.</p><p>Para obter mais informações, consulte a <a href="performance-monitoring/using/email-alerting.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Suporte total com o Campaign v8</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O <strong>Subdomínio</strong> e <strong>Certificado</strong> Os recursos de gerenciamento agora são suportados pelo Painel de controle do Campaign no Adobe Campaign v8.</a>.</p>
</td>
</tr>
</tbody>
</table>

## Agosto de 2021 {#august-2021}

<table>
<thead>
<tr>
<th><strong>Suporte com o Campaign v8</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Painel de controle do Campaign agora está disponível para Adobe Campaign v8, exceto o <strong>Subdomínio</strong> e <strong>Certificado</strong> recursos de gerenciamento, que ainda não são compatíveis.</p><p>Para obter mais informações, consulte <a href="https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html" target="blank">Documentação do Campaign v8</a>.</p>
</td>
</tr>
</tbody>
</table>

## Outubro de 2020 {#october-2020}

<table>
<thead>
<tr>
<th><strong>Configuração de subdomínio usando CNAMEs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora o Painel de Controle do Campaign permite configurar um subdomínio para funcionar com a Adobe usando CNAMEs diretamente da interface.</p><p>Para obter mais informações, consulte a <a href="subdomains-certificates/using/setting-up-new-subdomain.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Melhorias no monitoramento de banco de dados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O monitoramento de banco de dados foi aprimorado com métricas adicionais que permitem obter informações detalhadas sobre os recursos que estão consumindo espaço no banco de dados.</p><p>Para obter mais informações, consulte a <a href="performance-monitoring/using/database-monitoring.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

## Junho de 2020 {#june-2020}

<table>
<thead>
<tr>
<th><strong>Auditoria de entrega de subdomínio</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Após delegar um novo subdomínio, o Painel de controle do Campaign agora permite rastrear a auditoria feita pela equipe de avaliação do delivery.</p><p>Para obter mais informações, consulte a <a href="subdomains-certificates/using/setting-up-new-subdomain.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gerenciamento de chaves GPG</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Painel de controle do campaign agora permite gerar um par de chaves GPG para que você possa decodificar facilmente os dados externos que chegam ao Campaign. Além disso, adicionamos um recurso para que você possa instalar uma chave GPG pública para criptografar os dados ao deixar o Campaign.</p><p>Para obter mais informações, consulte a <a href="instances-settings/using/gpg-keys-management.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoramento de perfis ativos</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Painel de controle do Campaign agora permite monitorar o número de perfis ativos usados por suas instâncias e contados para fins de faturamento.</p><p>Para obter mais informações, consulte a <a href="performance-monitoring/using/active-profiles-monitoring.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

>[!IMPORTANT]
>
>O monitoramento de perfis ativos pelo Painel de controle do Campaign está disponível em beta e está sujeito a atualizações e modificações frequentes sem aviso prévio.

## Maio de 2020 {#may-2020}

<table>
<thead>
<tr>
<th><strong>Gerenciamento de certificados para subdomínios CNAME</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora o Painel de Controle do Campaign permite renovar os certificados SSL de seus subdomínios que foram delegados com o método CNAME.</p><p>Para obter mais informações, consulte a <a href="subdomains-certificates/using/renewing-subdomain-certificate.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

## Abril de 2020 {#april-2020}

<table>
<thead>
<tr>
<th><strong>Gerenciamento de registros TXT do Google</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adicione o registro de verificação do site Google TXT a todos os seus subdomínios usados para enviar emails para endereços Gmail por meio do Painel de controle do Campaign.</p><p>Para obter mais informações, consulte a <a href="subdomains-certificates/using/managing-txt-records.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Monitoramento de espaço de banco de dados</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Painel de controle do Campaign está equipado com recursos de monitoramento de banco de dados, permitindo visualizar a utilização do espaço do banco de dados sob demanda e ao longo do tempo.</p><p>Para obter mais informações, consulte a <a href="performance-monitoring/using/database-monitoring.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Alerta por email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Painel de controle do Campaign está equipado com recursos de email de alerta em tempo real, permitindo que você faça logon no Painel de controle do Campaign e se inscreva para receber alertas quando o sistema estiver em risco de deterioração do desempenho, ou quando uma ação for necessária para garantir alto desempenho no futuro.</p><p>Para obter mais informações, consulte a <a href="performance-monitoring/using/email-alerting.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>

## Janeiro de 2020 {#january-2020}

Adicionamos novos recursos para usuários administradores delegarem subdomínios e renovarem certificados SSL pelo Painel de Controle do Campaign.

Para obter mais informações, consulte estas páginas:
* [Configurar um novo subdomínio](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Renovar um certificado SSL de subdomínio](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Esses recursos estarão disponíveis na versão beta e estão sujeitos a atualizações e modificações frequentes sem aviso prévio.

## Setembro de 2019 {#september-2019}

Adicionamos novos recursos para que os usuários administradores adicionem endereços IP à lista de permissões para se conectarem às instâncias do Campaign v7/v8.
Além disso, os usuários administradores agora podem exibir a lista de instâncias do Campaign v7/v8 e a qualificação para atualizações de builds.

Para obter mais informações, consulte a [documentação específica](instances-settings/using/ip-allow-listing-instance-access.md).

## Agosto de 2019 {#august-2019}

Adicionamos novos recursos para que os usuários administradores recebam notificações antes que os certificados SSL de seus domínios expirem. Para obter mais informações, consulte a [documentação detalhada](subdomains-certificates/using/monitoring-ssl-certificates.md).

Além disso, agora os usuários administradores podem excluir chaves SSH que foram adicionadas para acessar os servidores SFTP.

## Julho de 2019 {#july-2019}

Adicionamos novos recursos para potencializar os usuários administradores para que tenham mais controle das configurações de instância do Campaign v7/v8. Os novos recursos do Painel de controle do Campaign incluem a habilidade de adicionar URLs aos quais o Adobe Campaign se conecta para transferir dados/arquivos.

Para obter mais informações, consulte a [documentação detalhada](instances-settings/using/url-permissions.md).
