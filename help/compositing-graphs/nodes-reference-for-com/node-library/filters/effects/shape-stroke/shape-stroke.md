---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-stroke.html"
breadcrumb-title: ''
description: Use o nó Traçado de forma para adicionar contornos de traçado a formas para criar bordas e efeitos de borda.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Stroke
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Traçado da forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---


# Traçado da forma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-stroke.png){width="128px"}

![](../../../../../../assets/shape-stroke-grayscale.png){width="128px"}

## Traçado da forma (tons de cinza)

**Entrada:** *Filtros/Efeitos*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Adiciona um traçado ou contorno em torno de uma máscara em preto e branco (para a versão em tons de cinza) ou de uma forma com um canal alfa (para a versão colorida), como você já deve estar familiarizado com outros aplicativos de edição de imagens 2D. Pode ser visto como uma versão mais completa da [Detecção de borda](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md).

Muito útil para diversos efeitos de edição de imagens.

## Parâmetros

* **Largura**: *-1.0 - 1.0* Largura do efeito de traçado.
* **Opacidade**: *0.0 - 1.0*\
  Opacidade global do efeito.
* Cor **(Contorno)**: *(Valor da cor)*Cor usada para o efeito de contorno.
* **Cor da máscara**: *(Valor da cor) *(Somente versão em tons de cinza)**Cor sólida a ser usada para a saída mapeada de transparência.
* **A Entrada É Pré-Multiplicada**: *False/True *(Somente Versão de Cor)**Se a entrada deve ser assumida como pré-multiplicada.
* **Saída de Pré-Multiplicação**: *Falso/Verdadeiro* Se a saída deve ser pré-multiplicada.

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shapestroke-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
