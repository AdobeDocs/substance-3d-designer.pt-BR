---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-3.html"
breadcrumb-title: ''
description: Use o nó do Células 3 para gerar padrões celulares intermediários a fim de criar efeitos de textura orgânica e biológica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: CÉLULAS 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---


# CÉLULAS 3

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Células 3 - Ícone](../../../../../../assets/cells_3.png "Células 3 - Ícone"){width="200px"}

<b>Entrada:</b> geradores de textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma variação das <b>Células</b> ruídos de paredes.

A interseção de discos produz células com paredes finas de suavidade desigual.

Veja também: [Células 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md), [Células 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md), [Células 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

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
| <b>Dureza</b> flutuante | A definição das paredes celulares, onde um valor mais alto resulta em paredes mais definidas e nítidas. |
| <b>Inverter</b> Booleano | Inverte os valores em tons de cinza da saída da imagem. |
| <b>Desordem</b> Flutuante | Desloca os ingredientes do ruído.    Isso pode ser usado para animar o ruído. |
| <b>Velocidade do distúrbio</b> flutuante | Ajusta a distância de deslocamento aplicada pelo parâmetro <b>Desordem</b>.    Isso pode ser usado para controlar a velocidade de deslocamento ao animar o ruído. |
| <b>anisotropia de desordem</b> flutuante | Controla a extensão das direções do deslocamento aplicadas pelo parâmetro <b>Desordem</b>, em que um valor mais alto resulta em uma direção mais estreita e definida.    A direção é controlada pelo parâmetro <b>Ângulo de anisotropia de desordem</b>. |
| <b>Ângulo de anisotropia do distúrbio</b> flutuante | Controla a direção do deslocamento aplicado pelo parâmetro <b>Desordem</b> quando o parâmetro &#39;anisotropia de Desordem&#39; não é zero. |
| <b>Tamanho do padrão</b> Float2 | Um multiplicador para o tamanho de um disco disperso em sua célula., onde 1,0 é o intervalo completo da célula. |
| <b>Escala de padrão</b> Flutuante | Um multiplicador para o <b>Tamanho do padrão</b>, onde 1,0 é o tamanho máximo. |
| <b>Ângulo</b> Flutuante | Ângulo usado para definir a direção dos discos, em número de voltas e começando na horizontal direita. |
| <b>Ângulo aleatório</b> flutuante | O valor máximo de variação aleatória aplicado ao valor <b>Ângulo</b>, em número de voltas. |
| <b>Deslocamento do bloco</b> flutuante2 | Controla a posição da parte de plano infinito usada para renderizar o ruído. |
| <b>Expansão não quadrada</b> Booleana | Em imagens não quadradas, mantém o ladrilho gerado quadrado e expande a geração de ruído até os limites da imagem. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Células 3 - Exemplo 1](../../../../../../assets/cells_3_1.png "Células 3 - Exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Células 3 - Exemplo 2](../../../../../../assets/noise_cells_3_v2_speed0.6_aniso0.gif "Células 3 - Exemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Células 3 - Exemplo 3](../../../../../../assets/noise_cells_3_v2_speed0.6_aniso1.gif "Células 3 - Exemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Células 3 - Exemplo 4](../../../../../../assets/noise_cells_3_v2_speed0.3_aniso0.6.gif "Células 3 - Exemplo 4"){zoomable="yes"}

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
