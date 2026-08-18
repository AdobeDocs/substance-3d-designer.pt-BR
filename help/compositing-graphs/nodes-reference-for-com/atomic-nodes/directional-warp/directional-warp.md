---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/directional-warp.html"
breadcrumb-title: ''
description: Use o nó Distorção direcional para aplicar distorção direcional a texturas para criar efeitos de fluxo e movimento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Directional warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Distorção direcional
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 9%

---


# Distorção direcional

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: distorção direcional](../../../../assets/comp_directionalwarp_1.png "Nó atômico: distorção direcional"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Desloca os pixels em uma direção especificada de acordo com um mapa de intensidade, o que pode resultar em deformação.

Distorce uma entrada em uma direção definida pelo usuário, multiplicada por um mapa de Intensidade definido pelo usuário. Funciona de maneira semelhante a Distorcer, mas somente em uma direção específica.

</td>
</tr>
</table>

O nó Distorcer é um nó bastante simples, mas útil, que serve como uma boa base para outros efeitos mais avançados. Existem alternativas mais avançadas, como outros nós de interesse relacionados, como o [Desfoque de Inclinação](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md) e a [Distorção de vetor](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md).

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
| <b>Ângulo de distorção</b> *Flutuante* | Define o ângulo do efeito de distorção, em número de voltas. |
| <b>Modo de filtragem de entrada</b> *Booleano* | Controla se a filtragem mais próxima ou bilinear é usada para obter amostra da <b>Entrada</b>. |
| <b>Deslocamento do mapa de intensidade</b> *Flutuante* | Este valor é subtraído dos valores de imagem de <b>Entrada de intensidade</b>. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Tons de Cinza/Cor* PRIMÁRIO | A imagem de entrada em tons de cinza ou colorida na qual o efeito de distorção deve ser aplicado. |
| <b>Entrada de intensidade</b> *Tons de cinza* | A imagem em tons de cinza que define a quantidade de distorção que deve ser aplicada à imagem de <b>entrada</b>. |

## Conectores de saída

|  |  |
| --- | --- |
| <b>Saída</b> *Tons de cinza/Cor* |  |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Distorção Direcional - Exemplo 1](../../../../assets/dir-warp.gif "Distorção Direcional - Exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Distorção Direcional - Exemplo 2](../../../../assets/dir-warp02.gif "Distorção Direcional - Exemplo 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Distorção Direcional - Exemplo 3](../../../../assets/dir-warp03.gif "Distorção Direcional - Exemplo 3"){zoomable="yes"}

</td>
</tr>
</table>
