---
product: campaign
solution: Campaign
title: Gerenciamento de registros TXT
description: Saiba como gerenciar registros TXT para verificação de propriedade de domínio.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: 013d6674-0988-4553-a23e-b3ec23da5323
TQID: 'https://experienceleague.adobe.com/G8eirPm9hY0XRZTtMOBpmdwxuo3-Uvdo9LQjiSiElPU'
product_v2:
  - id: dfc56824-e8b9-499e-85d4-21aedb507314
    internal-label: Campaign
feature_v2:
  - id: ae9127b0-c11d-467b-903d-a84cef43f6ed
    internal-label: Control Panel
  - id: a7760dfc-5c44-4d77-bb68-c50b1e265c93
    internal-label: Security and privacy
subfeature_v2:
  - id: f807e46f-d823-43a9-98be-82e0b2f3a05c
    internal-label: Subdomains and certificates
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: b2723b0683a305a992b710a37a3e47927e1fb65e
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 100%
---
# Introdução a registros TXT {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="Gerenciamento de registros TXT"
>abstract="Os registros TXT são um tipo de registro DNS usado para fornecer informações de texto sobre um domínio, que pode ser lido por fontes externas. O Painel de controle do Campaign permite adicionar três tipos de registros aos subdomínios: verificações de site do Google e registros DMARC e BIMI."

## Sobre registros TXT {#about}

Os registros TXT são um tipo de registro DNS usado para fornecer informações de texto sobre um domínio, que pode ser lido por fontes externas. O painel de controle permite adicionar três tipos de registros aos subdomínios:

* Os **registros TXT do Google** permitem atestar sua propriedade do domínio, garantindo altas taxas de entregabilidade e diminuindo a probabilidade de seus emails serem enviados à pasta de spam. [Saiba como adicionar registros TXT do Google](managing-txt-records.md)
* **Registros DMARC** fornecem uma maneira de autenticar o domínio do remetente e impedir o uso não autorizado do domínio para fins mal-intencionados. [Saiba como adicionar registros DMARC](dmarc.md)
* **Registros BIMI** permitem exibir um logotipo aprovado ao lado de seus emails nas caixas de entrada dos provedores para aumentar o reconhecimento e a confiança da marca. [Saiba como adicionar registros BIMI](bimi.md)

## Monitorar os registros dos subdomínios {#monitor}

É possível monitorar todos os registros TXT adicionados em cada subdomínio acessando os detalhes dos subdomínios.

Todos os registros de formato TXT do subdomínio selecionado são exibidos nessa tela, com as informações na coluna “Valor” das configurações. Para excluir um registro DMARC, BIMI ou TXT do Google, clique no botão de reticências e selecione Excluir. Também é possível editar registros DMARC e BIMI, se necessário.

![](assets/txt-records.png)
