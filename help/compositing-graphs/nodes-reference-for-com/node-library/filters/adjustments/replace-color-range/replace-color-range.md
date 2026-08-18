---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/replace-color-range.html"
breadcrumb-title: ''
description: Use o nó Substituir intervalo de cores para substituir cores dentro de um intervalo especificado por novas cores para a correção de cores.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Replace Color Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substituir gama de cores
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---


# Substituir gama de cores

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/replace-color-range.png){width="128px"}

## Substituir gama de cores

**Entrada:** *Filtros/Ajustes*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Substitui a cor de origem pela cor de destino, com controles adicionais. Pode, por exemplo, ser usado para recolorir partes de um mapa de ID de material (bolo).

Para uma versão mais avançada, consulte [Correspondência de cores.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-match/color-match.md)

## Parâmetros

* **Cor de origem**: *(valor da cor)*Cor para substituir.
* **Cor de destino**: *(valor da cor)*Cor pela qual substituir.
* **Intervalo de Origem**: *0.0 -* 1.0\
  Faixa ou tolerância da Origem separada. Pode ser aumentado para que outras cores vizinhas também tenham o matiz alterado.
* **Limite**: *0.0 - 1.0* Queda/contraste para o intervalo. Defina como baixo para substituir apenas a cor de origem, definido como um valor maior para substituir as cores misturadas na origem.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/replace-color-range-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
