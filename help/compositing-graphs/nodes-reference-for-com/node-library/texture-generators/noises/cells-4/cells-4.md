---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-4.html"
breadcrumb-title: ''
description: Use o nó do Células 4 para gerar padrões celulares avançados para criar efeitos de textura orgânicos e biológicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: CÉLULAS 4
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 3%

---


# CÉLULAS 4

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Células 4 - Ícone](../../../../../../assets/cells_4.png "Células 4 - Ícone"){width="200px"}

<b>Entrada:</b> geradores de textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma variação das <b>Células</b> ruídos de paredes.

A cada célula é atribuída uma cor sem graça, que pode ser aleatória ou de amostra de uma imagem de entrada.

Veja também: [Células 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md), [Células 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md), [Células 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Entradas

</td>
<td style="border: 0;" valign="top">

### Saídas

</td>
<td style="border: 0;" valign="top">

### Parâmetros

</td>
<td style="border: 0;" valign="top">

### Exemplos

</td>
</tr>
</table>

## Entradas

|  |  |
| --- | --- |
| <b>Entrada</b> *Tons de cinza* |  |

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
| <b>Origem da cor</b> Inteiro | A origem da cor simples aplicada às células:<ul data-preserve-html="true"> <li data-preserve-html="true"><b><i>Aleatório:</i></b> use uma cor aleatória controlada pela semente aleatória do nó</li> <li data-preserve-html="true"><b><i>Pseudorandom:</i></b> usar uma cor aleatória propagada por um valor separado definido pelo usuário</li> <li data-preserve-html="true"><b><i>Entrada de imagem:</i></b> use a cor amostrada no local da célula na imagem de entrada</li> </ul> |
| <b>Semente Pseudorandom</b> Inteiro *Disponível quando &#39;Origem da cor&#39; está definido como &#39;Pseudorandom&#39;* | Permite alterar a semente da cor separadamente da semente do nó. |
| <b>Expansão não quadrada</b> Booleana | Em imagens não quadradas, mantém o ladrilho gerado quadrado e expande a geração de ruído até os limites da imagem. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Células 4 - Exemplo 1](../../../../../../assets/cells_4_1.png "Células 4 - Exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Células 4 - Exemplo 2](../../../../../../assets/noise_cells_4_v2_speed0.3_aniso0.6.gif "Células 4 - Exemplo 2"){zoomable="yes"}

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
