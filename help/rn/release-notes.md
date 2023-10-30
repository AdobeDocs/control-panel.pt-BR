---
title: Versão mais recente
description: Esta página lista todos os novos recursos e melhorias do Painel de controle
feature: Control Panel, Release Notes
role: Admin
level: Experienced
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 100%

---

# Versão mais recente {#control-panel-releases}

Esta página lista todos os novos recursos e melhorias do Painel de controle.

## Outubro de 2023 {#october-2023}

**Interface**

* O Painel de controle agora está disponível em outros idiomas. [Saiba mais](../discover/using/discovering-the-interface.md#supported-languages-languages)

**Monitoramento de perfis ativos**

* Agora é possível monitorar o número de perfis ativos aos quais você está atribuído na sua organização e a contagem total de perfis usados na organização em todas as instâncias, se estiver usando várias instâncias. [Saiba mais](../performance-monitoring/using/active-profiles-monitoring.md)

**Registros DMARC**

* Agora, vários endereços de email podem receber emails de relatórios agregados e de relatório de falhas. [Saiba mais](../subdomains-certificates/using/dmarc.md)
* Foram feitas alterações em caso de ambos os registros, DMARC e BIMI, existirem em um subdomínio:

   * Os registros DMARC não podem ser excluídos. Se quiser excluir um, será necessário excluir o registro BIMI primeiro.
   * Os registros DMARC podem ser editados, mas o downgrade da política para &quot;Nenhum&quot; não é permitido e seu valor percentual deve ser 100.

