---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-render.html"
breadcrumb-title: ''
description: Use o nó Renderização do histograma para visualizar dados do histograma como uma textura para análise e depuração.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Renderização de histograma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 25c39c29f26db98b103665dba13e7619ed624d0b
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# Renderização de histograma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone Anisotrópico de Escala de Cinza Kuwahara](histogram-render.resources/histogram_render.png "Ícone Anisotrópico de Escala de Cinza Kuwahara"){width="200px"}

<b>Entrada:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Desenha o histograma de uma imagem em tons de cinza.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Tons de cinza</i> PRIMÁRIO | A imagem para a qual o histograma deve ser desenhado. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Saída</b> <i>Tons de cinza</i> | A visualização do histograma foi calculada a partir da imagem de entrada. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Resolução do histograma</b> *Inteiro* | A largura do histograma. Um valor mais alto permite uma melhor distribuição de valores.   As resoluções disponíveis são, em pixels: 256, 512, 1024, 2048, 4096 |
| <b>Escala automática</b> *Booleano* | Quando &#39;Verdadeiro&#39;, remapeia o histograma para usar o height completo da imagem.   Quando &#39;Falso&#39;, cada coluna usa quantos pixels em height houver ocorrências de um valor na imagem de entrada. |
| <b>Escala</b> *Precisão decimal* | Dimensiona o histograma verticalmente, onde o valor 1 é o height completo do histograma. |
| <b>Amostragem</b> *Inteiro* | O método de filtrar a imagem do histograma, que afeta o resultado quando a resolução do histograma e a resolução de renderização são incompatíveis:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Bilinear:</b> aplica filtragem bilinear ao histograma, resultando em pontos interpolados</li> <li data-preserve-html="true"><b>Mais próximo:</b> faz a amostragem do pixel mais próximo sem filtragem, resultando em etapas simples</li> </ul> |
| <b>Virar eixo Y</b> *Booleano* | Quando &#39;Verdadeiro&#39;, espelha o histograma verticalmente. |

## Exemplos

![Renderização do histograma: Exemplo 1](histogram-render.resources/histogram_render_example_1.png "Renderização do histograma: Exemplo 1"){zoomable="yes"}

![Renderização do histograma: Exemplo 2](histogram-render.resources/histogram_render_example_2.png "Renderização do histograma: Exemplo 2"){zoomable="yes"}
