---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-grayscale-color.html"
breadcrumb-title: ''
description: Use o nó Cor de Flood Fill para tons de cinza a fim de preencher regiões conectadas com cores em tons de cinza para criar padrões monocromáticos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to GrayscaleColor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill para Tons de cinza
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---


# Flood Fill para tons de cinza/cor

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-grayscale-color.resources/floodfill-to-grayscale.png){width="128px"}

![](flood-fill-to-grayscale-color.resources/floodfill-to-color.png){width="128px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Usa dados de Flood Fill para gerar amostras de valores de tons de cinza ou de cores. Diferentemente de [Flood Fill para Tons de Cinza Aleatórios](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md), esses dois nós permitem mais controle para definir a variação exata e os tons, com um mapa de entrada extra adicional para determinar o valor base a ser aleatório por célula.

É um sistema poderoso para dar a cada célula um valor ou cor única, mas ainda manter o controle e baseá-lo em uma entrada predeterminada.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Flood Fill</b> <i>Entrada de cores</i> |  |
| <b>Entrada em Tons de Cinza/Cores</b> <i>Entrada em Tons de Cinza/Cores</i> |  |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Ajuste de luminância/cor</b> <i>-1.0 - 1.0</i> | Defina o valor de polarização ou base para o nó. Quando uma entrada Tons de cinza ou Cor é usada, isso é usado para alterar esse valor inicial como ponto de partida. |
| <b>Luminância/Cor Aleatória</b> <i>-1.0 - 1.0</i> | Defina o valor da variação. |
