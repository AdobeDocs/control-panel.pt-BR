---
product: campaign
solution: Campaign
title: Adicionar registros DMARC
description: Saiba como adicionar um registro DMARC para um subdomínio.
feature: Control Panel
role: Architect
level: Experienced
exl-id: 2ca66983-5beb-495a-9639-a31905500cff
source-git-commit: 64ea5e26786eea107983ee5025025c81334b0a91
workflow-type: tm+mt
source-wordcount: '714'
ht-degree: 0%

---

# Adicionar registros DMARC {#dmarc}

## Sobre registros DMARC {#about}

O DMARC (Domain Based Message Authentication, Reporting and Conformance) é um protocolo padrão de autenticação de email que ajuda as organizações a proteger seus domínios de email contra ataques de phishing e de falsificação. Ele permite decidir como um provedor de caixa de correio deve lidar com emails que não passam nas verificações SPF e DKIM, fornecendo uma maneira de autenticar o domínio do remetente e impedir o uso não autorizado do domínio para fins mal-intencionados.

Informações detalhadas sobre a implementação do DMARC estão disponíveis em [Guia de práticas recomendadas de capacidade de delivery do Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-dmarc.html)

## Limitações e pré-requisitos {#limitations}

* Os registros SPF e DKIM são pré-requisitos para criar um registro DMARC.
* Os registros DMARC só podem ser adicionados a subdomínios usando a delegação de subdomínio completa. [Saiba mais sobre métodos de configuração de subdomínios](subdomains-branding.md#subdomain-delegation-methods)

## Adicionar um registro DMARC para um subdomínio {#add}

Para adicionar um registro DMARC para um subdomínio, siga estas etapas:

1. Na lista de subdomínios, clique no botão de reticências ao lado do subdomínio desejado e selecione **[!UICONTROL Subdomain details]**.

1. Clique em **[!UICONTROL Add TXT record]** e escolha **[!UICONTROL DMARC]** do **[!UICONTROL Record Type]** lista suspensa.

   ![](assets/dmarc-add.png)

1. Escolha o **[!UICONTROL Policy Type]** que o servidor do recipient deve seguir quando um de seus emails falhar. Os tipos de política disponíveis são:

   * **[!UICONTROL None]**,
   * **[!UICONTROL Quarantine]** (posicionamento da pasta de spam),
   * **[!UICONTROL Reject]** (bloquear o email).

   Como prática recomendada, é recomendável implantar lentamente a implementação DMARC escalando sua política DMARC de p=none, para p=quarantine, para p=reject à medida que você obtém a compreensão DMARC do impacto potencial da DMARC.

   * **Etapa 1:** Analise o feedback que você recebe e usa (p=none), que instrui o destinatário a não executar nenhuma ação em relação às mensagens com falha de autenticação, mas ainda enviar relatórios de email ao remetente. Além disso, revise e corrija problemas com o SPF/DKIM se as mensagens legítimas estiverem falhando na autenticação.

   * **Etapa 2:** Determine se o SPF e o DKIM estão alinhados e transmitem a autenticação para todos os emails legítimos e, em seguida, mova a política para (p=quarentena), que instrui o servidor de email de recebimento a colocar em quarentena os emails que falham na autenticação (geralmente significa colocar essas mensagens na pasta de spam). Se a política estiver definida como quarentena, recomenda-se que você comece com uma pequena porcentagem de seus emails.

   * **Etapa 3:** Ajuste a política para (p=reject). OBSERVAÇÃO: use essa política com cuidado e determine se é apropriada para sua organização. A política p= reject informa ao destinatário para negar completamente (retornar) qualquer email para o domínio que não é autenticado. Com essa política ativada, somente os emails verificados como 100% autenticados pelo seu domínio terão uma chance de inserção na Caixa de entrada.

   >[!NOTE]
   >
   > A criação do registro BIMI não está disponível com um tipo de política de registro DMARC definido como &quot;Nenhum&quot;.

1. Preencha os endereços de email que devem receber os relatórios DMARC. Quando um de seus emails falhar, os relatórios DMARC são enviados automaticamente para o endereço de email de sua escolha:

   * Os relatórios DMARC agregados fornecem informações de alto nível, como, por exemplo, o número de emails que falharam em um determinado período.
   * Os relatórios de falha DMARC do Forensic fornecem informações detalhadas, como por exemplo, de qual endereço IP o email com falha se origina.

1. Se a política DMARC estiver definida como &quot;Nenhum&quot;, insira uma porcentagem que se aplique a 100% dos emails.

   Se a política estiver definida como &quot;Rejeitar&quot; ou &quot;Quarentena&quot;, recomenda-se que você comece com uma pequena porcentagem de seus emails. À medida que mais emails do seu domínio passam na autenticação com servidores receptores, atualize seu registro lentamente com uma porcentagem maior.

   >[!NOTE]
   >
   >Se o domínio usar BIMI, a política DMARC deverá ter um valor de porcentagem de 100%. O BIMI não é compatível com políticas DMARC com esse valor definido como menos de 100%.

   ![](assets/dmarc-add2.png)

1. Os relatórios DMARC são enviados a cada 24 horas. É possível alterar a frequência de envio dos relatórios no **[!UICONTROL Reporting Interval]** campo. O intervalo mínimo autorizado é de 1 hora, enquanto o valor máximo autorizado é de 2190 horas (ou seja, 3 meses).

1. No **SPF** e **[!UICONTROL DKIM Identifier Alignment]** , especifique a rigidez dos servidores de recipients ao verificar autenticações SPF e DKIM para um email.

   * **[!UICONTROL Relaxed]** mode: o servidor aceita autenticação mesmo se o email for enviado de um subdomínio,
   * **[!UICONTROL Strict]** O modo aceita autenticação somente quando o domínio remetente corresponde exatamente a um domínio SPF e DKIM.

   Digamos que estamos trabalhando com o `http://www.luma.com` domínio. No modo &quot;Relaxado&quot;, os emails provenientes da `marketing.luma.com` O subdomínio será autorizado pelo servidor, enquanto será rejeitado no modo &quot;Estrito&quot;.

1. Clique em **[!UICONTROL Add]** para confirmar a criação do registro DMARC.

Depois que a criação do registro DMARC é processada (aproximadamente 5 minutos), ela é exibida na tela de detalhes dos subdomínios. [Saiba como monitorar registros TXT para seus subdomínios](gs-txt-records.md#monitor)
