---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-noise-4.html"
breadcrumb-title: ''
description: Use o nó Ruído direcional 4 para gerar padrões de ruído direcional com quatro oitavas para criar texturas anisotrópicas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional noise 4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: RUÍDO DIRECIONAL 4
user-guide-description: ''
user-guide-title: ''
source-git-commit: 93824555c1b2d3de289eaf470e6f929ebf90dd71
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---


# RUÍDO DIRECIONAL 4

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ruído direcional 4 - Ícone](directional-noise-4.resources/directional_noise_4.png "Ruído direcional 4 - Ícone"){width="200px"}

<b>Entrada:</b> geradores de Textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma variação dos ruídos de <b>Ruído direcional</b>.

Veja também: [Ruído direcional 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-1/directional-noise-1.md), [Ruído direcional 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-2/directional-noise-2.md), [Ruído direcional 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-3/directional-noise-3.md)

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
| <b>Desordem</b> <i>Precisão decimal</i> | Desloca os ingredientes do ruído.    Isso pode ser usado para animar o ruído. |
| <b>Velocidade do distúrbio</b> <i>Precisão decimal</i> | Ajusta a distância de deslocamento aplicada pelo parâmetro <b>Desordem</b>.    Isso pode ser usado para controlar a velocidade de deslocamento ao animar o ruído. |
| <b>anisotropia de distúrbio</b> <i>Precisão decimal</i> | Controla a extensão das direções do deslocamento aplicadas pelo parâmetro <b>Desordem</b>, em que um valor mais alto resulta em uma direção mais estreita e definida.    A direção é controlada pelo parâmetro <b>ângulo de anisotropia de Desordem</b>. |
| <b>ângulo de anisotropia de desordem</b> <i>Precisão decimal</i> | Controla a direção do deslocamento aplicado pelo parâmetro <b>Desordem</b> quando o parâmetro &#39;anisotropia de Desordem&#39; não é zero. |
| <b>Ângulo</b> <i>Precisão decimal</i> | Ângulo usado para definir a direção do ruído, em número de voltas e começando na horizontal direita. |
| <b>Ângulo aleatório</b> <i>Precisão decimal</i> | O valor máximo de variação aleatória aplicado ao valor <b>Ângulo</b>, em número de voltas. |
| <b>Deslocamento do bloco</b> <i>Precisão decimal 2</i> | Controla a posição da parte de plano infinito usada para renderizar o ruído. |
| <b>Expansão não quadrada</b> <i>Booleano</i> | Em imagens não quadradas, mantém o ladrilho gerado quadrado e expande a geração de ruído até os limites da imagem. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ruído direcional 4 - Exemplo 1](directional-noise-4.resources/directional_noise_4_1.png "Ruído direcional 4 - Exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ruído direcional 4 - Exemplo 2](directional-noise-4.resources/noise_directional_noise_4_v2_speed0.6_aniso0.gif "Ruído direcional 4 - Exemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ruído direcional 4 - Exemplo 3](directional-noise-4.resources/noise_directional_noise_4_v2_speed0.6_aniso1.gif "Ruído direcional 4 - Exemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ruído direcional 4 - Exemplo 4](directional-noise-4.resources/noise_directional_noise_4_v2_speed0.3_aniso0.6.gif "Ruído direcional 4 - Exemplo 4"){zoomable="yes"}

</td>
</tr>
</table>
