---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/median-filter-color.html"
breadcrumb-title: ''
description: Use o nó Cor do filtro mediano para reduzir o ruído e preservar as bordas em texturas coloridas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Median filter color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cor do filtro mediano
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---


# Cor do filtro mediano

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Cor do filtro mediano: ícone](median-filter-color.resources/MedianFilter_Icon_Color.png "Cor do filtro mediano: ícone")

<b>Entrada:</b> Filtros > Desfoques

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Esse filtro suaviza o ruído em uma imagem preservando as arestas.

Para cada pixel, o nó calcula um valor de cor de acordo com o valor mediano dos vizinhos do pixel.

</td>
</tr>
</table>

>[!NOTE]
>
> Consulte também [Escala de cinza do filtro Mediana](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/median-filter-grayscale/median-filter-grayscale.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Cor</i> | A imagem colorida à qual o filtro deve ser aplicado. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Saída</b> <i>Cor</i> | A imagem colorida calculada com a aplicação do filtro à imagem colorida de entrada. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Tamanho do kernel</b> *Inteiro* | Um kernel é um grupo específico de valores usados nos cálculos de um filtro. Nesse contexto, são os valores dos pixels vizinhos.<br><br>Para cada pixel, o filtro pega todos os vizinhos ao redor desse pixel em um kernel quadrado e calcula o valor mediano de todos os vizinhos.<br><br>Este parâmetro controla o tamanho desse kernel quadrado, em pixels. Um kernel maior resulta em um efeito de suavização mais forte e de maior alcance, ao custo de alguns detalhes.<br><br>*- 3x3:* um kernel com 3 pixels de largura e 3 pixels de altura, totalizando 8 pixels vizinhos.<br>*- 5x5:* um kernel com 5 pixels de largura e 5 pixels de altura, totalizando 24 pixels vizinhos. |
| <b>Tipo de filtro</b> *Inteiro* | O cálculo aplicado aos vizinhos amostrados no kernel.<br><br>*- Mediana:* Use o valor mediano de todos os vizinhos diretamente.<br>*- MLMAD:* Representa &#39;Mediana do Menor Desvio Absoluto Mediano&#39;. O desvio explica o quão diferente um valor é da mediana. Em vez de usar diretamente o valor mediano que pode ser distorcido por um pixel de exceção com alto desvio, o método MLMAD usa a mediana de todos os desvios. Esse método resulta em um efeito de suavização mais forte, que pode nivelar as áreas de acordo com o tamanho do núcleo. |
| <b>Afetar alfa</b> *Booleano* | Controla se o filtro deve ser aplicado ao canal alfa da imagem. Quando *Verdadeiro*, o canal alfa não é alterado. |

## Exemplos

<table>
  <tr>
    <td>
      <img src="median-filter-color.resources/MedianFilter_Variant2A.png" alt="MedianFilter_Variant2A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="median-filter-color.resources/MedianFilter_Variant2B.png" alt="MedianFilter_Variant2B">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="median-filter-color.resources/MedianFilter_Variant3A.png" alt="MedianFilter_Variant3A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="median-filter-color.resources/MedianFilter_Variant3B.png" alt="MedianFilter_Variant3B">
      <br><i>Depois</i>
    </td>
  </tr>
</table>
