---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-range.html"
breadcrumb-title: ''
description: Use o nó Intervalo do histograma para remapear valores de textura com base em intervalos de histograma para correção e ajustes de cores.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Intervalo do histograma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 5%

---


# Intervalo do histograma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-range.resources/histogram-range-01.png){width="128px"}

<b>Entrada:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Reduza e/ou mova o intervalo de uma entrada em tons de cinza. Pode ser usado para remapear transições, semelhantes à [Luminosidade de contraste](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/contrast-luminosity/contrast-luminosity.md), mas com diferentes controles que podem fazer mais sentido em algumas situações.\
Consulte também [Verificação de histograma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) para obter outra maneira mais útil de remapear o intervalo.

[Clique aqui para assistir a um vídeo do Substance Academy sobre a gama de histogramas.](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=517s)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Intervalo</b> <i>0.0 - 1.0</i> | Quanto reduzir o intervalo de. Isso é semelhante a mover os controles deslizantes Níveis mínimo e Máximo para dentro. |
| <b>Posição</b> <i>0.0 - 1.0</i> | Deslocamento para a redução de intervalo, definindo um ponto médio diferente para a redução de intervalo. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="histogram-range.resources/histogram-range-02.gif" />
        </td>
    </tr>
</table>
