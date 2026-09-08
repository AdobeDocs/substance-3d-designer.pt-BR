---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-noise-2.html"
breadcrumb-title: ''
description: Use o nó Ruído direcional 2 para gerar padrões de ruído direcional com duas oitavas para criar efeitos anisotrópicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional noise 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: RUÍDO DIRECIONAL 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 1%

---


# RUÍDO DIRECIONAL 2

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ruído direcional 2 - Ícone](../../../../../../assets/directional_noise_2.png "Ruído direcional 2 - Ícone"){width="200px"}

<b>Entrada:</b> geradores de textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma variação dos ruídos de <b>Ruído direcional</b>.

Veja também: [Ruído direcional 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-1/directional-noise-1.md), [Ruído direcional 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-3/directional-noise-3.md), [Ruído direcional 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/directional-noise-4/directional-noise-4.md)

</td>
</tr>
</table>

## Saídas

|  |  |
| --- | --- |
| <b>Saída</b> *Tons de cinza* | O ruído gerado como bitmap em tons de cinza. |

## Parâmetros

|  |  |
| --- | --- |
| <b>Escala</b> Inteiro | A subdivisão da grade usada para gerar os blocos de ruído.    Um valor mais alto resulta no desenho de mais ladrilhos e em um ruído mais denso. |
| <b>Desordem</b> Flutuante | Desloca os ingredientes do ruído.    Isso pode ser usado para animar o ruído. |
| <b>Velocidade do distúrbio</b> flutuante | Ajusta a distância de deslocamento aplicada pelo parâmetro <b>Desordem</b>.    Isso pode ser usado para controlar a velocidade de deslocamento ao animar o ruído. |
| <b>anisotropia de desordem</b> flutuante | Controla a extensão das direções do deslocamento aplicadas pelo parâmetro <b>Desordem</b>, em que um valor mais alto resulta em uma direção mais estreita e definida.    A direção é controlada pelo parâmetro <b>Ângulo de anisotropia de desordem</b>. |
| <b>Ângulo de anisotropia do distúrbio</b> flutuante | Controla a direção do deslocamento aplicado pelo parâmetro <b>Desordem</b> quando o parâmetro &#39;anisotropia de Desordem&#39; não é zero. |
| <b>Ângulo</b> Flutuante | Ângulo usado para definir a direção do ruído, em número de voltas e começando na horizontal direita. |
| <b>Ângulo aleatório</b> flutuante | O valor máximo de variação aleatória aplicado ao valor <b>Ângulo</b>, em número de voltas. |
| <b>Deslocamento do bloco</b> flutuante2 | Controla a posição da parte de plano infinito usada para renderizar o ruído. |
| <b>Expansão não quadrada</b> Booleana | Em imagens não quadradas, mantém o ladrilho gerado quadrado e expande a geração de ruído até os limites da imagem. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ruído direcional 2 - Exemplo 1](../../../../../../assets/directional_noise_2_1.png "Ruído direcional 2 - Exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ruído direcional 2 - Exemplo 2](../../../../../../assets/noise_directional_noise_2_v2_speed0.6_aniso0.gif "Ruído direcional 2 - Exemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ruído direcional 2 - Exemplo 3](../../../../../../assets/noise_directional_noise_2_v2_speed0.6_aniso1.gif "Ruído direcional 2 - Exemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ruído direcional 2 - Exemplo 4](../../../../../../assets/noise_directional_noise_2_v2_speed0.3_aniso0.6.gif "Ruído direcional 2 - Exemplo 4"){zoomable="yes"}

</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
