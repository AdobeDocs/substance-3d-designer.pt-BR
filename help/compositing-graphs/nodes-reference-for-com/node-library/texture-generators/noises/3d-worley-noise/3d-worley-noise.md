---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-worley-noise.html"
breadcrumb-title: ''
description: Use o nó Ruído Worley 3D para gerar ruído Worley com base na posição 3D para criar efeitos de textura volumétrica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Worley Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruído Worley 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1f6cd80beb50560ef8711ff67335b0bb54df04ca
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 7%

---


# Ruído Worley 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/3d-worley.png){width="128px"}

<b>Entrada:</b> Geradores de Textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Um dos ruídos mais versáteis e avançados da biblioteca, ele gera um ruído Worley no espaço 3D, com base em um mapa de posição de entrada. Tem várias opções que o tornam muito mais poderoso do que os ruídos padrão baseados em [Células](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md)ou [Distância](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/distance/distance.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Escala</b> <i>1 - 64</i> | Defina a escala global para o efeito. |
| <b>Tamanho</b> <i>0.0 - 1.0</i> | Executar escala não uniforme nos eixos X, Y e Z separadamente. |
| <b>Modo</b> <i>Euclidiano, Manhattan, Chebyshev, Minkowski</i> | Altere a métrica de distância. Permite alguns tipos de ruído muito diferentes. |
| <b>Número de Minkowski</b> <i>0.0 - 20.0</i> | Somente com a métrica de distância de Minkowski. Mistura diferentes tipos de métricas. |
| <b>Estilo</b> <i>F1, F2, F2-F1, Borda, Cor Aleatória</i> | Defina a combinação de Métrica. Permite muitas outras combinações. |
| <b>Largura da borda</b> <i>0.0 - 1.0</i> | Quando a matemática de combinação de bordas estiver ativa, controla a largura da borda. |
| <b>Arredondamento</b> <i>0.0 - 1.0</i> | Disponível apenas nos modos F1, F2 e F2-F1. Define a posição intermediária do nível. |
| <b>Inverter</b> <i>Falso/Verdadeiro</i> | Inverte o resultado. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3d-worley-ex04.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3d-worley-ex03.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3d-worley-ex02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3d-worley-ex01.png" />
        </td>
    </tr>
</table>
