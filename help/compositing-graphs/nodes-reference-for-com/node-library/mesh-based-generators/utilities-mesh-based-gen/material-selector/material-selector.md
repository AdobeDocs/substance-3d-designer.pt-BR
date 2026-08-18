---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-selector.html"
breadcrumb-title: ''
description: Use o nó Seletor de material para selecionar materiais com base em dados de malha para criar efeitos de textura multimaterial.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Selector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Seletor de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 1%

---


# Seletor de material

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-selector.png){width="128px"}

## Seletor de material

**Entrada:** *Geradores Baseados Em Malha**/Utilitários*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Converte um mapa de ID de cor completa em uma máscara binária, preta e branca. Permite a mesclagem e a combinação de diferentes cores em uma máscara.

Isso é útil se você não quiser usar a [Mesclagem de vários materiais](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md) e preferir usar a máscara manualmente ou, como alternativa, se quiser usar manualmente as mesmas máscaras em outros locais.

## Parâmetros

* **Materiais**: 1 - 16\
  Define o número de materiais para os quais a combinação está habilitada.
* **Habilitar material #1-16**: falso/verdadeiro\
  Alterna a mesclagem e a combinação de cores na máscara de saída final. Pode ser ativada para quantas cores você deseja combinar.
* **Material #1-16**: (valor da cor)\
  Seletor de cores para a cor dos materiais que serão convertidos em preto e branco.
* **Parâmetros do Seletor de Cores**\
  Modifica a mesclagem e a conversão da cor em preto e branco.
  * **Grau de seleção**: 0.01 - 1.0\
    O quanto misturar com cores vizinhas.
  * **Preenchimento**: 0.0 - 1.0\
    Nitidez da transição, como Contraste.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/matselector-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
