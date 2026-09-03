---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-2.html"
breadcrumb-title: ''
description: Use o nó do Células 2 para gerar padrões celulares intermediários a fim de criar efeitos de textura orgânica e biológica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: CÉLULAS 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---


# CÉLULAS 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Células 2 - Ícone](cells-2.resources/cells-2-01.png "Células 2 - Ícone"){width="200px"}

<b>Entrada:</b> geradores de textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma variação das <b>Células</b> ruídos de paredes.

Uma máscara binária das células com um thickness de parede ajustável.

Veja também: [Células 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md), [Células 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-3/cells-3.md), [Células 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

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
| <b>Largura da borda</b> <i>Flutuante</i> | Ajusta o thickness das paredes entre as células, como uma proporção da grade. (Ou seja, não depende da resolução) |
| <b>Inverter</b> <i>Booleano</i> | Alterna pretos e brancos na imagem de saída. |
| <b>Desordem</b> <i>Flutuante</i> | Desloca os ingredientes do ruído.    Isso pode ser usado para animar o ruído. |
| <b>Velocidade do distúrbio</b> <i>Flutuante</i> | Ajusta a distância de deslocamento aplicada pelo parâmetro <b>Desordem</b>.    Isso pode ser usado para controlar a velocidade de deslocamento ao animar o ruído. |
| <b>Expansão não quadrada</b> <i>Booleano</i> | Em imagens não quadradas, mantém o ladrilho gerado quadrado e expande a geração de ruído até os limites da imagem. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Células 2 - Exemplo 1](cells-2.resources/cells-2-02.png "Células 2 - Exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Células 2 - Exemplo 2](cells-2.resources/cells-2-03.gif "Células 2 - Exemplo 2"){zoomable="yes"}

</td>
</tr>
</table>
