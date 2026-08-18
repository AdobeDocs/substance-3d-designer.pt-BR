---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-bbox-size.html"
breadcrumb-title: ''
description: Use o nó Flood Fill para tamanho de caixa para preencher regiões com valores de tamanho de caixa delimitadora para efeitos de escala de procedimento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to BBox Size
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tamanho do Flood Fill para a caixa
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# Tamanho do Flood Fill para a caixa

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-bbox-size.png){width="128px"}

## Tamanho do Flood Fill para a caixa

**Entrada:** *Filtros/Efeitos*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera um mapa em tons de cinza a partir de uma base [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md), com valores vinculados ao tamanho individual de cada ladrilho.

Os valores são relativos ao tamanho total da tela de desenho (um ladrilho branco completo significaria que ela estica toda a tela de desenho), portanto, o contraste geralmente é baixo.

## Parâmetros

* **Saída**: *max(X, Y), X, Y* Define em qual métrica o valor se baseia: largura, comprimento ou ambos.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/floodbbox-ex1.png" width="256px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
