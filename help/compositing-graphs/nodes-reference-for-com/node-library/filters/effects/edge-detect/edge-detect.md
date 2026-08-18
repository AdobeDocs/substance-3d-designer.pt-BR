---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/edge-detect.html"
breadcrumb-title: ''
description: Use o nó Detecção de borda para detectar bordas em texturas para criar contornos e efeitos de máscara baseados em bordas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Edge Detect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Detecção de borda
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---


# Detecção de borda

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-detect.png){width="128px"}

## Detecção de borda

**Entrada:** *Filtros/Efeitos*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Detecta o contraste em imagens em preto e branco e, em seguida, cria uma máscara em preto e branco destacando o contraste.

Útil em muitos casos em que algum tipo de máscara para bordas é necessário. Lembre-se de que ele funciona melhor com entradas de alto contraste; se necessário, ajuste o contraste antes de passar algo para esse nó.

## Parâmetros

* **Largura da Borda**: *1.0 - 16.0* Largura das áreas detectadas ao redor das bordas.
* **Arredondamento da borda**: *0.0 - 16.0* Arredonda, desfoca e suaviza a máscara gerada.
* **Inverter**: *Falso/Verdadeiro*\
  Inverte o resultado.
* **Tolerância**: *0.0 - 1.0* Fator de limite de tolerância para onde as bordas devem aparecer.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/edge-detect-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
