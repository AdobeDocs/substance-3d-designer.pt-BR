---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-filter-node.html"
breadcrumb-title: ''
description: Use o nó do filtro Curvatura para gerar mapas de curvatura de mapas de height para detectar superfícies convexas e côncavas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Curvatura (Nó de filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---


# Curvatura (Nó de filtro)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/curvature-1.png){width="128px"}

## Curvatura

**Entrada:** *Filtros/Efeitos*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Executa uma conversão de curvatura de passagem única simples e áspera para a entrada [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md). O mapa resultante tem tons brancos para áreas convexas e tons pretos para côncavas. A curvatura sempre produzirá linhas finas em pixels e transições nítidas.

Esse nó é útil para um rápido realce ou escurecimento de determinadas bordas. É limitado em comparação à [Curvatura suave](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) (que produz resultados de maior qualidade) e à [Curvatura sólida](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md) (que tem mais opções).

## Parâmetros

* **Intensidade**: *0.0 - 10.0* Intensidade do efeito. Aumenta o contraste do resultado.
* **Formato Normal**: *DirectX, OpenGL*\
  Alterna entre diferentes formatos de Mapas Normais (inverte o canal Verde).

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/curvature-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
