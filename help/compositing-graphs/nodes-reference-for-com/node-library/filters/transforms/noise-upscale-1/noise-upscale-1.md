---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-1.html"
breadcrumb-title: ''
description: Use o nó Aumento de ruído 1 para aumentar texturas usando algoritmos baseados em ruído para preservar detalhes ao aumentar a resolução da textura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Aumento de ruído 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---


# Aumento de ruído 1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/noise-upscale.png){width="128px"}

## Aumento de ruído 1

**Entrada:** *Filtros/Transformações*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Utiliza um procedimento de ruído de entrada e o dimensiona para resolução dupla, mantendo os detalhes, mas sem introduzir muitos ladrilhos. Usa um tipo “X” de máscara e mescla com contraste semelhante à entrada original (o modo de mesclagem interno é Copiar).

Este nó é destinado principalmente para otimizar gráficos lentos que usam ruídos pesados e grandes. Ele permite que você use resoluções mais altas sem introduzir muito tempo extra de computação.

Consulte também [Atualização de Ruído 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md) e [Atualização de Ruído 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-3/noise-upscale-3.md) para obter variações diferentes desse processo.

## Parâmetros

* **Deslocamento1X**: *0.0 - 1.0* Desliza as partes superior e inferior sobre o eixo X.
* **Deslocamento1A**: *0.0 - 1.0*\
  Desliza as partes superior e inferior sobre o eixo Y.
* **Offset2X**: *0.0 - 1.0* Desliza as partes esquerda e direita sobre o eixo X.
* **Offset2Y**: *0.0 - 1.0* Desliza as partes esquerda e direita sobre o eixo Y.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/noise1ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
