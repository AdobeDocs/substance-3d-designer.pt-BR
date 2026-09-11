---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/gaussian-spots-2.html"
breadcrumb-title: ''
description: Use o nó Manchas gaussianas 2 para gerar padrões de manchas gaussianas avançados para criar variações de textura orgânica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Gaussian spots 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Manchas gaussianas 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: a2d6381b9bf224008fa412ef70c9b63b9b2756e8
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 1%

---


# Manchas gaussianas 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Manchas gaussianas 2 - Ícone](gaussian-spots-2.resources/gaussian_spots_2.png "Manchas gaussianas 2 - Ícone"){width="200px"}

<b>Entrada:</b> geradores de textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma variação dos <b>pontos gaussianos</b> suaves ruídos.\
Baseado no nó [Ruído gaussiano](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md), com gradientes mais estreitos e frequências mais altas.

Veja também: [Manchas gaussianas 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-spots-1/gaussian-spots-1.md)

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
| <b>Escala</b> <i>Inteiro</i> | A subdivisão da grade usada para gerar os blocos de ruído.    Um valor mais alto resulta no desenho de mais ladrilhos e em um ruído mais denso. |
| <b>Desordem</b> <i>Flutuante</i> | Desloca os ingredientes do ruído.    Isso pode ser usado para animar o ruído. |
| <b>Velocidade do distúrbio</b> <i>Flutuante</i> | Ajusta a distância de deslocamento aplicada pelo parâmetro <b>Desordem</b>.    Isso pode ser usado para controlar a velocidade de deslocamento ao animar o ruído. |
| <b>anisotropia de distúrbio</b> <i>Flutuante</i> | Controla a extensão das direções do deslocamento aplicadas pelo parâmetro <b>Desordem</b>, em que um valor mais alto resulta em uma direção mais estreita e definida.    A direção é controlada pelo parâmetro <b>Ângulo de anisotropia de desordem</b>. |
| <b>ângulo de anisotropia de desordem</b> <i>Flutuante</i> | Controla a direção do deslocamento aplicado pelo parâmetro <b>Desordem</b> quando o parâmetro <b>anisotropia de Desordem</b> não é zero. |
| <b>Deslocamento do bloco</b> <i>Flutuante2</i> | Controla a posição da parte de plano infinito usada para renderizar o ruído. |
| <b>Expansão não quadrada</b> <i>Booleano</i> | Em imagens não quadradas, mantém o ladrilho gerado quadrado e expande a geração de ruído até os limites da imagem. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Manchas gaussianas 2 - Exemplo 1](gaussian-spots-2.resources/gaussian_spots_2_1.png "Manchas gaussianas 2 - Exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Manchas gaussianas 2 - Exemplo 2](gaussian-spots-2.resources/noise_gaussian_spots_2_v2_speed0.6_aniso0.gif "Manchas gaussianas 2 - Exemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Manchas gaussianas 2 - Exemplo 3](gaussian-spots-2.resources/noise_gaussian_spots_2_v2_speed0.6_aniso1.gif "Manchas gaussianas 2 - Exemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Manchas gaussianas 2 - Exemplo 4](gaussian-spots-2.resources/noise_gaussian_spots_2_v2_speed0.3_aniso0.6.gif "Manchas gaussianas 2 - Exemplo 4"){zoomable="yes"}

</td>
</tr>
</table>
