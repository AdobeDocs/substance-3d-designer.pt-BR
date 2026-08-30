---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-normal-blender.html"
breadcrumb-title: ''
description: Use o nó Mesclador normal de Height para mesclar mapas normais e de height para combinar informações detalhadas da superfície.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height Normal Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Misturador normal do height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# Misturador normal do height

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-normal-blender.resources/height-normal-blender.png){width="128px"}

<b>Entrada:</b> Filtros > Mapa normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Um nó de atalho que mescla um Heightmap em tons de cinza em um Normalmap. A entrada do Height é convertida internamente em um Normalmap e, em seguida, mesclada corretamente com a entrada Normal.

Essa é uma maneira mais rápida de mesclar detalhes do que fazer isso manualmente com nós separados, mas você pode perceber que não há controle e refinamento para determinadas necessidades.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Height</b> <i>Entrada em tons de cinza</i> | Tons de cinza com os quais mesclar. |
| <b>Normal</b> <i>Entrada de cores</i> | Base Normalmap para mesclagem. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Intensidade normal</b> <i>0.0 - 16.0</i> | Intensidade da conversão normal da entrada do Height. |
| <b>Formato Normal</b> <i>DirectX, OpenGL</i> | Alterna entre diferentes formatos de Mapas Normais (inverte o canal verde). |
