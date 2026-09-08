---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/quad-transform-on-path.html"
breadcrumb-title: ''
description: Use o nó Transformo Quad no caminho para aplicar transformações quadráticas a elementos ao longo de curvas de caminho.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Quad Transform on Path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformo Quad no Caminho
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4034c519f3367597b09165c267379fd8ac4e7062
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# Transformo Quad no Caminho

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](../../../../../../assets/quad-transform-on-paths-icon.png "Ícone de nó")

<b>Ferramentas de Spline e Caminho </b> > Ferramentas de Caminho

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Deforme um caminho usando 4 alças.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Caminhos</b> <i>Cor</i> | Uma lista de caminhos de segmentos codificados. Conecte esta entrada ao resultado de uma [Máscara para Caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) ou a outro nó de processamento de *Caminho*. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Caminhos</b> <i>Cor</i> | Os Caminhos transformados. Você pode usar [Visualizar Caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) para ter uma ideia do que o resultado representa, usar outro nó de processamento de Caminhos ou inseri-lo em um [Caminhos para Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) para processá-lo posteriormente como Splines. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>p00</b> <i>Precisão decimal 2</i> | A posição da alça superior esquerda. |
| <b>p01</b> <i>Precisão decimal 2</i> | A posição da alça superior direita. |
| <b>p02</b> <i>Precisão decimal 2</i> | A posição da alça inferior esquerda. |
| <b>p03</b> <i>Precisão decimal 2</i> | A posição da alça inferior direita. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/QuadTransformOnPaths-Variant1-After.jpg" alt="QuadTransformOnPaths-Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/QuadTransformOnPaths-Variant2-After.jpg" alt="QuadTransformOnPaths-Variant2-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 1](../../../../../../assets/QuadTransformOnPaths-Demo2.gif "Exemplo de nó 1")

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](../../../../../../assets/QuadTransformOnPaths-Demo1.gif "Exemplo de nó 2")

</td>
</tr>
</table>
