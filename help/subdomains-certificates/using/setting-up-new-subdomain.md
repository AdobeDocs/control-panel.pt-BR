---
title: Configurar um novo subdomínio
description: Saiba como configurar um novo subdomínio para instâncias do Campaign
translation-type: tm+mt
source-git-commit: c215836129487530e50398ca1454895a2f319867
workflow-type: tm+mt
source-wordcount: '1098'
ht-degree: 50%

---


# Configurar um novo subdomínio {#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id="cp_subdomain_management"
>title="Configurar novos subdomínios e gerenciar certificados"
>abstract="É necessário configurar um novo subdomínio e gerenciar os certificados SSL dos subdomínios para iniciar a enviar emails ou publicar páginas de aterrissagem com o Adobe Campaign."
>additional-url="https://docs.adobe.com/content/help/pt-BR/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="Como monitorar os certificados SSL de subdomínios"

>[!IMPORTANT]
>
>A configuração de subdomínio do Painel de controle do Campaign está disponível em beta e sujeita a atualizações e modificações frequentes sem aviso prévio.

Esta página fornece informações sobre como configurar novos subdomínios usando delegação de subdomínio completa ou CNAMEs. Os conceitos globais sobre estes dois métodos são apresentados nesta seção: [](../../subdomains-certificates/using/subdomains-branding.md).

**Tópicos relacionados:**

* [Delegar subdomínios (vídeo tutorial)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [Configurar subdomínios usando CNAMEs](https://docs.adobe.com/content/help/en/campaign-classic-learn/control-panel/subdomains-and-certificates/delegating-subdomains-using-cname.html)
* [Monitorar subdomínios](../../subdomains-certificates/using/monitoring-subdomains.md)

## Leitura obrigatória {#must-read}

### Seleção da instância

Subdomain configuration is available for **production** instances only.

Se a instância selecionada no assistente não tiver subdomínios configurados anteriormente, o primeiro subdomínio configurado se tornará o subdomínio **** primário dessa instância e você não poderá alterá-lo no futuro.

Como resultado, os registros **DNS** reversos serão criados para outros subdomínios que usam esse subdomínio primário. **Endereços de resposta e de rejeição para outros subdomínios serão gerados a partir do subdomínio primário.**

### Configuração de servidores de nomes

Ao configurar servidores de nomes, **nunca delegue o subdomínio raiz à Adobe**. Caso contrário, o domínio poderá trabalhar somente com a Adobe. Qualquer outro uso será impossível, como por exemplo, enviar emails internos aos funcionários de sua organização.

Além disso, **não crie um arquivo de zona separado** para esse novo subdomínio.

## Delegação de subdomínio completa {#full-subdomain-delegation}

Para delegar completamente um subdomínio ao Adobe Campaign, siga estas etapas:

1. No cartão **[!UICONTROL Subdomains & Certificates]**, selecione a instância de produção desejada e clique em **[!UICONTROL Setup new subdomain]**.

   ![](assets/subdomain1.png)

1. Clique em **[!UICONTROL Next]** para confirmar o método de delegação completo.

   ![](assets/subdomain3.png)

1. Crie o subdomínio e os servidores de nomes desejados na solução de hospedagem usada por sua organização. Para fazer isso, copie e cole as informações do Servidor de nomes da Adobe exibidas no assistente. Para obter mais informações sobre como criar um subdomínio em uma solução de hospedagem, consulte o [vídeo tutorial](https://video.tv.adobe.com/v/30175?captions=por_br).

   ![](assets/subdomain4.png)

1. Depois que o subdomínio for criado com as informações correspondentes do servidor de nomes da Adobe, clique em **[!UICONTROL Next]**.

1. Se você selecionou uma instância Campaign Classic, selecione o caso de uso desejado para o subdomínio: **Comunicações** de marketing ou comunicações **transacionais e operacionais**. Os conceitos globais sobre casos de uso de subdomínios são apresentados [nesta seção](../../subdomains-certificates/using/subdomains-branding.md#about-subdomains-use-cases).

   ![](assets/subdomain5.png)

1. Digite o subdomínio que você criou na solução de hospedagem e clique em **[!UICONTROL Submit]**.

   Preencha o **nome completo** do subdomínio que será delegado. Por exemplo, para delegar o subdomínio &quot;usoffer.email.weretail.com&quot;, digite &quot;usoffer.email.weretail.com&quot;.

   ![](assets/subdomain6.png)

Depois que o subdomínio for enviado, várias verificações e etapas de configuração serão executadas pelo Painel de controle do Campaign. Para obter mais informações, consulte [](../../subdomains-certificates/using/setting-up-new-subdomain.md#subdomain-verify-and-configuration).

## Configuração de subdomínio usando CNAMEs {#use-cnames}

Para configurar um subdomínio usando CNAMEs, siga estas etapas:

1. No cartão **[!UICONTROL Subdomains & Certificates]**, selecione a instância de produção desejada e clique em **[!UICONTROL Setup new subdomain]**.

   ![](assets/subdomain1.png)

1. Select the **[!UICONTROL CNAME]** method, then click **[!UICONTROL Next]**.

   ![](assets/cname-method-selection.png)

1. Se você selecionou uma instância Campaign Classic, selecione o caso de uso desejado para o subdomínio: **Comunicações** de marketing ou comunicações **transacionais e operacionais**. Os conceitos globais sobre casos de uso de subdomínios são apresentados [nesta seção](../../subdomains-certificates/using/subdomains-branding.md#about-subdomains-use-cases).

   ![](assets/cname-use-case.png)

1. Digite o subdomínio que você criou na solução de hospedagem e clique em **[!UICONTROL Next]**.

   Make sure you fill in the **full name** of the subdomain to setup. Por exemplo, para configurar o subdomínio &quot;usoffer.email.weretail.com&quot;, digite &quot;usoffer.email.weretail.com&quot;.

   ![](assets/cname-submit.png)

1. A lista de registros a serem colocados em seus servidores DNS é exibida. Copie esses registros, um por um, ou baixando um arquivo CSV e, em seguida, navegue até sua solução de hospedagem de domínio para gerar os registros DNS correspondentes.

   ![](assets/cname-generate-record.png)

1. Verifique se todos os registros de DNS de etapas anteriores foram gerados na solução de hospedagem de domínio. Se tudo estiver configurado corretamente, selecione a primeira instrução e clique **[!UICONTROL Submit]** para confirmar.

   ![](assets/cname-confirmation.png)

   >[!NOTE]
   >
   >Se desejar criar os registros e enviar a configuração do subdomínio posteriormente, selecione a segunda instrução e clique em **[!UICONTROL Submit later]**. Você poderá retomar a configuração do subdomínio diretamente da área de tela do gerenciamento de subdomínio **[!UICONTROL Processing]** .
   >
   >Observe que os registros de DNS a serem colocados em seu servidor serão mantidos por Painel de controle do Campaign 30 dias. Além desse período, será necessário configurar o subdomínio do zero.

Depois que o subdomínio for enviado, várias verificações e etapas de configuração serão executadas pelo Painel de controle do Campaign. Para obter mais informações, consulte [](../../subdomains-certificates/using/setting-up-new-subdomain.md#subdomain-checks-and-configuration).

## Verificações e configuração do subdomínio {#subdomain-checks-and-configuration}

1. Depois que um subdomínio for submetido, o Painel de controle do Campaign verificará se ele aponta corretamente para os registros Adobe NS e se o registro do Start da Autoridade (SOA) não existe para esse subdomínio.

   >[!NOTE]
   >
   >Observe que, enquanto a configuração do subdomínio for executada, outras solicitações por meio do Painel de controle do Campaign serão inseridas em uma fila e executadas somente após a conclusão da configuração do subdomínio, para evitar problemas de desempenho.

1. Se as verificações forem bem-sucedidas, o Painel de controle do Campaign começará a configurar o subdomínio com registros DNS, URLs adicionais, caixas de entrada, etc.

   ![](assets/subdomain7.png)

   You can get more details on the configuration progress by clicking the subdomain configuration **[!UICONTROL Details]** button.

   ![](assets/subdomain_audit.png)

1. Eventualmente, a **Equipe de avaliação do delivery** será notificada sobre o novo subdomínio para fazer a auditoria. O processo de auditoria pode levar até 10 dias úteis após a configuração do subdomínio.

   >[!IMPORTANT]
   >
   >As verificações de entrega realizadas incluem loops de feedback e testes de loops de reclamação de spam. Portanto, não recomendamos a utilização do subdomínio antes da conclusão da auditoria, uma vez que poderá resultar em uma má reputação do subdomínio.

1. No final do processo, os subdomínios serão configurados para funcionar com a instância do Adobe Campaign e os elementos abaixo serão criados:

   * **O subdomínio com os seguintes registros DNS**: SOA, MX, CNAME(s), DKIM, SPF, TXT,
   * **Subdomínios adicionais** para hospedar mirror, recursos, páginas de rastreamento e chave de domínio,
   * **Caixas de entrada**: Remetente, Erro, Responder para.

   Por padrão, a caixa de entrada &quot;Responder para&quot; no Painel de controle do Campaign está configurada para apagar emails e não é revisável. Se quiser monitorar a caixa de entrada “Responder para” para suas campanhas de marketing, não use este endereço.

Para obter mais detalhes sobre o subdomínio, clique nos botões **[!UICONTROL Subdomain details]** e **[!UICONTROL Sender info]**.

![](assets/detail_buttons.png)

![](assets/subdomain_details.png)

![](assets/sender_info.png)

## Solução de problemas {#troubleshooting}

* Em alguns casos, a configuração do subdomínio passa, mas o subdomínio pode não ser verificado com êxito. O subdomínio permanecerá na **[!UICONTROL Configured]** lista com um log de trabalho que fornece informações sobre o erro. Entre em contato com o Atendimento ao cliente se tiver dificuldades para resolver o problema.
* Se o subdomínio estiver sendo exibido como &quot;Não verificado&quot; após a configuração, inicie uma nova verificação de subdomínio (**...** / **[!UICONTROL Verify subdomain]**). Se ainda mostrar o mesmo status, o motivo pode ser que haja alguma personalização feita no schema de recipients, que não pode ser verificada usando processos padrão. Tente enviar uma campanha com esse subdomínio.
* Se a configuração do subdomínio estiver demorando muito (mais de 10 dias úteis) na etapa de auditoria de entrega, entre em contato com o Atendimento ao cliente.
