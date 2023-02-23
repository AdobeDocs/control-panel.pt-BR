---
product: campaign
solution: Campaign
title: Remover delegação de subdomínios
description: Saiba como remover a delegação de subdomínios para o Adobe.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 5a8c4c4d1c5c527135901cd41f2b0936af8737b4
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 2%

---

# Remover delegação de subdomínios para o Adobe {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="Remover delegação de subdomínio"
>abstract="Essa tela permite remover a delegação de um subdomínio para o Adobe. Lembre-se de que esse processo não pode ser revertido ou interrompido depois de enviado.<br><br>Se estiver tentando remover a delegação de um domínio primário para a instância selecionada, você será solicitado a escolher o domínio que o substituirá."

O Painel de controle do Campaign permite remover a delegação de um subdomínio que foi delegado ao Adobe, incluindo a configuração CNAME.

## Observações importantes {#important}

Antes de continuar, considere cuidadosamente os impactos que ocorrem quando o processo de remoção é acionado:

* A remoção da delegação de subdomínio não pode ser desfeita e será irreversível uma vez iniciada até que a execução do processo continue.
* Nenhuma outra delegação de subdomínio pode ser removida quando um processo semelhante em outro subdomínio estiver em andamento.
* Uma delegação removida em um subdomínio não pode ser delegada novamente até três dias após sua remoção.

## Remover uma delegação de subdomínio {#steps}

Para remover a delegação de um subdomínio para o Adobe, siga estas etapas:

1. Clique no botão de reticências ao lado da delegação de domínio que deseja remover e selecione **[!UICONTROL Remove delegated subdomain]**.

   ![](assets/undelegate-subdomain.png)

1. Revise o aviso de isenção de responsabilidade e confirme a remoção da delegação de domínio para o Adobe.

1. Revise informações sobre a instância à qual o subdomínio está associado, incluindo afinidades de IP relacionadas e configurações de marca.

   Se estiver removendo a delegação do domínio primário para a instância selecionada, será necessário escolher o domínio que a substituirá usando o **[!UICONTROL Replacement Domain]** lista.

   Clique em **[!UICONTROL Next]** para prosseguir com a remoção.

   ![](assets/undelegate-subdomain-details.png)

1. Revise o resumo que é exibido. Para confirmar a remoção, digite o URL do domínio para o qual deseja remover a delegação e clique em **[!UICONTROL Submit]**.

   ![](assets/undelegate-submit.png)

Depois que a remoção da delegação for iniciada, o trabalho pendente será exibido nos logs de trabalho até que seja concluído.

![](assets/undelegate-job.png)

## Códigos de erro {#FAQ}

Esta seção lista as mensagens de erro que podem ser encontradas ao tentar remover a delegação de um subdomínio:

| Código de erro | Mensagem | Descrição |
|  ---  |  ---  |  ---  |
| 8002 | A remoção de Domínio Delegado solicitado não pode ser solucionada, pois há uma solicitação de sobreposição semelhante em andamento. Tente após 3 dias | Um trabalho de remoção de delegação de subdomínio já está em andamento para a instância selecionada. Aguarde 3 dias para iniciar um novo trabalho de remoção. |
| 8003 | A remoção de Domínio Delegado solicitado não é suportada para esta instância. | A remoção da delegação não é compatível com o subdomínio selecionado devido a um problema técnico, entre em contato com o Atendimento ao cliente. |
| 8004 | A remoção de Domínio Delegado solicitado não é permitida, pois há apenas um domínio nesta instância. | Somente um subdomínio foi delegado para a instância selecionada. Não é permitida a remoção da delegação. |
| 8005 | A remoção de Domínio Delegado solicitado não é suportada para esta configuração. | A remoção da delegação não é compatível com o subdomínio selecionado devido a um problema técnico, entre em contato com o Atendimento ao cliente. |
| 8006 | A remoção de Domínio Delegado solicitado não é permitida devido a motivos desconhecidos. Entre em contato com o Atendimento ao cliente. | A remoção da delegação não é suportada para a instância selecionada devido a problemas desconhecidos, entre em contato com o Atendimento ao cliente. |
