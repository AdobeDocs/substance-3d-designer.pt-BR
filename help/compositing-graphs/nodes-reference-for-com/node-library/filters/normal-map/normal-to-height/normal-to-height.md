---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height.html"
breadcrumb-title: ''
description: Use o nó Normal para Height para converter mapas normais em mapas de height para extrair informações de profundidade de superfície.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal to Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal para Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 1%

---


# Normal para Height

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-to-height.png){width="128px"}

## Normal para Height

**Entrada:** *Filtros/Mapa Normal*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Nó de conversão reversa que tenta converter um Normalmap de espaço tangente em um Heightmap. Esta é a versão ligeiramente mais simples; o [Normal para o Height HQ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height-hq/normal-to-height-hq.md) tem mais opções.

Útil quando você tem apenas uma origem Normalmap, mas ainda deseja executar operações que a combinam com um Heightmap. Lembre-se de que isso nunca poderá fornecer um resultado 100% correto, pois as informações são perdidas por natureza do processo quando o Height é convertido para Normal. Se você ajustar as configurações de acordo, esta versão não-HQ faz um trabalho decente de converter detalhes simples.

## Parâmetros

* **Equilíbrio de Relevos**: *0.0 - 1.0* Ajuste a extensão em que as diferentes frequências influenciam o resultado final. Isso é amplamente dependente do mapa de entrada e requer um pouco de ajustes.
* **Formato Normal**: *DirectX, OpenGL*\
  Alterna entre diferentes formatos de Mapas Normais (inverte o canal verde).
* **Opacidade global**: *0.0 - 1.0* Ajusta a opacidade global do efeito.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/normal2heightex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
