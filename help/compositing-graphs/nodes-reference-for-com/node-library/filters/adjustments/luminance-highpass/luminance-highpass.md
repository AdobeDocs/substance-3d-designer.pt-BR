---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/luminance-highpass.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 6%

---


# Highpass de luminância

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/luminance-highpass.png){width="128px"}

## Highpass de luminância

**Entrada:** *Filtros/Ajustes*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Cancela as informações de iluminação executando um [highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)no valor de Luminância da entrada. Útil para corrigir texturas fotografadas com informações de iluminação. Pode ser combinado no [Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html) com várias passagens para remover diferentes frequências de detalhes de iluminação.

Faz um trabalho um pouco melhor na preservação de cores do que [Cancelamento de iluminação em baixas frequências.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md)

## Parâmetros

* **Raio**: *0.0 - 64.0* Raio do efeito highpass. Um raio menor cancela uma iluminação menor, ajuste para corresponder às imagens de entrada.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/luminance-highpass-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
