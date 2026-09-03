---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale.html"
breadcrumb-title: ''
description: Use o nó Escala de cinza do Mapeador UV para mapear texturas em tons de cinza ao longo de splines para geração de textura processual.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Escala de cinza do mapeador UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# Escala de cinza do mapeador UV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](uv-mapper-grayscale.resources/uv-mapper-grayscale-01.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Mapeia a imagem em tons de cinza de entrada usando as coordenadas fornecidas na entrada UV.

</td>
</tr>
</table>

>[!NOTE]
>
> Consulte também [Cor do Mapeador UV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-color/uv-mapper-color.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>UV</b> <i>Cor</i> | Coordenadas de imagem codificadas nos canais vermelho (U) e verde (V) de uma imagem colorida. |
| <b>Entrada</b> <i>Cor</i> | A imagem em tons de cinza que deve ser mapeada para as coordenadas fornecidas na entrada UV. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Saída</b> <i>Cor</i> | O resultado do mapeamento da imagem de entrada usando as coordenadas UV de entrada, como uma imagem em tons de cinza. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-grayscale.resources/uv-mapper-grayscale-02.jpg" alt="UVMapper-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="uv-mapper-grayscale.resources/uv-mapper-grayscale-03.jpg" alt="UVMapperGrayscale-Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-grayscale.resources/uv-mapper-grayscale-04.jpg" alt="UVMapper-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="uv-mapper-grayscale.resources/uv-mapper-grayscale-05.jpg" alt="UVMapper-Variant2-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![Exemplo de nó 1](uv-mapper-grayscale.resources/uv-mapper-grayscale-06.jpg "Exemplo de nó 1")
