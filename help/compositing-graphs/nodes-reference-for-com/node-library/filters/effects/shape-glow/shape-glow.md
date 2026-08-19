---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-glow.html"
breadcrumb-title: ''
description: Use o nó Brilho da forma para adicionar efeitos de brilho a formas e texturas para criar efeitos visuais luminosos e atmosféricos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Brilho da forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---


# Brilho da forma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-glow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-glow.png){width="128px"}

## Brilho da forma (tons de cinza)

**Entrada:** *Filtros/Efeitos*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Cria um brilho suave ao redor de uma máscara de entrada (para a versão em tons de cinza) ou de uma forma com um canal alfa (para a versão colorida). Em comparação ao [Brilho](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/glow/glow.md), ele funciona de maneiras mais semelhantes a outros softwares de edição de imagens 2D, pois é um efeito mais completo com mais controles.

## Parâmetros

* **Modo**: *Suave, Preciso* Alterna entre dois modos de precisão.
* **Largura**: *-1.0 - 1.0* Controla o quanto o brilho alcança.
* **Propagação**: *0.0 - 1.0* Corte/limite para o efeito de desfoque, faz com que o brilho pareça sólido próximo à forma.
* **Opacidade**: *0.0 - 1.0*\
  Opacidade de mesclagem para o efeito de brilho.
* **(Sombra) Cor**: *(Valor da cor)*Tonalidade da cor a ser aplicada ao brilho.
* **Cor da máscara**: *(Valor da cor) *(Somente versão em tons de cinza)**Cor sólida a ser usada para a saída mapeada de transparência.
* **A Entrada É Pré-Multiplicada**: *False/True *(Somente Versão de Cor)**Se a entrada deve ser assumida como pré-multiplicada.
* **Saída de Pré-Multiplicação**: *Falso/Verdadeiro* Se a saída deve ser pré-multiplicada.

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shapeglow-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
