---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-to-spline.html"
breadcrumb-title: ''
description: Use o nó Caminhos para spline para converter dados de caminho em splines para uso com nós baseados em spline.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths to Spline
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Caminhos para a spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4034c519f3367597b09165c267379fd8ac4e7062
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# Caminhos para a spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](../../../../../../assets/paths-to-splines-icon.png "Ícone de nó")

<b>Ferramentas de Spline e Caminho </b> > Ferramentas de Caminho

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Converte um caminho em splines que podem ser visualizadas usando um nó de [Renderização de spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-render/spline-render.md) e processadas usando [nós de spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-tools.md).

</td>
</tr>
</table>

>[!NOTE]
>
> As splines são curvas e, portanto, não podem manter a nitidez dos caminhos. Você encontrará um pouco de suavização nas formas ao converter caminhos em splines.

>[!TIP]
>
> Este nó pode ser usado após o nó [Mascarar para Caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) para formar uma cadeia que converta uma máscara em splines.

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Caminhos</b> <i>Cor</i> | Uma lista de caminhos de segmentos codificados. Conecte esta entrada ao resultado de uma [Máscara para Caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) ou a outro nó de processamento de Caminho. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Cordas de spline</b> <i>Cor</i> | As coordenadas dos pontos das linhas divisórias de entrada codificadas nos canais RGBA de uma imagem colorida:<br><b>R</b> - posição X<br><b>G</b> - posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br> * Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br> * Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> <i>Cor</i> | Dados adicionais das splines de entrada codificadas nos canais RGBA de uma imagem <b>colorida</b>:<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usadas<br><b>A</b> - Não Usadas |
| <b>Valor da spline</b> <i>Inteiro</i> | O número de splines de entrada. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Precisão de Splines</b> <i>Inteiro</i> | O logaritmo de base 2 (log2) do número de vértices amostrados em cada caminho da entrada de Caminhos para construir a spline correspondente. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant1-Before.jpg" alt="PathsToSpline-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant1-After.jpg" alt="PathsToSpline-Variant1-After">
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
      <img src="../../../../../../assets/PathsToSpline-Variant2-After.jpg" alt="PathsToSpline-Variant2-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
