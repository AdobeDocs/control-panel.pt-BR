---
title: Notas de versão de 2022
description: Esta página lista todas as versões de 2022 do Painel de controle do Campaign.
exl-id: 9fb18bb6-c4e4-48aa-849c-d9129add5266
source-git-commit: 95390bb1f8af21907ce8984279a6a73dd7828b00
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 100%

---

# Notas de versão de 2022 {#rn-2022}

## Setembro de 2022 {#september-2022}

Os clientes com modelo de hospedagem híbrida agora podem configurar novos subdomínios. [Saiba mais](../subdomains-certificates/using/setting-up-new-subdomain.md)

## Agosto de 2022 {#august-2022}

* Os clientes com modelo de hospedagem híbrida agora podem verificar seus subdomínios. [Saiba mais](../subdomains-certificates/using/monitoring-subdomains.md)
* O campo Unidade da organização (OU) agora é opcional na Solicitação de geração de certificado (CSR). [Saiba mais](../subdomains-certificates/using/renewing-subdomain-certificate.md)

## Julho de 2022 {#july-2022}

<table>
<thead>
<tr>
<th><strong>Instalação de certificados de subdomínios para modelo de hospedagem híbrido</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><p>Os clientes com modelo de hospedagem híbrida agora podem renovar os certificados SSL dos subdomínios pelo Painel de controle do Campaign.</p><p>Para obter mais informações, consulte a <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">documentação detalhada.</a></p>
</td>
</tr>
</tbody>
</table>

## Junho de 2022 {#june-2022}

### Novidades

<table>
<thead>
<tr>
<th><strong>Os 10 arquivos que consomem mais espaço em servidores SFTP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora é possível identificar os 10 arquivos que consomem mais espaço em um servidor SFTP. <a href="../sftp/using/sftp-storage-management.md">Saiba mais</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Lembretes do calendário de serviço</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O Calendário de serviço agora permite que você defina lembretes para ser notificado por email antes que um evento ocorra em suas instâncias. <a href="../service-events/service-events.md">Saiba mais</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aprimoramentos na geração de CSR de subdomínios</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Foram feitos vários aprimoramentos no processo de geração de CSR. <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">Saiba mais</a></p><ul><li>Ao gerar uma CSR, agora você pode selecionar um dos subdomínios incluídos como o Nome comum.</li><li>Agora você pode copiar o resumo da CSR antes de gerá-la.</li><li>Depois que uma CSR é gerada, você pode baixá-la novamente nos logs do processo. Esse recurso não se aplica a certificados gerados antes desta versão.</li></ul><p>

</td>
</tr>
</tbody>
</table>

### Aprimoramentos

**Configurações de instâncias**

* O número máximo de chaves GPG no Painel de controle do Campaign foi aumentado para 60 chaves. [Saiba mais](../instances-settings/using/gpg-keys-management.md)

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
<p>O Painel de controle do Campaign agora está disponível para clientes com modelo de hospedagem híbrida. Esses clientes podem aproveitar os recursos do Painel de controle do Campaign ao fornecerem o URL da instância MID/RT configurado em sua instância de marketing do Painel de controle.</p><p>Para obter mais informações, consulte a <a href="../instances-settings/using/external-accounts.md">documentação detalhada.</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Atualizações do monitoramento de taxas de transferências e latências</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Os recursos de monitoramento de taxas de transferência e latências foram aprimorados:<ul><li>Agora, é possível identificar as IDs das 5 principais entregas que estão contribuindo para a taxa de transferência da instância.</li><li>Agora, clientes do Campaign Classic v7/v8 podem visualizar a latência de um canal específico.</p></li><p>Para obter mais informações, consulte a <a href="../performance-monitoring/using/thoughputs-latencies.md">documentação detalhada.</a></p>
</td>
</tr>
</tbody>
</table>


## Abril de 2022 {#april-2022}

<table>
<thead>
<tr>
<th><strong>Monitore contatos e eventos importantes em suas instâncias</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Agora você pode monitorar versões e revisões de serviços anteriores e futuras em suas instâncias, bem como acessar uma lista de contatos importantes na Adobe para qualquer solicitação ou problema.</p><p>Para obter mais informações, consulte a <a href="../service-events/service-events.md">documentação detalhada.</a></p>
</td>
</tr>
</tbody>
</table>

## Março de 2022 {#march-2022}

<table>
<thead>
<tr>
<th><strong>Disponibilidade de monitoramento de taxas de transferência e latência</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>O monitoramento de taxas de transferência e latência agora está disponível para todos os clientes do Campaign Standard e v8 e para clientes do Campaign V7 com números de build 9032, 9330, 9346 ou 9349 que têm implantações independentes (sem nenhuma instância intermediária).</p><p>Para obter mais informações, consulte a <a href="../performance-monitoring/using/thoughputs-latencies.md">documentação detalhada.</a></p>
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
<p>Agora é possível monitorar parâmetros de fluxo de trabalho que podem exigir atenção específica para evitar problemas em suas instâncias. </p><p>Para obter mais informações, consulte a <a href="../performance-monitoring/using/workflow-monitoring.md">documentação detalhada</a>.</p>
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
<p>O Painel de controle do Campaign agora permite monitorar as consultas que estão sendo executadas há mais tempo em suas instâncias.</p><p>Para obter mais informações, consulte a <a href="../performance-monitoring/using/database-active-queries.md">documentação detalhada</a>.</p>
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
<p>Agora é possível monitorar a tendência das taxas de transferência e latência de entrega ao longo de um período em suas instâncias.</p><p>Para obter mais informações, consulte a <a href="../performance-monitoring/using/thoughputs-latencies.md">documentação detalhada</a>.</p>
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
<p>As operações de certificados SSL agora podem ser executadas em um subdomínio recém-configurado, mesmo se a auditoria de entrega ainda estiver em andamento.</p><p>Para obter mais informações, consulte a <a href="../subdomains-certificates/using/renewing-subdomain-certificate.md">documentação detalhada</a>.</p>
</td>
</tr>
</tbody>
</table>
