---
product: campaign
solution: Campaign
title: Adicionar registros BIMI
description: Saiba como adicionar um registro BIMI para um subdomínio.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: dfb6f548c4d53df7eb807d9aa21065449927f945
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---


# Adicionar registros BIMI {#dmarc}

## Sobre registros BIMI {#about}

Brand Indicators for Message Identification (BIMI) é um padrão do setor que permite que um logotipo aprovado apareça ao lado do email de um remetente nas caixas de entrada dos provedores de caixa de correio para aprimorar o reconhecimento e a confiança da marca. Ele ajuda a impedir a falsificação de email e o phishing, verificando a identidade do remetente por meio da autenticação DMARC, dificultando que atores mal-intencionados personifiquem marcas legítimas em emails. Informações detalhadas sobre a implementação de BIMI estão disponíveis em [Guia de práticas recomendadas de capacidade de delivery do Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-bimi.html)

![](assets/bimi-example.png){width="70%" align="center"}

## Limitações e pré-requisitos {#limitations}

* Os registros SPF, DKIM e DMARC são pré-requisitos para a criação de um registro BIMI.
* Os registros BIMI só podem ser adicionados a subdomínios usando a delegação de subdomínio completa. [Saiba mais sobre métodos de configuração de subdomínios](subdomains-branding.md#subdomain-delegation-methods)
* Pré-requisitos do registro DMARC:

   * O tipo de política de registro para o subdomínio deve ser definido como &quot;Quarentena&quot; ou &quot;Rejeitar&quot;. A criação do registro BIMI não está disponível com um tipo de política DMARC definido como &quot;Nenhum&quot;.
   * A porcentagem de emails aos quais a política DMARC é aplicada deve ser 100%. O BIMI não é compatível com políticas DMARC com essa porcentagem definida como menos de 100%.

[Saiba como configurar registros DMARC](dmarc.md)

## Adicionar um registro BIMI para um subdomínio {#add}

Para adicionar um registro BIMI a um subdomínio, siga estas etapas:

1. Na lista de subdomínios, clique no botão de reticências ao lado do subdomínio desejado e selecione **[!UICONTROL Subdomain details]**.

1. Clique em **[!UICONTROL Add TXT record]** e escolha **[!UICONTROL BIMI]** do **[!UICONTROL Record type]** lista suspensa.

   ![](assets/bimi-add.png)

1. No **[!UICONTROL Company Logo URL]**, especifique o URL do arquivo SVG que contém o logotipo.

1. Embora **[!UICONTROL Certificate URL]** é opcional, é necessário para alguns provedores de caixa de correio, como Gmail e Apple, que cobrem 80% do mercado de caixas de correio. Portanto, recomendamos obter um Certificado de Marca Verificada (VMC) para realmente aproveitar o BIMI.

   +++Como obtenho um VMC?

   As principais etapas para obter um VMC são as seguintes:

   1. Registre o logotipo da sua marca como uma marca registrada em um escritório de propriedade intelectual reconhecido pelos emissores de VMC. Se você tiver uma equipe jurídica, recomendamos que trabalhe com ela para que seu logotipo seja registrado ou verifique se já é marca comercial.

   1. Depois de verificar que seu logotipo é marca comercial, entre em contato com a DigiCert ou com a Entrust certificate authority (CA) para solicitar um VMC.

   1. Quando o VMC for aprovado, você receberá um arquivo PEM (Privacy Enhanced Mail) de certificado de entidade. Anexe quaisquer outros certificados intermediários obtidos da CA a este arquivo PEM. Faça upload do arquivo PEM (juntamente com os arquivos anexados) no servidor público da Web e anote o URL do arquivo PEM. Você usará o URL em seu registro BIMI TXT.

   1. Quando o registro BIMI estiver visível na página de detalhes do subdomínio de um subdomínio específico, você poderá usar o Inspetor BIMI disponível [aqui](https://bimigroup.org/bimi-generator/) para verificar se o registro BIMI está funcionando corretamente.

   Informações detalhadas sobre a implementação do BIMI estão disponíveis no [Documentação padrão BIMI](https://bimigroup.org/implementation-guide/)
+++

1. Clique em **[!UICONTROL Add]** para confirmar a criação do registro BIMI.

Depois que a criação do registro BIMI for processada (aproximadamente 5 minutos), ela será exibida na tela de detalhes dos subdomínios. [Saiba como monitorar registros TXT para seus subdomínios](gs-txt-records.md#monitor)
