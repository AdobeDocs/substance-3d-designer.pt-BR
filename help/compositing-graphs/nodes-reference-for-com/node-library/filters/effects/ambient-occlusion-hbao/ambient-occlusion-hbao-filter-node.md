---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-hbao-filter-node.html"
breadcrumb-title: ''
description: Use o nó do filtro HBAO de Oclusão ambiente para gerar mapas de oclusão ambiente usando algoritmos baseados em horizonte para sombreamento realista.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (HBAO) (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Oclusão ambiente (HBAO) (nó de filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%

---


# Oclusão ambiente (HBAO) (nó de filtro)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hbao.png){width="128px"}

## Oclusão ambiente (HBAO)

**Entrada:** *Filtros/Efeitos*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Utiliza um Heightmap como entrada e gera um mapa de Oclusão Ambiente a partir dele. Ele usa a Oclusão ambiente baseada em Horizon, um algoritmo originalmente destinado para a geração AO em tempo real de espaço de tela. Muito útil para criar mapas de AO de procedimento a partir de Heightmaps de procedimento.

Para uma versão alternativa mais avançada, mas mais lenta, do AO, consulte [Oclusão ambiente (RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)

## Parâmetros

* **Usar Unidades Mundiais**: *Falso/Verdadeiro* Alterna o uso de unidades mundiais ou de espaço de tela. Habilita parâmetros extras que permitem um controle mais preciso.
* **Profundidade de Height**: *0.0 - 1.0* Usado somente quando Unidades Mundiais está definido como Falso. Controla o dimensionamento global.
* **Tamanho da Superfície**: **0.0 - 1000.0** Usado somente quando Unidades Mundiais está definido como Verdadeiro. Controla o dimensionamento global.
* **Escala do Height (cm)**: *0.0 - 1000.0* Usada somente quando Unidades Mundiais está definida como Verdadeiro. Controla o dimensionamento global.
* **Raio**: *0.0 - 1.0* Controla a propagação do AO.
* **Qualidade**: *4 amostras, 8 amostras, 16 amostras*\
  Define o nível de Qualidade determinando a quantidade de amostras usada para cálculo.
* **Otimização de GPU**: *Falso/Verdadeiro* Habilita a otimização interna de GPU, acelera o processamento.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/image2021-6-18-11-11-11-1.png" width="300px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/image2021-6-18-11-11-22.png" width="300px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
