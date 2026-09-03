---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-color.html"
breadcrumb-title: ''
description: Use o nó Cor do mapeador UV para mapear texturas de cores ao longo das linhas para geração de textura processual.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cor do mapeador UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---


# Cor do mapeador UV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](uv-mapper-color.resources/uv-mapper-color-01.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Mapeia a imagem colorida de entrada usando as coordenadas fornecidas na entrada UV.

</td>
</tr>
</table>

>[!NOTE]
>
> Consulte também [Escala de cinza do Mapeador UV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale/uv-mapper-grayscale.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>UV</b> <i>Cor</i> | Coordenadas de imagem codificadas nos canais vermelho (U) e verde (V) de uma imagem colorida. |
| <b>Entrada</b> <i>Cor</i> | A imagem colorida que deve ser mapeada para as coordenadas fornecidas na entrada UV. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Saída</b> <i>Cor</i> | O resultado do mapeamento da imagem de entrada usando as coordenadas UV de entrada, como uma imagem colorida. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Cor do plano de fundo</b> <i>Flutuante4</i> | A cor de plano de fundo da imagem de saída.<br>O plano de fundo é visível nas áreas da imagem em que os UVs não estão definidos (ou seja, o valor é (0, 0, 0, 0)). |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-color.resources/uv-mapper-color-02.jpg" alt="UVMapper-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="uv-mapper-color.resources/uv-mapper-color-03.jpg" alt="UVMapper-Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-color.resources/uv-mapper-color-04.jpg" alt="UVMapper-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="uv-mapper-color.resources/uv-mapper-color-05.jpg" alt="UVMapperColor-Variant2-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![Nó no gráfico](uv-mapper-color.resources/uv-mapper-color-06.jpg "Nó no gráfico")
