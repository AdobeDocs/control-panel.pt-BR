---
title: Configurar um novo subdomínio
description: Saiba como configurar um novo subdomínio para as instâncias da sua campanha
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Configurar um novo subdomínio {#setting-up-subdomain}

## Delegação de subdomínio completa {#full-subdomain-delegation}

O Painel de controle permite que você delegue totalmente um subdomínio ao Adobe Campaign. Para fazer isso, siga estas etapas:

1. No **[!UICONTROL Subdomains & Certificates]**cartão, selecione a instância de produção desejada e clique em**[!UICONTROL Setup new subdomain]**.

   >[!NOTE]
   >
   >A delegação de subdomínio está disponível somente para instâncias **de produção** .

   ![](assets/subdomain1.png)

1. Clique em **[!UICONTROL Next]**para confirmar o método de delegação completo.

   >[!NOTE]
   >
   >[No momento, os métodos CNAME](#use-cnames) e personalizados não são suportados pelo Painel de controle.

   ![](assets/subdomain3.png)

1. Crie o subdomínio e os servidores de nomes desejados na solução de hospedagem usada por sua organização. Para fazer isso, copie e cole as informações do Adobe NamesServer exibidas no assistente.

   Para obter mais informações sobre como criar um subdomínio em uma solução de hospedagem, consulte este vídeo tutorial.

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

1. Depois que o subdomínio for submetido, o Painel de controle verificará se ele aponta para os registros Adobe NS e se o registro Início da autoridade (SOA) não existe para esse subdomínio.

1. Se as verificações forem bem-sucedidas, o Painel de Controle iniciará a configuração do subdomínio com registros DNS, URLs adicionais, caixas de entrada, etc. Para obter mais detalhes sobre o progresso da configuração, clique no **[!UICONTROL Process details]**botão.

   ![](assets/subdomain7.png)

No final do processo, os subdomínios serão configurados para funcionar com sua instância do Adobe Campaign e os elementos abaixo serão criados:

* **O subdomínio** com os seguintes registros **** DNS: SOA, MX, CNAME(s), DKIM, SPF, TXT,
* **Subdomínios** adicionais para hospedar espelhamento, recurso, páginas de rastreamento e chave de domínio,
* **Caixas de entrada**: Remetente, Erro, Responder.

## Uso de CNAMEs {#use-cnames}

O uso de CNAMEs para delegação de subdomínio não é recomendado pela Adobe e não é suportado pelo Painel de controle.

Para usar esse método, entre em contato com o Atendimento ao cliente da Adobe.
