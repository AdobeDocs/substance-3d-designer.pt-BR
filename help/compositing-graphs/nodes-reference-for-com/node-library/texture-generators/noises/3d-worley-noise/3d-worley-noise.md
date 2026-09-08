---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-worley-noise.html"
breadcrumb-title: ''
description: Use o nó Ruído Worley 3D para gerar ruído Worley com base na posição 3D para criar efeitos de textura volumétrica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Worley Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruído Worley 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---


# Ruído Worley 3D

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-worley.png){width="128px"}

## Ruído Worley 3D

**Entrada:** *Geradores De Textura**/Ruídos*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Um dos ruídos mais versáteis e avançados da biblioteca, ele gera um ruído Worley no espaço 3D, com base em um mapa de posição de entrada. Tem várias opções que o tornam muito mais poderoso do que os ruídos padrão baseados em [Células](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md)ou [Distância](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/distance/distance.md).

## Parâmetros

* **Escala**: *1 - 64*\
  Defina a escala global para o efeito.
* **Tamanho**: *0.0 - 1.0* Execute um dimensionamento não uniforme nos eixos X, Y e Z separadamente.
* **Modo**: *Euclidiano, Manhattan, Chebyshev, Minkowski\
  Altere a métrica de distância. Permite alguns tipos de ruído muito diferentes.*
* **Número de Minkowski**: *0.0 - 20.0* Somente com a métrica de distância de Minkowski. Mistura diferentes tipos de métricas.
* **Estilo**: *F1, F2, F2-F1, Borda, Cor Aleatória* Defina a combinação de métrica para matemática. Permite muitas outras combinações.
* **Largura da Borda**: *0.0 - 1.0* Quando a matemática de combinação de Borda está ativa, controla a largura da borda.
* **Redondo**: *0.0 - 1.0* Disponível apenas nos modos F1, F2 e F2-F1. Define a posição intermediária do nível.
* **Inverter**: *Falso/Verdadeiro*\
  Inverte o resultado.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/3d-worley-ex04.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/3d-worley-ex03.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="../../../../../../assets/3d-worley-ex02.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c3_image" src="../../../../../../assets/3d-worley-ex01.png" width="256px"/></div> |
| --- | --- | --- | --- |
|  |  |  |  |

</td>
</tr>
</table>
