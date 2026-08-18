---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-grayscale-color.html"
breadcrumb-title: ''
description: Use o nó Cor de Flood Fill para tons de cinza a fim de preencher regiões conectadas com cores em tons de cinza para criar padrões monocromáticos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to GrayscaleColor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill para Tons de cinza
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 2%

---


# Flood Fill para tons de cinza/cor

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-grayscale.png){width="128px"}

![](../../../../../../assets/floodfill-to-color.png){width="128px"}

## Flood Fill para tons de cinza/cor aleatórios

**Entrada:** *Filtros/Efeitos*

**&#x200B;**&#x200B;Simples&#x200B;**&#x200B;**

</td>
<td style="border: 0;" valign="top">

## Descrição

Usa dados de Flood Fill para gerar amostras de valores de tons de cinza ou de cores. Diferentemente de [Flood Fill para Tons de Cinza Aleatórios](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md), esses dois nós permitem mais controle para definir a variação exata e os tons, com um mapa de entrada extra adicional para determinar o valor base a ser aleatório por célula.

É um sistema poderoso para dar a cada célula um valor ou cor única, mas ainda manter o controle e baseá-lo em uma entrada predeterminada.

## Parâmetros

### Entradas

* **Flood Fill**: *Entrada de cores*
* **Entrada em Tons de Cinza/Cores**: *Entrada em Tons de Cinza/Cores*

### Parâmetros

* **Ajuste de Luminância/Cor**: *-1.0 - 1.0* Defina o valor de polarização ou base para o nó. Quando uma entrada Tons de cinza ou Cor é usada, isso é usado para alterar esse valor inicial como ponto de partida.
* **Luminância/Cor Aleatória**: *-1.0 - 1.0* Defina a quantidade de variação.

</td>
</tr>
</table>
