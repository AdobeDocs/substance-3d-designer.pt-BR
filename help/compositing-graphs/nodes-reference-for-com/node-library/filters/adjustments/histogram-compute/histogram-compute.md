---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-compute.html"
breadcrumb-title: ''
description: Use o nó Cálculo do histograma para calcular os dados do histograma a partir das texturas para análise e processamento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram compute
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Computação de histograma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 1%

---


# Computação de histograma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Computação do histograma: ícone](../../../../../../assets/histogram_compute.png "Computação do histograma: ícone"){width="200px"}

<b>Entrada:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Calcula o histograma de uma imagem em tons de cinza.

O histograma é codificado como uma linha de pixels em uma imagem, onde cada valor de pixel é a *população* do valor de cor correspondente à posição de pixel no eixo X.\
Por exemplo, um valor de pixel de 75 em (0,25, 0) significa que há 75 pixels com o valor de cor 0,25 na imagem.

</td>
</tr>
</table>

O nó também gera a *função de distribuição cumulativa* (CDF) computada para a imagem.

Ferramentas personalizadas podem ser criadas usando os dados computados pelo nó, como máscaras personalizadas, conforme mostrado abaixo na seção “Exemplos”.

>[!IMPORTANT]
>
> Todos os valores fora do intervalo [0,1] são bloqueados, portanto o histograma pode não ser preciso para imagens HDR.

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Tons de cinza</i> PRIMÁRIO | A imagem para a qual o histograma deve ser calculado. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Histograma</b> <i>Tons de cinza</i> | O histograma computado para a imagem de entrada, codificado como uma linha de pixels onde cada valor de pixel é a *população* do valor de cor correspondente à posição de pixel no eixo X.   Por exemplo, um valor de pixel de 75 em (0,25, 0) significa que há 75 pixels com o valor de cor 0,25 na imagem. |
| <b>CDF</b> <i>Tons de cinza</i> | O resultado da *função de distribuição cumulativa* (CDF) computada para a imagem, codificada em uma linha de pixels onde cada pixel é a soma de todos os valores de pixel à sua esquerda.   Essa soma é então *normalizada* em relação ao número total de pixels na imagem. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Resolução do histograma</b> *Inteiro* | A largura do histograma. Um valor mais alto permite uma melhor distribuição de valores.   As resoluções disponíveis são, em pixels: 256, 512, 1024, 2048, 4096 |

## Exemplos

![Computação de histograma: Exemplo 1](../../../../../../assets/histogram_compute_example_1.jpg "Computação de histograma: Exemplo 1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/histogram_compute_example_2_before.jpg" alt="histogram_compute_example_2_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/histogram_compute_example_2_after.jpg" alt="histogram_compute_example_2_after">
      <br><i>Depois</i>
    </td>
  </tr>
</table>
