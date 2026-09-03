---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/warp.html"
breadcrumb-title: ''
description: Use o nó Distorcer para aplicar efeitos de distorção ao textura para criar efeitos de distorção e de deslocamento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Distorcer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 9%

---


# Distorcer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: Distorcer](warp.resources/warp-01.png "Nó atômico: Distorcer"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Desloca os valores de pixel na imagem de entrada de acordo com as inclinações calculadas a partir de uma entrada de gradiente separada, resultando em deformação.

Diferentemente da Deformação direcional, esse nó afasta uniformemente das áreas brancas, em uma direção definida pela inclinação ou gradiente da Entrada de gradiente.

</td>
</tr>
</table>

O nó pode ser um pouco complicado de trabalhar, pois o resultado do efeito é muito dependente da entrada de gradiente: pequenos ajustes ao gradiente podem fazer uma grande diferença visual com os mesmos valores de intensidade. Experimente o Contraste, a Luminância e a escala da Entrada de gradiente, bem como o controle deslizante de Intensidade neste nó.

Se você estiver familiarizado com Mapas normais, pode imaginar o funcionamento desse nó como sendo semelhante ao de converter a Entrada de gradiente em um [Mapa normal](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) e, em seguida, distorcer a Entrada base na direção definida pelos vetores de Mapa normal. Na verdade, essa mesma coisa pode ser obtida com a [Distorção de vetor](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md). Efeitos semelhantes também podem ser encontrados no [Desfoque de Inclinação](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md).

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Conectores de saída

</td>
<td style="border: 0;" valign="top">

### Exemplos

</td>
</tr>
</table>

## Parâmetros

|  |  |
| --- | --- |
| <b>Intensidade</b> *Flutuante* | Define a intensidade da distorção. |
| <b>Modo de filtragem de entrada</b> *Booleano* | Controla se a filtragem mais próxima ou bilinear é usada para obter amostra da Entrada. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Tons de Cinza/Cor* PRIMÁRIO | A imagem colorida ou em tons de cinza. |
| <b>Entrada de gradiente</b> *Tons de cinza* | A inclinação do gradiente da imagem de entrada em tons de cinza determina o efeito de distorção na imagem de saída. |

## Conectores de saída

|  |  |
| --- | --- |
| <b>Saída</b> *Tons de cinza/Cor* |  |

## Exemplos

*Em breve.*
