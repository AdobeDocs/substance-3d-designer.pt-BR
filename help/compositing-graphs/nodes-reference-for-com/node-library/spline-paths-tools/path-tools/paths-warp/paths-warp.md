---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-warp.html"
breadcrumb-title: ''
description: Use o nó Distorção de caminhos para distorcer texturas ao longo de curvas de caminho para criar padrões curvos e orgânicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Distorção de caminhos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4034c519f3367597b09165c267379fd8ac4e7062
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# Distorção de caminhos

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](../../../../../../assets/paths-warp-icon.png "Ícone de nó")

<b>Ferramentas de Spline e Caminho </b> > Ferramentas de Caminho

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Deforme os Caminhos de entrada de acordo com a <b>Entrada de gradiente</b>. (Mesmo efeito que o nó [Distorcer](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md).)

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Caminhos</b> <i>Cor</i> | Uma lista de caminhos de segmentos codificados. Conecte esta entrada ao resultado de uma [Máscara para Caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) ou a outro nó de processamento de Caminho. |
| <b>Entrada de gradiente</b> <i>Tons de cinza</i> | A entrada do tipo height que controla a quantidade e a direção da distorção. (Mesmo efeito que o nó [Distorcer](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md).) |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Caminhos</b> <i>Cor</i> | Os caminhos transformados. Você pode usar [Visualizar Caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) para ter uma ideia do que o resultado representa, usar outro nó de processamento de Caminhos ou inseri-lo em um [Caminhos para Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) para processá-lo posteriormente como Splines. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Intensidade</b> <i>Flutuante</i> | O parâmetro <b>Intensidade</b> define a intensidade da distorção. |
| <b>Número de etapas</b> <i>Inteiro</i> | Use um valor mais alto para distorcer os caminhos de entrada em vários incrementos pequenos.<br>Isso pode impedir que o caminho se cruze, especialmente ao usar valores altos de <b>Intensidade</b>. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/PathsWarp-Variant1-After.jpg" alt="PathsWarp-Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/PathsWarp-Variant2-After.jpg" alt="PathsWarp-Variant2-After">
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

![Exemplo de nó 1](../../../../../../assets/PathsWarp-Demo1.gif "Exemplo de nó 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
