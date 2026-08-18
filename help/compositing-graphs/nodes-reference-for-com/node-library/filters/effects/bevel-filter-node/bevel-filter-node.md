---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-filter-node.html"
breadcrumb-title: ''
description: Use o nó do filtro de Chanfro para criar bordas chanfradas em formas e padrões para adicionar profundidade e dimensão.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Chanfro (Nó de filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 2%

---


# Chanfro (Nó de filtro)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/bevel.png){width="128px"}

## Chanfro

**Entrada:** *Filtros/Efeitos*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Executa um efeito de chanfro de borda em um Heightmap em tons de cinza de entrada. Retorna Heightmap e Normalmap chanfrados com base nesse Heightmap.

Esse é um nó útil para aplicar perfis de curva exatos em um mapa de altura básico idealmente binário (preto/branco de contrato alto).

## Parâmetros

### Entradas

* **entrada**: *entrada em tons de cinza*\
  Mapa de altura a converter.
* **Curva Personalizada**: *Entrada Em Tons De Cinza*\
  Gradiente que determina a curva/inclinação exata. O ideal é um nó Gradiente linear, no qual você pode executar qualquer tipo de ajuste, como [Níveis](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) ou [Curvas](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md). Ativo somente quando “Usar curva personalizada” é Verdadeiro.

### Parâmetros

* **Distância**: *-1.0 - 1.0* A que distância o efeito de chanfro deve chegar.
* **Tipo de canto**: *Redondo, Angular* Se o perfil de chanfro deve ser arredondado ou reto.
* **Suavização**: *0.0 - 5.0* Quanta suavização adicional (desfoque) executar após o bisel.
* **Usar Desfoque Não Uniforme**: *Falso/Verdadeiro* Se a suavização deve ser feita de maneira não uniforme.
* **Usar curva personalizada**: *Falso/Verdadeiro* Alterna o uso de sua própria curva de height personalizada. Veja acima para obter mais informações.
* **Intensidade normal**: *0.0 - 50.0* Intensidade do Normalmap gerado.
* **Formato Normal**: *DirectX, OpenGL*\
  Alterne entre diferentes formatos de Mapas Normais (inverte o canal Verde).

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/bevel-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
