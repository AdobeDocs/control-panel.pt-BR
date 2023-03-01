---
product: campaign
solution: Campaign
title: Remover delegação de subdomínios
description: Saiba como remover a delegação de subdomínios para o Adobe.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: deb99ceb789f40c905de1a76cca8deca6b979765
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 16%

---

# Remover delegação de subdomínios para o Adobe {#remove-delegated--subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="Remover delegação de subdomínio"
>abstract="Essa tela permite remover a delegação de um subdomínio para o Adobe. Lembre-se de que esse processo não pode ser desfeito e é irreversível até que sua execução seja concluída.<br><br>Se estiver tentando remover a delegação de um domínio primário para a instância selecionada, você deverá escolher o domínio que a substituirá."

O Painel de controle do Campaign permite remover a delegação de um subdomínio que foi delegado ao Adobe, incluindo a configuração CNAME.

## Observações importantes {#important}

Antes de continuar, considere cuidadosamente os impactos que ocorrem assim que o processo de remoção é acionado:

* Depois que o processo é acionado, a remoção da delegação de subdomínio não pode ser desfeita e é irreversível até que a execução do processo seja concluída.
* Nenhuma outra delegação de subdomínio pode ser removida quando um processo semelhante em outro subdomínio estiver em andamento.
* Uma delegação removida em um subdomínio não pode ser delegada novamente até 3 dias após sua remoção.

## Remover uma delegação de subdomínio {#steps}

Para remover a delegação de um subdomínio para o Adobe, siga estas etapas:

1. Clique no botão de reticências ao lado da delegação de domínio que deseja remover e selecione **[!UICONTROL Remove delegated subdomain]**.

   ![](assets/undelegate-subdomain.png)

1. Revise o aviso e confirme a remoção da delegação de domínio para o Adobe.

1. Revise as informações sobre a instância à qual o subdomínio está associado, incluindo afinidades de IP relacionadas e configurações de marca.

   Se você estiver removendo a delegação do domínio primário para a instância selecionada, será necessário escolher o domínio que a substituirá usando o **[!UICONTROL Replacement Domain]** lista.

   Clique em **[!UICONTROL Next]** para prosseguir com a remoção.

   ![](assets/undelegate-subdomain-details.png)

1. Revise o resumo exibido. Para confirmar a remoção, digite o URL do domínio para o qual deseja remover a delegação e clique em **[!UICONTROL Submit]**.

   ![](assets/undelegate-submit.png)

Após iniciar a remoção da delegação, o trabalho pendente é exibido nos logs de trabalho até sua conclusão.

![](assets/undelegate-job.png)

## Códigos de erro {#FAQ}

Esta seção lista as mensagens de erro que você pode encontrar ao tentar remover a delegação de um subdomínio:

| Código de erro | Mensagem | Descrição |
|  ---  |  ---  |  ---  |
| 8002 | A remoção de domínio delegado solicitada não pode ser realizada porque já existe uma solicitação semelhante em andamento. Tente novamente após 3 dias | Um trabalho de remoção de delegação de subdomínio já está em processo para a instância selecionada. Aguarde até 3 dias para iniciar um novo trabalho de remoção. |
| 8003 | Não há suporte para a remoção de domínio delegado solicitada nesta instância. | Não há suporte para a remoção de delegação para o subdomínio selecionado devido a um problema técnico. Entre em contato com o Atendimento ao cliente. |
| 8004 | A remoção de domínio delegado solicitada não é permitida, pois há apenas um domínio nesta instância. | Somente um subdomínio foi delegado para a instância selecionada. A remoção de delegação não é permitida. |
| 8005 | Não há suporte para a remoção de domínio delegado solicitada nesta configuração. | Não há suporte para a remoção de delegação para o subdomínio selecionado devido a um problema técnico. Entre em contato com o Atendimento ao cliente. |
| 8006 | A remoção de domínio delegado solicitada não é permitida por motivos desconhecidos. Entre em contato com o Atendimento ao cliente. | Não há suporte para a remoção de delegação para a instância selecionada devido a problemas desconhecidos. Entre em contato com o Atendimento ao cliente. |
