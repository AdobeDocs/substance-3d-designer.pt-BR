---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/technical-issues/crash-when-rendering-graphs.html"
breadcrumb-title: ''
description: Solucione problemas ao renderizar gráficos no Substance 3D Designer e encontre soluções para evitá-los.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Crash when rendering graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Falha ao renderizar gráficos
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 3%

---


# Falha ao renderizar gráficos

Esta página lista as falhas que ocorrem durante o processo de renderização do gráfico no Substance 3D Designer e oferece etapas de solução de problemas para cada uma.

## TDR (somente Windows)

<b>[![(error)](../../assets/error.svg)](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) Problema</b>

O timer do <b>Timeout Detection &amp; Recovery (TDR)</b> do sistema é *muito curto* para permitir que o Substance 3D Designer conclua seus cálculos atuais antes que o driver gráfico seja *reiniciado*.

Os cálculos executados pelo Substance 3D Designer podem ser muito intensivos e usam os drivers gráficos em um grau que *não responde* ao sistema operacional por algum tempo.\
Como medida de estabilidade e segurança, o sistema operacional *reinicia o driver gráfico*, encurtando os cálculos e resultando no *travamento* do Substance 3D Designer.

<b>![(tick)](../../assets/check.svg) Etapas recomendadas</b>

Os valores do temporizador TDR precisam ser *aumentados* para evitar essas falhas. Você pode fazer isso seguindo as instruções nesta [página](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash) da documentação da Substance 3D Painter, que também se aplicam ao Substance 3D Designer.
