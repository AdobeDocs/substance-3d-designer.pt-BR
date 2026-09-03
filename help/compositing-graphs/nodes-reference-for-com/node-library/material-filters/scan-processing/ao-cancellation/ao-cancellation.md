---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/ao-cancellation.html"
breadcrumb-title: ''
description: Use o nó Cancelamento de AO para remover a oclusão ambiente dos materiais digitalizados para o processamento de textura limpa.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > AO Cancellation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cancelamento de AO
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 4%

---


# Cancelamento de AO

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](ao-cancellation.resources/ao-cancellation-01.png){width="128px"}

<b>Entrada:</b> Filtros Materiais > Processamento de materiais escaneados

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Este nó tenta remover qualquer informação de iluminação de Oclusão ambiente do mapa de Albedo (cor base), com base em uma entrada de mapa AO separada. Ele pode ser usado para garantir que as informações do seu Albedo sejam PBR corretas e na maior parte do tempo desprovidas de informações de iluminação (fortes).

Um nó útil para quando você tem um mapa de AO feito bake de uma malha digitalizada, ou, alternativamente, até mesmo um mapa de AO gerado a partir de informações de Height ou Normais.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Cancelamento de AO</b> <i>0.0 - 1.0</i> | Intensidade com a qual remover informações de iluminação. |
| <b>Saturação do AO</b> <i>0.0 - 1.0</i> | Compensação de (De)Saturação para áreas onde a iluminação é removida. Isso pode ser usado para retornar qualquer perda de cor em áreas mais escuras. |
