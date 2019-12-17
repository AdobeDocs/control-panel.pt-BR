---
title: Gerenciamento de armazenamento SFTP
description: Saiba como monitorar e gerenciar o armazenamento do servidor SFTP
translation-type: tm+mt
source-git-commit: 85bef8fa652be883bc2afbc42a2d893ea75a4e77

---


# Gerenciamento de armazenamento SFTP {#sftp-storage-management}

Você pode ter uma capacidade de armazenamento diferente provisionada no servidor SFTP, dependendo dos termos contratuais.

É essencial monitorar regularmente o espaço disponível para cada um dos servidores SFTP. Caso contrário, talvez você não consiga salvar mais arquivos adicionais no servidor ou executar com êxito fluxos de trabalho que dependam das atualizações deste servidor.

**Tópicos relacionados:**

* [Vídeo tutorial do Campaign Standard](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/monitoring-server-capacity-whitelisting-adding-ssh-key.html)
* [Vídeo tutorial do Campaign Classic](https://docs.adobe.com/content/help/en/campaign-learn/campaign-classic-tutorials/administrating/control-panel-acc/managing-sftp-servers.html)

## Acessar informações de capacidade de armazenamento {#accessing-storage-capacity-information}

A **[!UICONTROL Top utilized SFTP disk capacity]**seção no cabeçalho inclui os três principais servidores mais utilizados conectados às instâncias às quais você tem acesso de Administrador. Essas informações estão disponíveis em todas as guias do cartão SFTP.

![](assets/control_panel_topspace.png)

As informações sobre o espaço usado por todas as instâncias às quais você tem acesso estão disponíveis na **[!UICONTROL Storage]**guia do cartão SFTP. Ele é atualizado em cada atualização de página.

![](assets/control_panel_space.png)

Para cada instância, um alerta visual informa quando seu armazenamento ultrapassa sua capacidade:

* **Laranja**: o caso superou 80% da sua capacidade,
* **Vermelho**: a instância supera 90% de sua capacidade.

Dicas adicionais também estão disponíveis para ajudá-lo a saber como proceder à medida que o servidor se aproxima de sua capacidade.

## Práticas recomendadas quando a capacidade de armazenamento é esgotada {#best-practices-when-capacity-runs-out}

1. **Limpe o servidor SFTP de arquivos** antigos ou desnecessários. Para obter mais informações sobre como acessar a pasta do servidor SFTP, consulte [esta seção](../../sftp/using/logging-into-sftp-server.md).
1. Verifique se os **fluxos** de trabalho que limpam os servidores SFTP foram executados com êxito. Para obter mais informações sobre fluxos de trabalho técnicos no Adobe Campaign, consulte as documentações dedicadas do [Campaign Classic](https://docs.campaign.adobe.com/doc/AC/en/WKF__General_operation_Building_a_workflow.html#Technical_workflows) e do [Campaign Standard](https://helpx.adobe.com/campaign/standard/administration/using/technical-workflows.html) .
1. Entre em contato com a equipe de sua conta para **solicitar mais armazenamento** (podem ser aplicadas taxas adicionais).
1. Entre em contato com o **Atendimento ao cliente**, se achar que existe um problema.
