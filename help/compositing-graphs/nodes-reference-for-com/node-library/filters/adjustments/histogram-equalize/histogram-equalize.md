---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-equalize.html"
breadcrumb-title: ''
description: Use o nó Equalização do histograma para redistribuir as intensidades de pixel para melhorar o contraste e o brilho.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram equalize
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Histograma equalizado
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---


# Histograma equalizado

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Equalização do histograma: ícone](histogram-equalize.resources/histogram-equalize-01.png "Equalização do histograma: ícone"){width="200px"}

<b>Entrada:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Equaliza o histograma para uma imagem em tons de cinza, ajustando efetivamente os valores da escala de cinza com o objetivo de obter uma distribuição igual.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Tons de cinza</i> PRIMÁRIO | A imagem para a qual o histograma deve ser equalizado. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Saída</b> <i>Tons de cinza</i> | A imagem resultante com a equalização do histograma aplicada. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Resolução do histograma</b> *Inteiro* | A largura do histograma. Um valor mais alto permite uma melhor distribuição de valores.   As resoluções disponíveis são, em pixels: 256, 512, 1024, 2048, 4096 |
| <b>Suavização do histograma</b> *Flutuante* | O histograma pode ser suavizado redistribuindo os valores em tons de cinza da imagem para equalizar a *diferença* entre cada valor.   Esse parâmetro ajusta a intensidade dessa suavização. |

## Exemplos

<table>
  <tr>
    <td>
      <img src="histogram-equalize.resources/histogram-equalize-02.jpg" alt="histogram_equalize_example_1_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="histogram-equalize.resources/histogram-equalize-03.jpg" alt="histogram_equalize_example_1_after">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

![Equalização do histograma: Exemplo 1](histogram-equalize.resources/histogram-equalize-04.png "Equalização do histograma: Exemplo 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="histogram-equalize.resources/histogram-equalize-05.jpg" alt="histogram_equalize_example_2_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="histogram-equalize.resources/histogram-equalize-06.jpg" alt="histogram_equalize_example_2_after">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

![Equalização do histograma: Exemplo 2](histogram-equalize.resources/histogram-equalize-07.png "Equalização do histograma: Exemplo 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="histogram-equalize.resources/histogram-equalize-08.jpg" alt="histogram_equalize_example_4_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="histogram-equalize.resources/histogram-equalize-09.jpg" alt="histogram_equalize_example_4_after">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

![Equalização do histograma: Exemplo 3](histogram-equalize.resources/histogram-equalize-10.png "Equalização do histograma: Exemplo 3"){zoomable="yes"}
