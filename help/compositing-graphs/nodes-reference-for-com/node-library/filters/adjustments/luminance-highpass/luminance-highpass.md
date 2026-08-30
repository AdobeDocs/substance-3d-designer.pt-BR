---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/luminance-highpass.html"
breadcrumb-title: ''
description: Use o nó Highpass de luminância para extrair detalhes de luminância de alta frequência das texturas para aprimorar os detalhes da superfície.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Luminance Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Highpass de luminância
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 9%

---


# Highpass de luminância

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](luminance-highpass.resources/luminance-highpass.png){width="128px"}

<b>Entrada:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Cancela as informações de iluminação executando um [highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)no valor de Luminância da entrada. Útil para corrigir texturas fotografadas com informações de iluminação. Pode ser combinado no [Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html) com várias passagens para remover diferentes frequências de detalhes de iluminação.

Faz um trabalho um pouco melhor na preservação de cores do que [Cancelamento de iluminação em baixas frequências.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Raio</b> <i>0.0 - 64.0</i> | Raio do efeito highpass. Um raio menor cancela uma iluminação menor, ajuste para corresponder às imagens de entrada. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="luminance-highpass.resources/luminance-highpass-example.png" />
        </td>
    </tr>
</table>
