---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/messy-fibers-3.html"
breadcrumb-title: ''
description: Use o nó Messy Fibres 3 para gerar padrões de fibra complexos para criar efeitos de textura de tecido e têxtil.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Messy fibers 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fibras bagunçadas 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 1%

---


# Fibras bagunçadas 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Fibras bagunçadas 3 - Ícone](../../../../../../assets/messy_fibers_3.png "Fibras bagunçadas 3 - Ícone"){width="200px"}

<b>Entrada:</b> geradores de textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma variação dos <b>ruídos estruturados de fibras desordenadas</b>.

Veja também: [Fibras confusas 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-1/messy-fibers-1.md), [Fibras confusas 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-2/messy-fibers-2.md)

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
| <b>Ângulo</b> Flutuante | O ângulo usado para definir a direção dos encadeamentos, em número de voltas e começando da direita horizontal. |
| <b>Ângulo aleatório</b> flutuante | O valor máximo de variação aleatória aplicado ao valor <b>Ângulo</b>, em número de voltas. |
| <b>Luminância aleatória</b> flutuante | O intervalo de luminância subtraído aleatoriamente dos encadeamentos, em que 1 é o intervalo completo. |
| <b>Deslocamento do bloco</b> flutuante2 | Controla a posição da parte de plano infinito usada para renderizar o ruído. |
| <b>Expansão não quadrada</b> Booleana | Em imagens não quadradas, mantém o ladrilho gerado quadrado e expande a geração de ruído até os limites da imagem. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Fibras bagunçadas 3 - Exemplo 1](../../../../../../assets/messy_fibers_3_1.png "Fibras bagunçadas 3 - Exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Fibras bagunçadas 3 - Exemplo 2](../../../../../../assets/noise_messy_fibers_3_v2_speed0.1_aniso0.gif "Fibras bagunçadas 3 - Exemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Fibras bagunçadas 3 - Exemplo 3](../../../../../../assets/noise_messy_fibers_3_v2_speed0.1_aniso1.gif "Fibras bagunçadas 3 - Exemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Fibras bagunçadas 3 - Exemplo 4](../../../../../../assets/noise_messy_fibers_3_v2_speed0.1_aniso0.6.gif "Fibras bagunçadas 3 - Exemplo 4"){zoomable="yes"}

</td>
</tr>
</table>
