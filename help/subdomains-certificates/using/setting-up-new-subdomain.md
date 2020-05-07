---
title: Configurar um novo subdomínio
description: Saiba como configurar um novo subdomínio para suas instâncias de campanha
translation-type: tm+mt
source-git-commit: b27c6c8db765bc61b4e2afcadf446b28b15d3a93
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Configurar um novo subdomínio {#setting-up-subdomain}

>[!CONTEXTUALHELP]
>id="cp_subdomain_management"
>title="Configurar novos subdomínios e gerenciar certificados"
>abstract="É necessário configurar um novo subdomínio e gerenciar os certificados SSL de seus subdomínios para enviar e-mails por start ou publicar landings page com Adobe Campaign."
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="Como monitorar os certificados SSL de seus subdomínios"

>[!IMPORTANT]
>
>A delegação de subdomínios do Painel de controle está disponível em beta e sujeita a atualizações e modificações frequentes sem aviso prévio.

## Delegação de subdomínio completa {#full-subdomain-delegation}

O Painel de controle permite que você delegue totalmente um subdomínio para o Adobe Campaign. Para fazer isso, siga as etapas abaixo.

>[!NOTE]
>
>Se a instância selecionada não tiver subdomínios configurados anteriormente, o primeiro subdomínio delegado à Adobe se tornará o subdomínio **** primário dessa instância, você não poderá alterá-lo no futuro.
>
>Os registros de DNS reverso serão criados para outros subdomínios usando o subdomínio primário. Endereços de resposta e de rejeição para outros subdomínios serão gerados a partir do subdomínio primário.

1. No **[!UICONTROL Subdomains & Certificates]** cartão, selecione a instância de produção desejada e clique em **[!UICONTROL Setup new subdomain]**.

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >A delegação de subdomínio está disponível somente para instâncias **de produção** .

1. Clique em **[!UICONTROL Next]** para confirmar o método de delegação completo.

   ![](assets/subdomain3.png)

   >[!NOTE]
   >
   >[No momento, os métodos CNAME](#use-cnames) e personalizados não são suportados pelo Painel de controle.

1. Crie o subdomínio e os servidores de nomes desejados na solução de hospedagem usada por sua organização. Para fazer isso, copie e cole as informações do Adobe NamesServer exibidas no assistente. Para obter mais informações sobre como criar um subdomínio em uma solução de hospedagem, consulte o vídeo [do](https://video.tv.adobe.com/v/30175?captions=por_br)tutorial.

   >[!IMPORTANT]
   >
   >Ao configurar servidores de nomes, certifique-se de **nunca delegar seu subdomínio raiz à Adobe**. Caso contrário, o domínio poderá trabalhar somente com a Adobe. Qualquer outro uso será impossível, como, por exemplo, enviar emails internos aos funcionários de sua organização.
   >
   >Além disso, **não crie um arquivo** de zona separado para esse novo subdomínio.

   ![](assets/subdomain4.png)

   Depois que o subdomínio for criado com as informações correspondentes do servidor de nomes da Adobe, clique em **[!UICONTROL Next]**.

1. Selecione o caso de uso desejado para o subdomínio:

   * **Comunicações** de marketing: comunicações destinadas a fins comerciais. Exemplo: campanha de e-mail de vendas.
   * **Comunicações** transacionais e operacionais: as comunicações transacionais contêm informações destinadas a concluir um processo que o recipient iniciou com você. Exemplo: confirmação de compra, email de redefinição de senha. As comunicações organizacionais estão relacionadas com o intercâmbio de informações, ideias e visualizações dentro e fora da organização, sem fins comerciais.
   ![](assets/subdomain5.png)

   **Detalhar seus subdomínios de acordo com os casos de uso é uma prática recomendada para a entrega**. Ao fazê-lo, a reputação de cada subdomínio é isolada e protegida. Por exemplo, se seu subdomínio para comunicações de marketing acabar sendo incluído na blacklist por Provedores de serviço da Internet, seu subdomínio de comunicações transacionais não será afetado e continuará sendo capaz de enviar comunicações.

   **Você pode delegar subdomínios para casos** de uso de Marketing e Transacional:

   * Para casos de uso de Marketing, os subdomínios serão configurados em instâncias **MID** (Meid sourcing).
   * Para casos de uso transacional, os subdomínios serão configurados em TODAS as instâncias **RT** (Message Center / Real-time messaging) para garantir a conectividade. Os subdomínios operarão, portanto, com todas as suas instâncias de RT.
   >[!NOTE]
   >
   >Se você estiver usando o Campaign Classic, o Painel de controle permitirá que você veja quais instâncias de RT/MID estão conectadas à instância de Marketing com a qual você está trabalhando. Para obter mais informações, consulte [esta seção](../../instances-settings/using/instance-details.md).

1. Digite o subdomínio que você criou na solução de hospedagem e clique em **[!UICONTROL Submit]**.

   Certifique-se de preencher o nome **** completo do subdomínio a ser delegado. Por exemplo, para delegar o subdomínio &quot;usoffer.email.weretail.com&quot;, digite &quot;usoffer.email.weretail.com&quot;.

   ![](assets/subdomain6.png)

1. Depois que o subdomínio for submetido, o Painel de controle verificará se ele aponta corretamente para os registros Adobe NS e se o registro do Start da autoridade (SOA) não existe para esse subdomínio.

   >[!NOTE]
   >
   >Observe que enquanto a delegação de subdomínio é executada, outras solicitações por meio do Painel de controle serão inseridas em uma fila e executadas somente após a conclusão da Delegação de subdomínio, para evitar problemas de desempenho.

1. Se as verificações forem bem-sucedidas, o Painel de controle fará o start de configurar o subdomínio com registros DNS, URLs adicionais, caixas de entrada, etc.

   Eventualmente, a equipe de Disponibilidade será notificada sobre o novo subdomínio, a fim de fazer a auditoria. O processo de auditoria pode levar de 3 a 10 dias úteis após a delegação do subdomínio. As verificações realizadas incluem loops de feedback e testes de loops de reclamação de spam. Por conseguinte, não recomendamos a utilização do subdomínio antes de a auditoria ter sido concluída, uma vez que poderá resultar numa má reputação do subdomínio.

   Para obter mais detalhes sobre o progresso da configuração, clique no **[!UICONTROL Process details]** botão.

   ![](assets/subdomain7.png)

   >[!NOTE]
   >
   >Em alguns casos, a delegação passa, mas o subdomínio pode não ser verificado com êxito. O subdomínio permanecerá na **[!UICONTROL Processing]** lista com um registro de tarefas que fornece informações sobre o erro. Entre em contato com o Atendimento ao cliente se tiver problemas para resolver o problema.

No final do processo, os subdomínios serão configurados para funcionar com sua instância do Adobe Campaign e os elementos abaixo serão criados:

* **O subdomínio com os seguintes registros** DNS: SOA, MX, CNAME(s), DKIM, SPF, TXT,
* **Subdomínios** adicionais para hospedar espelhamento, recurso, páginas de rastreamento e chave de domínio,
* **Caixas de entrada**: Remetente, Erro, Responder.

   Por padrão, a caixa de entrada &quot;Responder&quot; no Painel de controle está configurada para apagar e-mails e não é revisável. Se quiser monitorar sua caixa de entrada &quot;Responder&quot; para suas campanhas de marketing, não use este endereço.

Para obter mais detalhes sobre o subdomínio, clique nos botões **[!UICONTROL Subdomain details]** e **[!UICONTROL Sender info]** .

![](assets/detail_buttons.png)

![](assets/subdomain_details.png)

![](assets/sender_info.png)

## Uso de CNAMEs {#use-cnames}

O uso de CNAMEs para delegação de subdomínio não é suportado pelo Painel de Controle. Para usar esse método, entre em contato com o Atendimento ao cliente da Adobe.

**Tópicos relacionados:**

* [Delegar subdomínios (vídeo do tutorial)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [Marca de subdomínios](../../subdomains-certificates/using/subdomains-branding.md)
* [Monitoramento de seus subdomínios](../../subdomains-certificates/using/monitoring-subdomains.md)