---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-sobel.html"
breadcrumb-title: ''
description: Use o nó Sobel normal para gerar mapas normais a partir de mapas de height usando a detecção de arestas Sobel para detalhes da superfície.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sobel normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---


# Sobel normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-sobel.resources/normal-sobel-01.png){width="128px"}

<b>Entrada:</b> Filtros > Mapa normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Converte uma entrada Heightmap em uma saída Normalmap. Uma versão um pouco mais avançada do [Nó Atômico Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md), esse nó usa amostragem Sobel em vez do método de amostragem padrão.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Intensidade</b> <i>0.0 - 3.0</i> | Intensidade dos normais convertidos. |
| <b>Formato Normal</b> <i>OpenGL, DirectX</i> | Alterna entre diferentes formatos de Mapas Normais (inverte o canal verde). |
