---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-color.html"
breadcrumb-title: ''
description: Use o nó Cor do mapeador UV para mapear texturas de cores ao longo das splines para a geração de texturas de procedimento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cor do mapeador UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---


# Cor do mapeador UV

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](../../../../../../assets/uv-mapper-color-icon.png "Ícone de nó")

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

## Conectores de entrada

<b>UV</b> Coordenadas de imagem *coloridas* codificadas nos canais vermelho (U) e verde (V) de uma imagem colorida.

<b>Entrada</b> *Cor* A imagem colorida que deve ser mapeada para as coordenadas fornecidas na entrada UV.

## Conectores de saída

<b>Saída</b> *Cor* O resultado do mapeamento da imagem de entrada usando as coordenadas UV de entrada, como uma imagem colorida.

## Parâmetros

<b>Cor do plano de fundo</b> *Flutuante4* A cor de plano de fundo da imagem de saída.\
O plano de fundo fica visível nas áreas da imagem em que os UVs não estão definidos (isto é, o valor é (0, 0, 0, 0)).

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant1-Before.jpg" alt="UVMapper-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant1-After.jpg" alt="UVMapper-Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant2-Before.jpg" alt="UVMapper-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/UVMapperColor-Variant2-After.jpg" alt="UVMapperColor-Variant2-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![Nó no gráfico](../../../../../../assets/UVMapperColor-Graph.jpg "Nó no gráfico")

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
