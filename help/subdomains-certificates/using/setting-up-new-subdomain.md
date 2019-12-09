---
title: Configurar um novo subdomínio
description: Saiba como configurar um novo subdomínio para as instâncias da sua campanha
translation-type: tm+mt
source-git-commit: cde5b58c1cf65d23b68c5fa6b1a484fc6db40325

---


# Configurar um subdomínio {#setting-up-subdomain}

O Painel de controle permite que você delegue totalmente um subdomínio ao Adobe Campaign. Para fazer isso, siga as etapas detalhadas abaixo.

>[!NOTE]
>
>O uso de CNAMEs para delegação de subdomínio não é suportado pelo Painel de Controle. For more on this method, refer to [this page](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).

1. No **[!UICONTROL Subdomains & Certificates]**cartão, selecione a instância desejada e clique no**[!UICONTROL Setup new subdomain]** botão.

   ![](assets/subdomain1.png)

   >[!NOTE]
   >
   >O **[!UICONTROL Setup new subdomain]**botão está disponível somente para instâncias de Produção.

1. Selecione o **[!UICONTROL Delegation to Adobe]**método e clique em**[!UICONTROL Next]**.

   ![](assets/subdomain3.png)

1. Crie o subdomínio desejado na solução de hospedagem usada por sua organização. Para fazer isso, copie as informações do Adobe NamesServer exibidas no assistente e cole-as na solução de hospedagem.

   Para obter mais informações sobre como criar um subdomínio em uma solução de hospedagem, consulte o vídeo tutorial acessível pelo assistente.

   ![](assets/subdomain4.png)

   Depois que o subdomínio for criado com as informações correspondentes do servidor de nomes da Adobe, clique em **[!UICONTROL Next]**.

1. Selecione o caso de uso desejado para o subdomínio:

   * **Comunicações** de marketing: comunicações destinadas a fins comerciais. Exemplo: campanha por email de vendas.
   * **Comunicações** transacionais e operacionais: as comunicações transacionais contêm informações destinadas a concluir um processo que o destinatário iniciou com você. Exemplo: confirmação de compra, email de redefinição de senha. As comunicações organizacionais dizem respeito ao intercâmbio de informações, ideias e opiniões dentro e fora da organização, sem fins comerciais.
   Analisar seus subdomínios desta forma é uma prática recomendada para a entrega. Ao fazê-lo, a reputação de cada subdomínio é isolada e protegida. Por exemplo, se seu subdomínio para comunicações de marketing acabar sendo bloqueado pelos provedores de serviços de Internet, seu subdomínio de comunicações transacionais não será afetado e continuará sendo capaz de enviar comunicações.

   ![](assets/subdomain5.png)

   >[!NOTE]
   >
   >Você só pode selecionar um caso de uso que tenha sido configurado para sua instância. Se a instância tiver sido configurada apenas para &quot;Comunicações de marketing&quot;, você não poderá selecionar o caso de uso &quot;Comunicações transacionais e operacionais&quot;.

1. Insira o subdomínio que você criou na solução de hospedagem com as informações do Adobe NamesServer e clique em **[Enviar]**.

   >[!NOTE]
   >
   > Certifique-se de preencher o subdomínio **completo** para delegar. Por exemplo, para delegar o subdomínio &quot;usoffer.email.weretail.com&quot;, digite &quot;usoffer.email.weretail.com&quot;.

   ![](assets/subdomain6.png)

1. Depois que o subdomínio for enviado, o Painel de controle executará várias operações para configurar o subdomínio e verificar se ele aponta corretamente para a instância da Campanha (criação de registros de namespace, configuração da instância da Campanha, verificação de registro Início da Autoridade etc.).

   Para obter mais detalhes sobre o andamento da configuração, clique no **[!UICONTROL Process details]**botão.

   ![](assets/subdomain7.png)

O que você consegue no final do processo?
* Subdomínio com os seguintes registros DNS - SOA, MX, CNAME(s), DKIM, SPF, TXT.
* Subdomínios adicionais para hospedar espelhamento, recurso, páginas de rastreamento e chave de domínio
* Caixas de entrada - Remetente, Erro, Responder a
* Em última análise, os subdomínios serão configurados para funcionar com sua instância do Adobe Campaign
