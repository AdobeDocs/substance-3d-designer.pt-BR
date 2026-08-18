---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-photo.html"
breadcrumb-title: ''
description: Use o nó Criar foto em bloco para converter fotografias em texturas de revestimento perfeitas para a criação de material.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Photo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tornar foto lado a lado
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---


# Tornar foto lado a lado

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/make-it-tile-photo.png)

![](../../../../../../assets/make-it-tile-photo-grayscale.png)

## Torná-lo uma foto lado a lado (tons de cinza)

**Entrada:** *Filtros/Divisão em blocos*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Este nó fornece a funcionalidade de correção de borda para qualquer imagem que possa não ser ladrilhada devido a bordas não contínuas. Ela não afeta nada além das bordas da imagem de entrada. Se quiser ajustar o dimensionamento ou o ladrilho de diferentes maneiras, observe [Criar um patch de ladrilho](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-patch/make-it-tile-patch.md).

## Parâmetros

* **Distorção de máscara H**: *-100.0 - 100.0* Introduz a distorção no eixo horizontal para evitar transições indefinidas.
* **Distorção de Máscara V**: *-100.0 - 100.0* Introduz a distorção no eixo vertical para evitar transições indefinidas.
* **Tamanho da máscara H**: *0.0 - 1.0* Define até onde a borda de transição alcança horizontalmente.
* **Tamanho da Máscara V**: *0.0 - 1.0* Define até onde a borda de transição alcança verticalmente.
* **Precisão da Máscara H**: *0.0 - 1.0* Define a suavidade da transição na horizontal.
* **Precisão da Máscara V**: *0.0 - 1.0* Define a suavidade da transição na vertical.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/mit-photo-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
