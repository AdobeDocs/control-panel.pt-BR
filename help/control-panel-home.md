---
title: Documentação do produto
description: Documentação do Painel de controle.
feature: Control Panel
role: Admin
level: Experienced
exl-id: 2b2cfaed-e42e-4c3a-a8d8-224b936890ab
source-git-commit: e8bffd8e7f571fd85c725adf837c2997f7615fcd
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 100%

---

# Central de ajuda {#control-panel-documentation}

>[!CONTEXTUALHELP]
>id="cp_overview"
>title="Sobre o Painel de controle"
>abstract="A página inicial do Painel de controle fornece acesso a todas as ações que podem ser executadas nas instâncias do Campaign."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/accessing-control-panel.html?lang=pt-BR" text="Acesso ao Painel de controle"

O Painel de controle do Campaign ajuda a aumentar a eficiência do seu trabalho como administrador de produto do Campaign Standard, v7 e v8, permitindo gerenciar configurações e rastrear o uso de cada uma de suas instâncias do Campaign.

## Novidades

**Interface**

* O Painel de controle agora está disponível em outros idiomas. [Saiba mais](discover/using/discovering-the-interface.md#supported-languages-languages)

**Monitoramento de perfis ativos**

* Agora é possível monitorar o número de perfis ativos aos quais você está atribuído na sua organização e a contagem total de perfis usados na organização em todas as instâncias, se estiver usando várias instâncias. [Saiba mais](performance-monitoring/using/active-profiles-monitoring.md)

**Registros DMARC**

* Agora, vários endereços de email podem receber emails de relatórios agregados e de relatório de falhas. [Saiba mais](subdomains-certificates/using/dmarc.md)
* Foram feitas alterações em caso de ambos os registros, DMARC e BIMI, existirem em um subdomínio:

   * Os registros DMARC não podem ser excluídos. Se quiser excluir um, será necessário excluir o registro BIMI primeiro.
   * Os registros DMARC podem ser editados, mas o downgrade da política para &quot;Nenhum&quot; não é permitido e seu valor percentual deve ser 100.

>[!CAUTION]
>
>* O Painel de controle é restrito aos usuários administradores. [Saiba mais](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=pt-BR#discover-control-panel)
>
>* Para o Campaign v7, restrições de implantação se aplicam. [Saiba mais](faq.md#v7-restrictions)

## Recursos adicionais {#additional-resources}

<table>
    <tr>
        <td><b>Campaign Standard</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/control-panel-overview.html?lang=pt-BR">tutoriais em vídeo do Painel de controle</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-standard/using/campaign-standard-home.html?lang=pt-BR">Documentação do produto Campaign Standard</a></li>
        </ul>
        </td>
        <td><b>Campaign v7</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/control-panel-overview.html?lang=pt-BR">tutoriais em vídeo do Painel de controle</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-classic/using/campaign-classic-home.html?lang=pt-BR">Documentação do produto Campaign v7</a></li>
        </ul>
        </td>
        <td><b>Campaign v8</b><br/>
        <ul>
            <li><a href="https://experienceleague.adobe.com/docs/campaign-learn/control-panel/control-panel-overview.html?lang=pt-BR">Tutoriais em vídeo do Painel de controle</a></li>
            <li><a href="https://experienceleague.adobe.com/docs/campaign/campaign-v8/campaign-home.html?lang=pt-BR">Documentação do produto Campaign v8</a></li>
        </ul>
        </td>
    </tr>
</table>
