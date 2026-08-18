---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/clone-filter-node.html"
breadcrumb-title: ''
description: Use o nó do filtro Clone para duplicar e deslocar regiões de textura para criar padrões perfeitos e efeitos de divisão em blocos gráficos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Clone (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Clonar (Nó de Filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# Clonar (Nó de Filtro)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-4.png)

## Clonar

**Entrada:** *Filtros/Transformações*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Clona uma imagem de entrada uma vez para um local especificado. Pode funcionar como uma ferramenta bruta de “carimbo”.

Requer um pouco de cuidado para obter os resultados desejados:

* O ideal é que a imagem de entrada tenha um canal alfa (como um decalque), uma vez que a mesclagem é apenas uma cópia reta.
* O padrão da máscara é preto. Portanto, para ver os resultados, um valor uniforme de tons de cinza branco precisa ser conectado, pelo menos.
* O Deslocamento recortará fora da imagem facilmente, portanto, use valores pequenos.

## Parâmetros

### Entradas

* **Origem**: *Entrada de Cores*\
  Imagem para clonar. Importante: o ideal é que a imagem tenha um canal alfa!
* **Máscara**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó. O padrão é preto!

### Parâmetros

* **Deslocamento**: *-*\
  Move ou traduz o resultado. Positivo é para a esquerda e para cima, Negativo é para a direita e para baixo. Use valores pequenos. A versão 1.0 ou posterior move o texto para fora da imagem.
* **Máscara de desfoque**: *0.0 - 10.0\
  Aplique um filtro de desfoque à máscara para suavizar bordas.*

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/clone-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
