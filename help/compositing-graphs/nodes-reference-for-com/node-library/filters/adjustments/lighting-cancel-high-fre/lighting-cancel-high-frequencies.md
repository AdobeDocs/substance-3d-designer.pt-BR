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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 2%

---


# Iluminação Cancelar frequências altas

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/lighting-cancel-high-frequencies.png){width="128px"}

## Iluminação Cancelar frequências altas

**Entrada:** *Filtros/Ajustes*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Semelhante ao [Highpass](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md), mas mais adequado para imagens coloridas completas (ele não diminui muito a saturação do resultado), este nó tenta cancelar pequenos detalhes de iluminação e alta frequência.

Consulte também [Cancelamento de iluminação em baixas frequências](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md) e o [Highpass de luminância](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/luminance-highpass/luminance-highpass.md) mais avançado e recomendado.

## Parâmetros

* **Intensidade**: *0.0 -* 1.0\
  Intensidade do efeito de cancelamento de iluminação.
* **Raio**: *0.0 - 10.0* Raio ou tamanho dos detalhes de iluminação a ser cancelado.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/lighting-cancel-highfrequencies-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
