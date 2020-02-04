---
title: Configurar um novo subdomínio
description: Saiba como configurar um novo subdomínio para as instâncias da sua campanha
translation-type: tm+mt
source-git-commit: ee5567a41f68d4dc51c19ae70e8b25693a1d33fa

---


# Configurar um novo subdomínio {#setting-up-subdomain}

>[!IMPORTANT]
>
>A delegação de subdomínios do Painel de controle está disponível em beta e sujeita a atualizações e modificações frequentes sem aviso prévio.

Se você tiver alguma dúvida sobre os métodos de delegação de subdomínio, entre em contato com a equipe de Entrega da Adobe ou, eventualmente, entre em contato com o Atendimento ao cliente para solicitar consultoria de Entrega.

## Delegação de subdomínio completa {#full-subdomain-delegation}

O Painel de controle permite que você delegue totalmente um subdomínio ao Adobe Campaign. Para fazer isso, siga as etapas abaixo.

>[!NOTE]
>
>Se a instância selecionada não tiver subdomínios configurados anteriormente, o primeiro subdomínio delegado à Adobe se tornará o subdomínio **** primário dessa instância, você não poderá alterá-lo no futuro.
>
>Os registros de DNS reverso serão criados para outros subdomínios usando o subdomínio primário. Endereços de resposta e de rejeição para outros subdomínios serão gerados a partir do subdomínio primário.

1. No **[!UICONTROL Subdomains & Certificates]**cartão, selecione a instância de produção desejada e clique em**[!UICONTROL Setup new subdomain]**.

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >A delegação de subdomínio está disponível somente para instâncias **de produção** .

1. Clique em **[!UICONTROL Next]**para confirmar o método de delegação completo.

   ![](assets/subdomain3.png)

   >[!NOTE]
   >
   >[No momento, os métodos CNAME](#use-cnames) e personalizados não são suportados pelo Painel de controle.

1. Crie o subdomínio e os servidores de nomes desejados na solução de hospedagem usada por sua organização. Para fazer isso, copie e cole as informações do Adobe NamesServer exibidas no assistente. Para obter mais informações sobre como criar um subdomínio em uma solução de hospedagem, consulte o vídeo [do](https://video.tv.adobe.com/v/30175?captions=por_br)tutorial.

   >[!CAUTION]
   >
   >Ao configurar servidores de nomes, certifique-se de **nunca delegar seu subdomínio raiz à Adobe**. Caso contrário, o domínio poderá trabalhar somente com a Adobe. Qualquer outro uso será impossível, como, por exemplo, enviar emails internos aos funcionários de sua organização.

   ![](assets/subdomain4.png)

   Depois que o subdomínio for criado com as informações correspondentes do servidor de nomes da Adobe, clique em **[!UICONTROL Next]**.

1. Selecione o caso de uso desejado para o subdomínio:

   * **Comunicações** de marketing: comunicações destinadas a fins comerciais. Exemplo: campanha por email de vendas.
   * **Comunicações** transacionais e operacionais: as comunicações transacionais contêm informações destinadas a concluir um processo que o destinatário iniciou com você. Exemplo: confirmação de compra, email de redefinição de senha. As comunicações organizacionais dizem respeito ao intercâmbio de informações, ideias e opiniões dentro e fora da organização, sem fins comerciais.
   >[!NOTE]
   >
   >Detalhar seus subdomínios de acordo com os casos de uso é uma prática recomendada para a entrega. Ao fazê-lo, a reputação de cada subdomínio é isolada e protegida.
   >
   >Por exemplo, se seu subdomínio para comunicações de marketing acabar sendo bloqueado pelos provedores de serviços de Internet, seu subdomínio de comunicações transacionais não será afetado e continuará sendo capaz de enviar comunicações.

   ![](assets/subdomain5.png)

1. Digite o subdomínio que você criou na solução de hospedagem e clique em **[!UICONTROL Submit]**.

   >[!NOTE]
   >
   > Certifique-se de preencher o nome **** completo do subdomínio a ser delegado. Por exemplo, para delegar o subdomínio &quot;usoffer.email.weretail.com&quot;, digite &quot;usoffer.email.weretail.com&quot;.

   ![](assets/subdomain6.png)

1. Depois que o subdomínio for submetido, o Painel de controle verificará se ele aponta corretamente para os registros Adobe NS e se o registro Início da autoridade (SOA) não existe para esse subdomínio.

1. Se as verificações forem bem-sucedidas, o Painel de Controle iniciará a configuração do subdomínio com registros DNS, URLs adicionais, caixas de entrada, etc. Para obter mais detalhes sobre o progresso da configuração, clique no **[!UICONTROL Process details]**botão.

   ![](assets/subdomain7.png)

   >[!NOTE]
   >
   >Em alguns casos, a delegação passa, mas o subdomínio pode não ser verificado com êxito. O subdomínio irá diretamente para a **[!UICONTROL Verified subdomains]**lista com o**[!UICONTROL Unverified]** status e um registro de trabalho que fornece informações sobre o erro. Entre em contato com o Atendimento ao cliente se tiver problemas para resolver o problema.
   >
   >Observe que enquanto a delegação de subdomínio é executada, outras solicitações por meio do Painel de controle serão inseridas em uma fila e executadas somente após a conclusão da Delegação de subdomínio, para evitar problemas de desempenho.

No final do processo, os subdomínios serão configurados para funcionar com sua instância do Adobe Campaign e os elementos abaixo serão criados:

* **O subdomínio** com os seguintes registros **** DNS: SOA, MX, CNAME(s), DKIM, SPF, TXT,
* **Subdomínios** adicionais para hospedar espelhamento, recurso, páginas de rastreamento e chave de domínio,
* **Caixas de entrada**: Remetente, Erro, Responder.

>[!NOTE]
>
>Por padrão, a caixa de entrada &quot;Responder&quot; no Painel de controle está configurada para apagar e-mails e não é revisável. Se você quiser monitorar sua caixa de entrada &quot;Responder&quot; para suas campanhas de marketing, não use este endereço.


Para obter mais detalhes sobre o subdomínio, clique no **[!UICONTROL Subdomain Details]**botão.

![](assets/subdomain_details_general.png)

![](assets/subdomains_details_senderinfo.png)

>[!NOTE]
>
>Além do estágio de processamento, a Adobe notificará a equipe de capacidade de entrega sobre o novo subdomínio para auditar o subdomínio que foi criado. O processo de auditoria pode demorar até 3 dias após a delegação do subdomínio.
>
>As verificações realizadas incluem loops de feedback e testes de loops de reclamação de spam. Por conseguinte, não recomendamos a utilização do subdomínio antes de a auditoria ter sido concluída, uma vez que poderá resultar numa má reputação do subdomínio.

## Uso de CNAMEs {#use-cnames}

O uso de CNAMEs para delegação de subdomínio não é suportado pelo Painel de Controle. Para usar esse método, entre em contato com o Atendimento ao cliente da Adobe.

**Tópicos relacionados:**

* [Delegar subdomínios (vídeo tutorial)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [Marca de subdomínios](../../subdomains-certificates/using/subdomains-branding.md)
* [Monitoramento de seus subdomínios](../../subdomains-certificates/using/monitoring-subdomains.md)