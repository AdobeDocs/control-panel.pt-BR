---
title: Configurar um novo subdomínio
description: Saiba como configurar um novo subdomínio para instâncias do Campaign
translation-type: ht
source-git-commit: 47b4c6abd7b41a63d881b658849ac985c72656f8
workflow-type: ht
source-wordcount: '932'
ht-degree: 100%

---


# Configurar um novo subdomínio {#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id="cp_subdomain_management"
>title="Configurar novos subdomínios e gerenciar certificados"
>abstract="É necessário configurar um novo subdomínio e gerenciar os certificados SSL dos subdomínios para iniciar a enviar emails ou publicar páginas de aterrissagem com o Adobe Campaign."
>additional-url="https://docs.adobe.com/content/help/pt-BR/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="Como monitorar os certificados SSL de subdomínios"

>[!IMPORTANT]
>
>A delegação de subdomínios pelo Painel de controle do Campaign está disponível em beta e está sujeita a atualizações e modificações frequentes sem aviso prévio.

## Delegação de subdomínio completa {#full-subdomain-delegation}

O Painel de controle do Campaign permite delegar um subdomínio totalmente para o Adobe Campaign. Para fazer isso, siga as etapas abaixo.

>[!NOTE]
>
>Se a instância selecionada não tiver subdomínios configurados anteriormente, o primeiro subdomínio delegado à Adobe se tornará o **subdomínio primário** dessa instância. Você não poderá alterá-lo no futuro.
>
>Os registros de DNS reverso serão criados para outros subdomínios usando o subdomínio primário. Endereços de resposta e de rejeição para outros subdomínios serão gerados a partir do subdomínio primário.

1. No cartão **[!UICONTROL Subdomains & Certificates]**, selecione a instância de produção desejada e clique em **[!UICONTROL Setup new subdomain]**.

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >A delegação de subdomínio está disponível somente para instâncias de **produção**.

1. Clique em **[!UICONTROL Next]** para confirmar o método de delegação completo.

   ![](assets/subdomain3.png)

   >[!NOTE]
   >
   >No momento, os métodos [CNAME](#use-cnames) e personalizados não são compatíveis com o Painel de controle do Campaign.

1. Crie o subdomínio e os servidores de nomes desejados na solução de hospedagem usada por sua organização. Para fazer isso, copie e cole as informações do Servidor de nomes da Adobe exibidas no assistente. Para obter mais informações sobre como criar um subdomínio em uma solução de hospedagem, consulte o [vídeo tutorial](https://video.tv.adobe.com/v/30175?captions=por_br).

   >[!IMPORTANT]
   >
   >Ao configurar servidores de nomes, **nunca delegue o subdomínio raiz à Adobe**. Caso contrário, o domínio poderá trabalhar somente com a Adobe. Qualquer outro uso será impossível, como por exemplo, enviar emails internos aos funcionários de sua organização.
   >
   >Além disso, **não crie um arquivo de zona separado** para esse novo subdomínio.

   ![](assets/subdomain4.png)

   Depois que o subdomínio for criado com as informações correspondentes do servidor de nomes da Adobe, clique em **[!UICONTROL Next]**.

1. Selecione o caso de uso desejado para o subdomínio:

   * **Comunicações de marketing**: comunicações destinadas a fins comerciais. Exemplo: campanha de email de vendas.
   * **Comunicações transacionais e operacionais**: as comunicações transacionais contêm informações destinadas a concluir um processo que o recipient iniciou com você. Exemplo: confirmação de compra, email de redefinição de senha. As comunicações organizacionais estão relacionadas com o intercâmbio de informações, ideias e visualizações dentro e fora da organização, sem fins comerciais.
   ![](assets/subdomain5.png)

   **Separar os subdomínios de acordo com os casos de uso é uma prática recomendada para o delivery**. A reputação de cada subdomínio é isolada e protegida. Por exemplo, se o subdomínio para comunicações de marketing acabar sendo incluído na blacklist por provedores de serviço de internet, o subdomínio de comunicações transacionais não será afetado e continuará sendo capaz de enviar comunicações.

   **Você pode delegar subdomínios para casos de uso de Marketing e Transacional**:

   * Para casos de uso de Marketing, os subdomínios serão configurados em instâncias **MID** (Mid sourcing).
   * Para casos de uso transacional, os subdomínios serão configurados em TODAS as instâncias **RT** (Centro de mensagens/Mensagens em tempo real) para garantir a conectividade. Os subdomínios operarão, portanto, com todas as instâncias de RT.
   >[!NOTE]
   >
   >Se você estiver usando o Campaign Classic, o Painel de controle permitirá que você veja quais instâncias de RT/MID estão conectadas à instância de Marketing com a qual você está trabalhando. Para obter mais informações, consulte [esta seção](../../instances-settings/using/instance-details.md).

1. Digite o subdomínio que você criou na solução de hospedagem e clique em **[!UICONTROL Submit]**.

   Preencha o **nome completo** do subdomínio que será delegado. Por exemplo, para delegar o subdomínio &quot;usoffer.email.weretail.com&quot;, digite &quot;usoffer.email.weretail.com&quot;.

   ![](assets/subdomain6.png)

1. Depois que o subdomínio for enviado, o Painel de controle do Campaign verificará se ele aponta corretamente para os registros Adobe NS e se o registro de SOA (Start of Authority, Início de Autoridade) não existe para esse subdomínio.

1. Se as verificações forem bem-sucedidas, o Painel de controle do Campaign começará a configurar o subdomínio com registros DNS, URLs adicionais, caixas de entrada, etc. Para obter mais detalhes sobre o progresso da configuração, clique no botão **[!UICONTROL Process details]**.

   ![](assets/subdomain7.png)

   >[!NOTE]
   >
   >Em alguns casos, a delegação prossegue, mas o subdomínio pode não ser verificado com êxito. O subdomínio irá diretamente para a lista **[!UICONTROL Verified subdomains]** com o status **[!UICONTROL Unverified]** e um registro de tarefas fornecendo informações sobre o erro. Entre em contato com o Atendimento ao cliente se tiver dificuldades para resolver o problema.
   >
   >Observe que enquanto a delegação de subdomínio é executada, outras solicitações por meio do Painel de controle do Campaign serão inseridas em uma fila e executadas somente após a conclusão da Delegação de subdomínio para evitar problemas de desempenho.

No final do processo, os subdomínios serão configurados para funcionar com a instância do Adobe Campaign e os elementos abaixo serão criados:

* **O subdomínio** com os seguintes **registros DNS**: SOA, MX, CNAME(s), DKIM, SPF, TXT,
* **Subdomínios adicionais** para hospedar mirror, recursos, páginas de rastreamento e chave de domínio,
* **Caixas de entrada**: Remetente, Erro, Responder para.

>[!NOTE]
>
>Por padrão, a caixa de entrada &quot;Responder para&quot; no Painel de controle do Campaign está configurada para apagar emails e não é revisável. Se quiser monitorar a caixa de entrada “Responder para” para suas campanhas de marketing, não use este endereço.

Para obter mais detalhes sobre o subdomínio, clique nos botões **[!UICONTROL Subdomain details]** e **[!UICONTROL Sender info]**.

![](assets/detail_buttons.png)

![](assets/subdomain_details.png)

![](assets/sender_info.png)

>[!IMPORTANT]
>
>Após a etapa de processamento, verifique com o Atendimento ao cliente da Adobe se foi apresentada uma solicitação de auditoria para a equipe de delivery auditar o novo subdomínio que foi criado. O processo de auditoria pode demorar de 3 a 10 dias úteis após a delegação do subdomínio.
>
>As verificações realizadas incluem loops de feedback e testes de loops de reclamação de spam. Portanto, não recomendamos a utilização do subdomínio antes da conclusão da auditoria, uma vez que poderá resultar em uma má reputação do subdomínio.

## Uso de CNAMEs {#use-cnames}

O uso de CNAMEs para delegação de subdomínio não é compatível com o Painel de controle do Campaign. Para usar esse método, entre em contato com o Atendimento ao cliente da Adobe.

**Tópicos relacionados:**

* [Delegar subdomínios (vídeo tutorial)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [Marca de subdomínios](../../subdomains-certificates/using/subdomains-branding.md)
* [Monitorar subdomínios](../../subdomains-certificates/using/monitoring-subdomains.md)