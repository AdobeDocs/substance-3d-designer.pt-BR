---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-1.html"
breadcrumb-title: ''
description: Use o nó do Células 1 para gerar padrões celulares básicos para criar efeitos de textura orgânicos e biológicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: CÉLULAS 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1f6cd80beb50560ef8711ff67335b0bb54df04ca
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---


# CÉLULAS 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Células 1 - Ícone](../../../../../../assets/cells_1.png "Células 1 - Ícone"){width="200px"}

<b>Entrada:</b> geradores de textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma variação das <b>Células</b> ruídos de paredes.

Os padrões selecionados pelo usuário são dispersos e sobrepostos usando um modo de mesclagem Máx.

Veja também: [Células 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md), [Células 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md), [Células 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

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
| <b>ângulo de anisotropia de desordem</b> <i>Flutuante</i> | Controla a direção do deslocamento aplicado pelo parâmetro <b>Desordem</b> quando o parâmetro &#39;anisotropia de Desordem&#39; não é zero. |
| <b>Padrão</b> <i>Inteiro</i> | A forma de base espalhada na imagem gerada. |
| <b>Tamanho do padrão</b> <i>Flutuante2</i> | Um multiplicador para o tamanho de um padrão disperso em sua célula., onde 1,0 é o intervalo completo da célula. |
| <b>Escala de padrão</b> <i>Flutuante</i> | Um multiplicador para o <b>Tamanho do padrão</b>, onde 1,0 é o tamanho máximo. |
| <b>Luminância aleatória</b> <i>Flutuante</i> | O intervalo de luminância subtraído aleatoriamente das células, onde 1 é o intervalo completo. |
| <b>Ângulo</b> <i>Flutuante</i> | O ângulo usado para definir a direção das células, em número de voltas e começando da direita horizontal. |
| <b>Ângulo aleatório</b> <i>Flutuante</i> | O valor máximo de variação aleatória aplicado ao valor <b>Ângulo</b>, em número de voltas. |
| <b>Deslocamento do bloco</b> <i>Flutuante2</i> | Controla a posição da parte de plano infinito usada para renderizar o ruído. |
| <b>Expansão não quadrada</b> <i>Booleano</i> | Em imagens não quadradas, mantém o ladrilho gerado quadrado e expande a geração de ruído até os limites da imagem. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Células 1 - Exemplo 1](../../../../../../assets/cells_1_1.png "Células 1 - Exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Células 1 - Exemplo 2](../../../../../../assets/noise_cells_1_v2_speed0.3_aniso0.3.gif "Células 1 - Exemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Células 1 - Exemplo 3](../../../../../../assets/noise_cells_1_v2_speed0.5_aniso0.6.gif "Células 1 - Exemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Células 1 - Exemplo 4](../../../../../../assets/noise_cells_1_v2_speed0.3_aniso0.6.gif "Células 1 - Exemplo 4"){zoomable="yes"}

</td>
</tr>
</table>
