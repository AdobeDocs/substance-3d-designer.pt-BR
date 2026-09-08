---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-1.html"
breadcrumb-title: ''
description: Use o nó Aumento de ruído 1 para aumentar texturas usando algoritmos baseados em ruído para preservar detalhes ao aumentar a resolução da textura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Aumento de ruído 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 6%

---


# Aumento de ruído 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/noise-upscale.png){width="128px"}

<b>Entrada:</b> Filtros > Transformas

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Utiliza um procedimento de ruído de entrada e o dimensiona para resolução dupla, mantendo os detalhes, mas sem introduzir muitos ladrilhos. Usa um tipo “X” de máscara e mescla com contraste semelhante à entrada original (o modo de mesclagem interno é Copiar).

Este nó é destinado principalmente para otimizar gráficos lentos que usam ruídos pesados e grandes. Ele permite que você use resoluções mais altas sem introduzir muito tempo extra de computação.

Consulte também [Atualização de Ruído 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md) e [Atualização de Ruído 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-3/noise-upscale-3.md) para obter variações diferentes desse processo.

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
            <img src="../../../../../../assets/noise1ex.png" />
        </td>
    </tr>
</table>
