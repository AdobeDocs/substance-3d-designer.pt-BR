---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-2.html"
breadcrumb-title: ''
description: Use o nó Ruído em escala 2 para aumentar as texturas usando interpolação baseada em ruído para manter a qualidade da textura em tamanhos maiores.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Aumento de ruído 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 6%

---


# Aumento de ruído 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](noise-upscale-2.resources/noise-upscale.png){width="128px"}

<b>Entrada:</b> Filtros > Transformas

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Utiliza um procedimento de ruído de entrada e o dimensiona para resolução dupla, mantendo os detalhes, mas sem introduzir muitos ladrilhos. Usa um tipo “X” de máscara e mescla com menos contraste do que a entrada original (os modos de mesclagem internos são Máx e Mín).

Este nó é destinado principalmente para otimizar gráficos lentos que usam ruídos pesados e grandes. Ele permite que você use resoluções mais altas sem introduzir muito tempo extra de computação.

Consulte também [Aumento de Ruído 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md) e [Aumento de Ruído 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-3/noise-upscale-3.md) para ver as diferentes variações deste processo.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Deslocamento1X</b> <i>0.0 - 1.0</i> | Desliza as partes superior e inferior sobre o eixo X. |
| <b>Deslocamento1A</b> <i>0.0 - 1.0</i> | Desliza as partes superior e inferior sobre o eixo Y. |
| <b>Deslocamento2X</b> <i>0.0 - 1.0</i> | Desliza as partes esquerda e direita sobre o eixo X. |
| <b>Deslocamento2Y</b> <i>0.0 - 1.0</i> | Desliza as partes esquerda e direita sobre o eixo Y. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="noise-upscale-2.resources/noise2ex.png" />
        </td>
    </tr>
</table>
