---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-sobel.html"
breadcrumb-title: ''
description: Use o nó Curvatura Sobel para detectar bordas de curvatura usando operadores Sobel para criar máscaras baseadas em bordas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Curvatura Sobel
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 1%

---


# Curvatura Sobel

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/curvature-sobel.png){width="128px"}

## Curvatura Sobel

**Entrada:** *Filtros/Efeitos*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Executa uma conversão de curvatura de passagem única simples e áspera para a entrada [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md). O mapa resultante tem tons brancos para áreas convexas e tons pretos para côncavas. A curvatura sempre produzirá linhas mais espessas e transições nítidas.

Esse nó é útil para realce ou escurecimento rápido de determinadas bordas. É um pouco diferente da [Curvatura](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md), pois produz resultados de melhor qualidade, mas ainda é nítida e áspera.

## Parâmetros

* **Intensidade**: *0.0 - 1.0* Intensidade do efeito, ajusta o contraste.
* **Tipo normal**: *DirectX, OpenGL*

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/curv-sobel-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
