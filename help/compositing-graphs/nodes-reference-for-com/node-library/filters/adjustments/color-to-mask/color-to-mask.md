---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-to-mask.html"
breadcrumb-title: ''
description: Use o nó Cor para máscara para converter cores específicas em máscaras para criar efeitos seletivos de processamento e mascaramento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color to mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cor para máscara
user-guide-description: ''
user-guide-title: ''
source-git-commit: 49bf753c2fa3d673b519b3ed87cc8bc82616bee6
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 1%

---


# Cor para máscara

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Cor para máscara - Ícone](color-to-mask.resources/color_to_mask.png "Cor para máscara - Ícone"){width="200px"}

<b>Entrada:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Extrai uma máscara de tons de cinza das cores selecionadas em uma imagem colorida.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Cor</i> | A imagem de cor de entrada da qual uma máscara deve ser extraída com base em suas cores. |
| <b>Entrada de cores</b> <i>Cor</i>   *Disponível quando &#39;Usar entrada de cor&#39; estiver definido como &#39;Verdadeiro&#39;* | A imagem de cor de entrada usada para definir a cor de referência por pixel. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Saída</b> <i>Tons de cinza</i> | A máscara gerada como um bitmap em tons de cinza. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Usar entrada de cores</b> *Booleano* | Use uma imagem de entrada em vez de uma cor uniforme, para definir uma cor de referência por pixel.    A imagem de entrada é fornecida pela entrada de <b>Cores</b>. |
| <b>Cor</b> *Precisão decimal 3* *Disponível quando &#39;Usar entrada de cor&#39; estiver definido como &#39;Falso&#39;* | A cor uniforme de referência em torno da qual a seleção de cores deve ser executada. |
| <b>Limite</b> *Flutuante* | A distância até a cor de referência abaixo da qual as cores são selecionadas. |
| <b>Atenuação da seleção</b> *Flutuante* | Esmaecer a seleção de cores com base na distância até a cor de referência. |
| <b>Espaço de cores à distância</b> *Inteiro* | O processo Equalizar envolve comparar cores para determinar a distância entre elas. Determinados espaços de cores e algoritmos de distância são mais adequados para casos de uso específicos.   Essa lista suspensa permite selecionar o espaço de cores usado para comparar as cores:<ul data-preserve-html="true"> <li data-preserve-html="true"><b><i>RGB (Dados):</i></b> a cor é dividida nos canais Vermelho, Verde e Azul e distribuída diretamente ao longo desses eixos, sem considerar a percepção humana. Isso é adequado para imagens que contêm dados brutos.</li> <li data-preserve-html="true"><i>sRGB lineares (cor):</i> a cor é dividida nos canais vermelho, verde e azul e distribuída em uma relação linear com a intensidade da luz do pixel. Isso é adequado para imagens que podem ser visualizadas em telas.</li> <li data-preserve-html="true"><b><i>Luminância (Cor):</i></b> a cor é dividida em valores de Matiz, Croma e Luminância, em que apenas o valor de Luminância é usado na comparação. Isso é adequado para imagens que podem ser visualizadas em telas.</li> <li data-preserve-html="true"><i>Lab (Cor):</i> um espaço de cores perceptual padronizado, que distribui cores de forma que as cores que &#39;parecem&#39; próximas estejam realmente próximas no cubo. Isso é adequado para imagens que podem ser visualizadas em telas.</li> <li data-preserve-html="true"><i>Ângulo (Normal):</i> a cor é dividida nos eixos X, Y, Z de um vetor e comparada por meio de um produto pontilhado. Isso é adequado para imagens que possuem normais de espaço tangente.</li> </ul> |
| <b>Espessuras de distância</b> *Flutuante3* | O algoritmo de distância de cores Lab (DeltaE2000) apresenta determinados fatores de peso para cada valor de luminosidade, croma e matiz.   Valores mais baixos diminuirão a influência dos fatores no algoritmo de diferença de cores.   Como o olho geralmente aceita maiores diferenças na luminosidade (L) do que no croma (C) ou matiz (H), uma proporção padrão para (L:C:H) é (0,5:1:1). Uma proporção de 0,5:1:1 permitirá duas vezes mais diferença na luminosidade do que no croma ou matiz. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
