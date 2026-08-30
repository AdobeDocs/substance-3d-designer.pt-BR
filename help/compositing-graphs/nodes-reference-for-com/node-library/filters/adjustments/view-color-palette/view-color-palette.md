---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/view-color-palette.html"
breadcrumb-title: ''
description: Use o nó Exibir paleta de cores para visualizar os dados da paleta de cores extraídos das texturas para análise.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > View Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Exibir paleta de cores
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---


# Exibir paleta de cores

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone Quantizar Cor](view-color-palette.resources/ViewColorPalette.png "ícone Quantizar Cor"){width="200px"}

<b>Entrada:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Empacota uma paleta de cores em um quadrado ou retângulo para visualizá-la mais facilmente na Exibição de gráfico ou na Exibição 2D.\
A embalagem visa deixar o menor número possível de espaços vazios.

</td>
</tr>
</table>

A ordem das cores na paleta é preservada, com as cores fluindo da esquerda para a direita e de cima para baixo de forma semelhante à quebra de texto.

Este nó pode ser usado para visualizar as paletas produzidas pelos seguintes nós: [Quantizar cor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [Criar paleta de cores](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md), [Modificar paleta de cores](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Paleta</b> <i>Cor</i> PRIMÁRIA | Uma lista ordenada de cores de RGB codificadas como uma linha de pixels. A paleta pode conter no máximo 256 cores.   Esta é a paleta que o nó empacota e renderiza. |
| <b>Quantidade de cores da paleta</b> <i>Inteiro</i> | A quantidade de cores armazenadas na paleta.   Se esse número não corresponder à quantidade real de cores na entrada da imagem da “Paleta”, a visualização poderá estar incompleta ou ter mais slots em branco do que o absolutamente necessário. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Saída</b> <i>Cor</i> | A visualização da paleta compactada. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exibir paleta de cores: exemplo 1](view-color-palette.resources/view_color_palette_example_1.png "Exibir paleta de cores: exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Exibir paleta de cores: exemplo 2](view-color-palette.resources/view_color_palette_example_2.png "Exibir paleta de cores: exemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exibir paleta de cores: exemplo 3](view-color-palette.resources/view_color_palette_example_3.png "Exibir paleta de cores: exemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Exibir paleta de cores: exemplo 4](view-color-palette.resources/view_color_palette_example_4.png "Exibir paleta de cores: exemplo 4"){zoomable="yes"}

</td>
</tr>
</table>
