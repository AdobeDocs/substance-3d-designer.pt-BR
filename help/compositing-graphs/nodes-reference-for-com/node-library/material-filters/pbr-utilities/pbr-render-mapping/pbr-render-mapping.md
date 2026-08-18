---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render-mapping.html"
breadcrumb-title: ''
description: Use o nó Mapeamento de Renderização PBR para converter saídas de material em diferentes formatos de mapeamento de Renderização PBR.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Render Mapping
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mapeamento de renderizações PBR
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# Mapeamento de renderizações PBR

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-render-mapping-color.png)![](../../../../../../assets/pbr-render-mapping-grayscale.png)

## Mapeamento de renderizações PBR (cor/tons de cinza)

**Entrada:** *Filtros de Material/Utilitários PBR*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Este é um nó de extensão para o [nó de Renderização PBR](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md), que permite mapear uma textura separada na forma de uma [Renderização PBR](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md) anterior. Seu principal objetivo é permitir que você remapeie cada canal separado de sua [Renderização PBR](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md), de volta para a forma, para criar detalhamentos de canal de mapa compostos, como nos exemplos abaixo. Você pode criar seu próprio método composto e máscaras usando os nós de mapeamento de Renderização PBR como componente.

Existem versões de cor e tons de cinza para os dois tipos de dados: use cor para mapas difusos, use tons de cinza para mapas de aspereza, metálicos e outros mapas em tons de cinza.

### Entradas

* **Textura**: *Entrada Colorida/Em Tons De Cinza*\
  Textura para mapear na forma.
* **UVs**: *Entrada de cores* Entrada de dados UV obrigatória de um nó de Renderização PBR [.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)

## Parâmetros

* **Cor do plano de fundo**: *(valor da cor)*Defina um valor de cor sólida para usar no plano de fundo.

## Imagens de exemplo

O exemplo é um composto de quatro nós de Mapeamento de Renderização PBR diferentes, usando uma [Seleção de histograma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-select/histogram-select.md) em um [Gradiente linear](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-linear-1/gradient-linear-1.md) como máscaras.

![](../../../../../../assets/pbr-render-mapping-ex.png){width="256px"}

![](../../../../../../assets/pbr-render-mapping-ex-2.png){width="256px"}

</td>
</tr>
</table>
