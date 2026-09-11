---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/median-filter-grayscale.html"
breadcrumb-title: ''
description: Use o nó Tons de cinza do filtro mediano para reduzir o ruído e preservar as bordas em texturas em tons de cinza.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Median filter grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tons de cinza do filtro mediano
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5efb14d81ad72b1982785319e446d7eb318c9a03
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%

---


# Tons de cinza do filtro mediano

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Escala de cinza de filtro mediano: ícone](median-filter-grayscale.resources/MedianFilter_Icon_Grayscale.png "Escala de cinza de filtro mediano: ícone")

<b>Entrada:</b> Filtros > Desfoques

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Esse filtro suaviza o ruído em uma imagem preservando as arestas.

Para cada pixel, o nó calcula um valor de tons de cinza de acordo com o valor mediano dos vizinhos do pixel.

</td>
</tr>
</table>

>[!NOTE]
>
> Consulte também [Cor do filtro mediano](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/median-filter-color/median-filter-color.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Tons de cinza</i> | A imagem em tons de cinza à qual o filtro deve ser aplicado. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Saída</b> <i>Tons de cinza</i> | A imagem em tons de cinza calculada aplicando-se o filtro à imagem em tons de cinza de entrada. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Tamanho do kernel</b> *Inteiro* | Um kernel é um grupo específico de valores usados nos cálculos de um filtro. Nesse contexto, são os valores dos pixels vizinhos.<br><br>Para cada pixel, o filtro pega todos os vizinhos ao redor desse pixel em um kernel quadrado e calcula o valor mediano de todos os vizinhos.<br><br>Este parâmetro controla o tamanho desse kernel quadrado, em pixels. Um kernel maior resulta em um efeito de suavização mais forte e de maior alcance, ao custo de alguns detalhes.<br><br>*- 3x3:* um kernel com 3 pixels de largura e 3 pixels de altura, totalizando 8 pixels vizinhos.<br>*- 5x5:* um kernel com 5 pixels de largura e 5 pixels de altura, totalizando 24 pixels vizinhos. |
| <b>Tipo de filtro</b> *Inteiro* | O cálculo aplicado aos vizinhos amostrados no kernel.<br><br>*- Mediana:* Use o valor mediano de todos os vizinhos diretamente.<br>*- MLMAD:* Representa &#39;Mediana do Menor Desvio Absoluto Mediano&#39;. O desvio explica o quão diferente um valor é da mediana. Em vez de usar diretamente o valor mediano que pode ser distorcido por um pixel de exceção com alto desvio, o método MLMAD usa a mediana de todos os desvios. Esse método resulta em um efeito de suavização mais forte, que pode nivelar as áreas de acordo com o tamanho do núcleo. |

## Exemplos

<table>
  <tr>
    <td>
      <img src="median-filter-grayscale.resources/MedianFilter_Variant2A.png" alt="MedianFilter_Variant2A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="median-filter-grayscale.resources/MedianFilter_Variant2B.png" alt="MedianFilter_Variant2B">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="median-filter-grayscale.resources/MedianFilter_Variant4A.png" alt="MedianFilter_Variant4A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="median-filter-grayscale.resources/MedianFilter_Variant4B.png" alt="MedianFilter_Variant4B">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="median-filter-grayscale.resources/MedianFilter_Variant1A.png" alt="MedianFilter_Variant1A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="median-filter-grayscale.resources/MedianFilter_Variant1B.png" alt="MedianFilter_Variant1B">
      <br><i>Depois</i>
    </td>
  </tr>
</table>
