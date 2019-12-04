---
title: Lista de permissões de intervalo IP
description: Saiba como adicionar intervalos IP à lista de permissões para acesso aos servidores SFTP
translation-type: tm+mt
source-git-commit: e080a86cc598581b75cffd622b2109e10355130a

---


# Lista de permissões de intervalo IP {#ip-range-whitelisting}

Os servidores SFTP estão protegidos. Para poder acessá-los para exibir arquivos ou gravar novos arquivos, é necessário adicionar o endereço IP público do sistema ou cliente que acessa os servidores.

## Sobre o formato CIDR {#about-cidr-format}

O CIDR (Classless Inter-Domain Routing) é o formato suportado ao adicionar intervalos IP com a interface do Painel de controle.

A sintaxe consiste em um endereço IP, seguido por um caractere '/' e um número decimal. O formato e sua sintaxe são detalhados por completo [neste artigo](https://whatismyipaddress.com/cidr).

Você pode procurar na Internet ferramentas online gratuitas que o ajudarão a converter o intervalo de IP disponível no formato CIDR.

## Práticas recomendadas {#best-practices}

Certifique-se de seguir as recomendações e limitações abaixo ao adicionar endereços IP à lista de permissões no Painel de controle.

* **Intervalos** de IP da lista de permissões em vez de endereços IP únicos. Para adicionar um único endereço IP à lista de permissões, anexe um '/32' a ele para indicar que o intervalo inclui apenas um único IP.
* **Não inclua intervalos** muito largos, por exemplo, incluindo &gt; 265 endereços IP. O Painel de controle rejeitará quaisquer intervalos no formato CIDR que estejam entre /0 e /23.
* Somente endereços **IP** públicos podem ser listados na lista de permissões.
* Certifique-se de excluir **regularmente os endereços** IP da lista de permissões de que você não precisa mais.

## Endereços IP da lista de permissões {#whitelisting-ip-addresses}

Para adicionar um intervalo IP à lista de permissões, siga estas etapas:

1. Open the **[!UICONTROL SFTP]** card, then select the **[!UICONTROL IP Whistelisting]** tab.
1. A lista de endereços IP da lista de permissões é exibida para cada instância. Selecione a instância desejada na lista do lado esquerdo e clique no **[!UICONTROL Add new IP range]** botão.

   ![](assets/control_panel_add_range.png)

1. Defina o Intervalo de IP que deseja incluir na lista de permissões, no formato CIDR, e defina o rótulo que será exibido na lista.

   >[!NOTE]
   >
   >Esses caracteres especiais são permitidos no campo Rótulo:
   > `. _ - : / ( ) # , @ [ ] + = & ; { } ! $`

   ![](assets/control_panel_add_range2.png)

   >[!CAUTION]
   >
   >Um intervalo IP não pode sobrepor um intervalo existente na lista de permissões. Nesse caso, primeiro exclua o intervalo que contém o IP sobreposto.
   >
   >É possível adicionar uma lista de permissões para várias instâncias. Para fazer isso, pressione a tecla de seta para baixo ou digite as primeiras letras da instância desejada e selecione-a na lista de sugestões.

   ![](assets/control_panel_add_range3.png)

1. Clique no botão **.[!UICONTROL Save]** A adição da lista de permissões IP será exibida como PENDENTE até que a solicitação seja totalmente processada. Isso deve levar apenas alguns segundos.

Para excluir intervalos IP da lista de permissões, selecione-os e clique no **[!UICONTROL Delete IP range]** botão.

![](assets/control_panel_delete_range2.png)

>[!NOTE]
>
>No momento, não é possível editar um intervalo na lista de permissões. Para modificar um intervalo de IP, exclua-o e crie um que corresponda às suas necessidades.

## Monitoramento de alterações {#monitoring-changes}

A página inicial **[!UICONTROL Job Logs]** do Painel de controle permite monitorar todas as alterações feitas em endereços IP da lista de permissões.

Para obter mais informações sobre a interface do Painel de controle, consulte [esta seção](../../discover/using/discovering-the-interface.md).

![](assets/control_panel_ip_logNEW.png)
