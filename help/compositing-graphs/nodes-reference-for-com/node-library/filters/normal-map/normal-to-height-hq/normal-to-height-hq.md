---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height-hq.html"
breadcrumb-title: ''
description: Use o nó QG Normal para Height para converter mapas normais em mapas de height de alta qualidade para extração de detalhes da superfície.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal To Height HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal para Height HQ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---


# Normal para Height HQ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-to-height-hq.png){width="128px"}

## Normal para Height HQ

**Entrada:** *Filtros/Mapa Normal*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Nó de conversão reversa que tenta converter um Normalmap de espaço tangente em um Heightmap. Este é o nó mais avançado; [Normal a Height](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height/normal-to-height.md) tem menos opções e usa cálculos diferentes.

Útil quando você tem apenas uma origem Normalmap, mas ainda deseja executar operações que a combinam com um Heightmap. Lembre-se de que isso nunca poderá fornecer um resultado 100% correto, pois as informações são perdidas por natureza do processo quando o Height é convertido para Normal. Ele nunca pode substituir um Heightmap gerado corretamente!

## Parâmetros

* **Formato Normal**: *DirectX, OpenGL*\
  Alterna entre diferentes formatos de Mapas Normais (inverte o canal verde).
* **Equilíbrio de Relevos**: *0.0 - 1.0* Mescla entre o viés de frequência baixa e alta.
* **Intensidade de Height**: *0.0 - 1.0* Intensidade ou multiplicador para o Heightmap, funciona um pouco como a opacidade global.
* **Normalizar Height**: *Falso/Verdadeiro* Dimensiona automaticamente o intervalo do Heightmap para usar contraste total, como [níveis automáticos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md).
* **Qualidade**: *Normal, Alta* Alterna entre velocidade ou qualidade.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/normal2height-hq-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
