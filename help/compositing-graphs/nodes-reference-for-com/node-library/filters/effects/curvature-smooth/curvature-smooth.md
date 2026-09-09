---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-smooth.html"
breadcrumb-title: ''
description: Use o nó Suavização da curvatura para gerar mapas de curvatura suaves a partir de mapas de altura para a extração de detalhes da superfície.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Smooth
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Suavização de curvatura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 07f136ebd89fbe737b6c042f1275bd348b2be514
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 1%

---


# Suavização de curvatura

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó Suave de Curvatura](curvature-smooth.resources/CurvatureSmooth.png "Ícone de nó Suave de Curvatura"){width="200px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Calcula a curvatura de uma superfície descrita por um mapa normal.

Um mapa de curvatura representa as áreas côncavas e convexas de uma superfície.\
As áreas planas são 50% cinza. As áreas convexas são mais brilhantes, enquanto as áreas côncavas são mais escuras.

</td>
</tr>
</table>

As áreas côncavas e convexas também são divididas em suas próprias saídas, para facilitar a seleção ou mascaramento de áreas com base nessas características.

>[!TIP]
>
> Procure uma versão mais nítida na [Curvatura](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md) ou na [Curvatura Sobel](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md) se precisar de mais opções.

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Normal</b> <i>Cor</i> <b>PRIMÁRIO</b> | O mapa normal que descreve a superfície cuja curvatura deve ser calculada. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Tons de cinza</i> | O mapa de curvatura calculado do mapa normal de entrada.   As áreas planas são 50% cinza. As áreas convexas são mais brilhantes, enquanto as áreas côncavas são mais escuras. |
| <b>Convexidade</b> <i>Tons de cinza</i> | O mapa de convexidade foi calculado a partir do mapa normal de entrada.   Quanto mais convexa for uma área, mais brilhante ela ficará no mapa.  As áreas planas ou côncavas são pretas. |
| <b>Concavidade</b> <i>Tons de cinza</i> | O mapa de concavidade calculado a partir do mapa normal de entrada.   Quanto mais côncava uma área, mais brilhante ela fica no mapa.  As áreas planas ou convexas são pretas. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Formato normal</b> *Inteiro* | O formato do mapa normal de entrada. Inverte efetivamente o canal de verde.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX:</b> o eixo Y aponta para cima</li> <li data-preserve-html="true"><b style="">OpenGL:</b> o eixo Y aponta para baixo</li> </ul> |

## Exemplos

<table>
  <tr>
    <td>
      <img src="curvature-smooth.resources/curvature_smooth_example_1_before.jpg" alt="curvature_Smoke_example_1_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="curvature-smooth.resources/curvature_smooth_example_1_after.jpg" alt="curvature_suave_example_1_after">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Curvatura suave: Exemplo 2](curvature-smooth.resources/curvature_smooth_example_2.jpg "Curvatura suave: Exemplo 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Curvatura suave: Exemplo 3](curvature-smooth.resources/curvature_smooth_example_3.jpg "Curvatura suave: Exemplo 3"){zoomable="yes"}

</td>
</tr>
</table>

<table>
  <tr>
    <td>
      <img src="curvature-smooth.resources/curvature_smooth_example_4_before.jpg" alt="curvature_Smoke_example_4_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="curvature-smooth.resources/curvature_smooth_example_4_after.jpg" alt="curvature_Smoke_example_4_after">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Curvatura suave: exemplo 4](curvature-smooth.resources/curvature_smooth_example_5.jpg "Curvatura suave: exemplo 4"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Curvatura suave: exemplo 5](curvature-smooth.resources/curvature_smooth_example_6.jpg "Curvatura suave: exemplo 5"){zoomable="yes"}

</td>
</tr>
</table>
