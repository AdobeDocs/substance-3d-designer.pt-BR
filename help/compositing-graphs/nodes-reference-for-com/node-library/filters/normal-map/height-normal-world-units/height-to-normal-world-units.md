---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-to-normal-world-units.html"
breadcrumb-title: ''
description: Use o nó Height para unidades do mundo normal para converter mapas de altura em mapas normais usando o dimensionamento de unidades do mundo para obter detalhes precisos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height to Normal World Units
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height para unidades do mundo normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---


# Height para unidades do mundo normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/normal-hq.png){width="128px"}

<b>Entrada:</b> Filtros > Mapa normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Um nó de conversão avançado Height-para-normal que faz uso de unidades do mundo real durante a conversão.

Útil para quando você conhece as dimensões do mapa de altura de origem e deseja executar a conversão mais precisa, como ao trabalhar com material digitalizado.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Tamanho da superfície (cm)</b> <i>0.0 - 1000.0</i> | Dimension do Heightmap de entrada. |
| <b>Profundidade de Height (cm)</b> <i>0.0 - 100.0</i> | Profundidade máxima de detalhes de Heightmap. |
| <b>Formato Normal</b> <i>OpenGL, DirectX</i> | Alterna entre diferentes formatos de Mapas Normais (inverte o canal verde). |
| <b>Amostragem</b> <i>Padrão, Sobel</i> | Alterna entre dois modos de amostragem determinando a precisão. |
