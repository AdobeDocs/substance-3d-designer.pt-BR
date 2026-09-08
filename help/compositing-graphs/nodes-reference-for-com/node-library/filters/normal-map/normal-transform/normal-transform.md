---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
breadcrumb-title: ''
description: Use o nó Transformação normal para aplicar transformações a mapas normais, preservando as direções vetoriais corretamente.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformação normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# Transformação normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/normal-transform.png){width="128px"}

<b>Entrada:</b> Filtros > Mapa normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Semelhante ao nó 2D de Transformação atômica, isso permite a transformação de Normalmaps sem quebrar o espaço Tangent, em vez disso, é recalculado na hora, resultando em Normalmaps sempre corretos.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Matrix2x2</b> <i>(Matriz de Transformação):</i> | Gire ou dimensione a entrada. |
| <b>Deslocamento</b> <i>-0.5 - 0.5</i> | Move ou traduz o resultado. Quando o controle de Transformação está presente, o resultado pode ser modificado ao interagir diretamente com a tela. |
| <b>Formato Normal</b> <i>DirectX, OpenGL</i> | Alternar entre Formatos de mapa normais diferentes (inverte o canal verde) |
