---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-4.html"
breadcrumb-title: ''
description: Use o nó da Soma fractal 4 para gerar ruído fractal com quatro oitavas para criar texturas orgânicas detalhadas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum 4
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SOMA FRACTAL 4
user-guide-description: ''
user-guide-title: ''
source-git-commit: a2d6381b9bf224008fa412ef70c9b63b9b2756e8
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---


# SOMA FRACTAL 4

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Soma fractal 4 - Ícone](fractal-sum-4.resources/fractal_sum_4.png "Soma fractal 4 - Ícone"){width="200px"}

<b>Entrada:</b> geradores de Textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma variação dos ruídos de <b>Soma fractal</b>.

Veja também: [Soma fractal base](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-base/fractal-sum-base.md), [Soma fractal 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-1/fractal-sum-1.md), [Soma fractal 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-2/fractal-sum-2.md), [Soma fractal 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-3/fractal-sum-3.md)

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
| <b>Desordem</b> <i>Precisão decimal</i> | Desloca os ingredientes do ruído.    Isso pode ser usado para animar o ruído. |
| <b>Velocidade do distúrbio</b> <i>Precisão decimal</i> | Ajusta a distância de deslocamento aplicada pelo parâmetro <b>Desordem</b>.    Isso pode ser usado para controlar a velocidade de deslocamento ao animar o ruído. |
| <b>Expansão não quadrada</b> <i>Booleano</i> | Em imagens não quadradas, mantém o ladrilho gerado quadrado e expande a geração de ruído até os limites da imagem. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Soma fractal 4 - Exemplo 1](fractal-sum-4.resources/fractal_sum_4_1.png "Soma fractal 4 - Exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Soma fractal 4 - Exemplo 2](fractal-sum-4.resources/noise_fractal_sum_4_v2_speed0.6_aniso0.gif "Soma fractal 4 - Exemplo 2"){zoomable="yes"}

</td>
</tr>
</table>
