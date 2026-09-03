---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/apply-color-palette.html"
breadcrumb-title: ''
description: Use o nó Aplicar paleta de cores para remapear texturas usando uma paleta de cores para efeitos de cores estilizadas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Apply Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Aplicar paleta de cores
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---


# Aplicar paleta de cores

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone Quantizar Cor](apply-color-palette.resources/apply-color-palette-01.png "ícone Quantizar Cor"){width="200px"}

<b>Entrada:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Aplica as cores de uma paleta ordenada a uma imagem, usando um mapa de ID.

As cores são distribuídas por meio da correspondência dos índices no mapa de ID com os índices de cores da paleta.

Por exemplo, a cor #2 na paleta será aplicada a todos os pixels no mapa de ID com um valor de ID igual a 2.

Este nó pode ser usado em combinação com os seguintes nós: [Quantificar cor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md), [Criar paleta de cores](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md), [Modificar paleta de cores](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md), [Exibir paleta de cores](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>ID</b> <i>Tons de cinza</i> PRIMÁRIO | O mapa de IDs de entrada usado para distribuir as cores na paleta de entrada.   Um mapa de ID é uma imagem na qual os pixels que fazem parte de um todo (por exemplo, uma forma) têm o mesmo valor de identificação exclusivo. Nesse caso, o valor é um inteiro.   Um mapa de ID pode ser produzido usando um nó [Quantizar Cor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md). |
| <b>Paleta</b> <i>Cor</i> | Uma lista ordenada de cores de RGB codificadas como uma linha de pixels. A paleta pode conter no máximo 256 cores. Esta é a paleta que o nó mapeia para os índices do mapa de ID.   As paletas podem ser produzidas com um nó [Quantizar cor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md) e modificadas com um nó [Modificar paleta de cores](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/modify-color-palette/modify-color-palette.md). |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Saída</b> <i>Cor</i> | Resultado do mapeamento das cores da paleta para os índices do mapa de ID. |

## Exemplos

![Aplicar paleta de cores: exemplo 1](apply-color-palette.resources/apply-color-palette-02.png "Aplicar paleta de cores: exemplo 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="apply-color-palette.resources/apply-color-palette-03.jpg" alt="apply_color_palette_example_1_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="apply-color-palette.resources/apply-color-palette-04.jpg" alt="apply_color_palette_example_1_after">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

![Aplicar paleta de cores: exemplo 3](apply-color-palette.resources/apply-color-palette-05.png "Aplicar paleta de cores: exemplo 3"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="apply-color-palette.resources/apply-color-palette-06.jpg" alt="apply_color_palette_example_3_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="apply-color-palette.resources/apply-color-palette-07.jpg" alt="apply_color_palette_example_3_after">
      <br><i>Depois</i>
    </td>
  </tr>
</table>
