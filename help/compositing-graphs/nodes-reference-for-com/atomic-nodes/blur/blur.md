---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blur.html"
breadcrumb-title: ''
description: Use o nó Desfoque para aplicar efeitos de desfoque ao textura para suavizar detalhes e criar efeitos de foco suave.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desfoque
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 6%

---


# Desfoque

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![Ícone de nó de desfoque](blur.resources/blur-9.png){width="200px"}

**Entrada:** Nós Atômicos

**Simples**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrição

O Nó de desfoque executa uma operação de “desfoque de caixa”: calculando a média dos valores de pixels em uma distância definida, resultando em uma aparência difusa e não nítida. Ela fornece a operação de desfoque mais simples, rápida e básica disponível no [Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html).

Embora o desfoque funcione bem para operações rápidas e simples, como suavizar ligeiramente algumas bordas, em qualquer cenário mais exigente, o [Desfoque da sede](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/blur-hq/blur-hq.md) é uma escolha melhor, trocando o desempenho pela qualidade.

</td>
</tr>
</table>

## Parâmetros

* **Intensidade**: 0-ilimitada\
  Define a intensidade ou distância do desfoque. O número não é limitado, mas em valores altos a imagem inteira se transforma em uma cor média.

O Exemplo a seguir mostra o Desfoque deste nó à esquerda, em comparação ao [Desfoque HQ](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/blur-hq/blur-hq.md) à direita, ao usar valores altos (50 neste caso). Em valores de cerca de 1-2, a diferença não é perceptível.

| Desfoque (atômico) | Desfoque HQ |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_dynamic_grid_items_grid-cell_position-par_image" src="blur.resources/blur-example.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c1_dynamic_grid_items_grid-cell_position-par_image" src="blur.resources/blur-hq.png"/></div> |
