---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-gradient.html"
breadcrumb-title: ''
description: Use o nó Flood Fill para gradiente a fim de preencher regiões com valores de gradiente a fim de criar transições de cores suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill para Gradiente
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---


# Flood Fill para Gradiente

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-gradient.png){width="128px"}

## Flood Fill para Gradiente

**Entrada:** *Filtros/Efeitos*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Transforma uma base [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) em gradientes (orientados aleatoriamente). Muito útil para criar um Heightmap onde os ladrilhos são aleatoriamente inclinados e inclinados.

## Parâmetros

### Entradas

* **Flood Fill**: *Entrada de cores* Dados de Flood Fill base.
* **Entrada De Ângulo**: *Entrada Em Tons De Cinza*\
  Mapa opcional para determinar o ângulo por célula com um mapa externo.
* **Entrada de Inclinação**: *Entrada em tons de cinza* Mapa opcional para determinar a intensidade de inclinação do gradiente por célula.

### *Parâmetros*

* **Ângulo**: *0.0 - 1.0* Define o ângulo/direção global uniforme para todos os blocos.
* **Variação de Ângulo**: *0.0 - 1.0* Torna aleatório o ângulo de cada bloco individualmente. Este é o parâmetro mais útil e poderoso!
* **Multiplicar pelo Tamanho da Caixa Delimitadora**: *0.0 - 1.0* Dimensiona todo o efeito linear pelo tamanho da caixa delimitadora individual do bloco. Isso significa que os ladrilhos menores acabarão sendo mais escuros do que os maiores.
* **Multiplicador de entrada de imagem de ângulo**: *0.0 - 1.0* Definir a influência do mapa de entrada de ângulo opcional nas direções de gradiente geradas
* **Multiplicador de Entrada de Imagem de Inclinação**: *0.0 - 1.0*\
  Defina a influência do mapa de entrada de Inclinação opcional na intensidade de inclinação do gradiente gerado.
* **Multiplicar por Intensidade de Inclinação**: *0.0 - 1.0*
* **Cor de Inclinação simples**: *(valor de tons de cinza)*Permite a configuração de valor sólido para inclinações planas.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/floodgradient-ex2.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/floodgradient-ex1.png" width="256px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
