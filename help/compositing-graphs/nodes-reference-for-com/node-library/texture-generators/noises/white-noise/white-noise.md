---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/white-noise.html"
breadcrumb-title: ''
description: Use o nó Ruído branco para gerar padrões de ruído branco para criar variações de textura e efeitos aleatórios.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > White noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruído branco
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 5%

---


# Ruído branco

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ruído branco - Ícone](white-noise.resources/white_noise_v2.png "Ruído branco - Ícone"){width="200px"}

<b>Entrada:</b> geradores de textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera um ruído branco usando um dos três métodos disponíveis para definir diferentes formas de histograma: uniforme, gaussiano e triângulo.

</td>
</tr>
</table>

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Saída</b> <i>Tons de cinza</i> | O ruído gerado como bitmap em tons de cinza. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Distribuição de ruído</b> <i>Inteiro</i> | O método de distribuição dos ingredientes para definir uma forma de histograma:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Uniforme:</i> Um histograma simples.</li> <li data-preserve-html="true"><i>Gaussiano:</i> um histograma que representa uma distribuição normal, semelhante a uma curva em forma de sino.</li> <li data-preserve-html="true"><i>Triângulo:</i> Um histograma triangular.</li> </ul> |
| <b>Desordem</b> <i>Flutuante</i> | Desloca os ingredientes do ruído.    Isso pode ser usado para animar o ruído. |
| <b>Velocidade do distúrbio</b> <i>Flutuante</i> | Ajusta a distância de deslocamento aplicada pelo parâmetro <b>Desordem</b>.    Isso pode ser usado para controlar a velocidade de deslocamento ao animar o ruído. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ruído branco - Exemplo 1](white-noise.resources/white_noise_v2_1.png "Ruído branco - Exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ruído branco - Exemplo 2](white-noise.resources/white_noise_v2_speed0.6_aniso0.gif "Ruído branco - Exemplo 2"){zoomable="yes"}

</td>
</tr>
</table>
