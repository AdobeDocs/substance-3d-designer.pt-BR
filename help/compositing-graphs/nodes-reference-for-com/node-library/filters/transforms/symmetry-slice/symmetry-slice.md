---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry-slice.html"
breadcrumb-title: ''
description: Use o nó Fatia de simetria para cortar texturas ao longo de eixos de simetria para criar efeitos e padrões espelhados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry Slice
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fatia de simetria
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---


# Fatia de simetria

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/mirror-2.png){width="128px"}

## Fatia de simetria

**Entrada:** *Filtros/Transformações*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Nó de operação de simetria/espelhamento complexo. Permite uma grande variedade de operações geométricas com controle total, mas requer alguns experimentos.

Comparado ao [Espelho](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md) e à [Simetria](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/symmetry/symmetry.md), este nó tem muito mais opções.

## Parâmetros

* **Modo de simetria**: *0 - 6* Escolha a linha de geometria/espelho de simetria. As opções são Horizontal, Vertical, Diagonal esquerda-direita, Diagonal direita-esquerda, Vertical Invert, Corner e Diagonal Corner.
* **Modo de Transferência**: *0 - 6\
  Modo de mesclagem. As opções são:*
* **Mesclar**: *0.0 - 1.0* Mescla a imagem original de volta ao resultado.
* **Inverter Lado**: *Falso/Verdadeiro* Inverte a origem, significando que o lado de origem da operação é invertido. A simetria da esquerda para a direita, por exemplo, torna-se da direita para a esquerda.
* **Inverter Lado2**: *Falso/Verdadeiro* Usado somente quando o Modo de Simetria é 5 ou 6. Inverter origem do canto.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/symslice.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
