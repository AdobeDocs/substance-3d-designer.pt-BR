---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/lighting-cancel-high-frequencies.html"
breadcrumb-title: ''
description: Use o nó Cancelamento de iluminação de altas frequências para remover detalhes de iluminação de alta frequência das texturas para análise de material.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Lighting Cancel High Frequencies
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Iluminação Cancelar frequências altas
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 7%

---


# Iluminação Cancelar frequências altas

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](lighting-cancel-high-frequencies.resources/lighting-cancel-high-frequencies.png){width="128px"}

<b>Entrada:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Semelhante ao [Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md), mas mais adequado para imagens coloridas completas (ele não diminui muito a saturação do resultado), este nó tenta cancelar pequenos detalhes de iluminação e alta frequência.

Consulte também [Cancelamento de iluminação em baixas frequências](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md) e o [Highpass de luminância](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/luminance-highpass/luminance-highpass.md) mais avançado e recomendado.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Intensidade</b> <i>0.0 - 1.0</i> | Intensidade do efeito de cancelamento de iluminação. |
| <b>Raio</b> <i>0.0 - 10.0</i> | Raio ou tamanho dos detalhes de iluminação para cancelar. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="lighting-cancel-high-frequencies.resources/lighting-cancel-highfrequencies-example.png" />
        </td>
    </tr>
</table>
