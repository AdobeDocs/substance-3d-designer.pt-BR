---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-blend.html"
breadcrumb-title: ''
description: Use o nó Mesclagem normal para mesclar mapas normais para criar transições suaves entre os detalhes da superfície.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mesclagem normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---


# Mesclagem normal

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-blend.png){width="128px"}

## Mesclagem normal

**Entrada:** *Filtros/Mapa Normal*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

A Mesclagem normal permite mesclar dois Mapas normais com uma máscara opcional, garantindo que todos os valores permaneçam normalizados. Ele não difere muito de um [Nó de mesclagem atômico](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md), mas adicionou cálculos internos para os Mapas Normais.

A Mesclagem normal não se destina a combinar (sobrepor) Mapas normais, enquanto o mapa superior adiciona detalhes ao mapa inferior. Para isso, use a [Combinação normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-combine/normal-combine.md).

## Parâmetros

### Entradas

* **NormalFG**: *Entrada de Cores*\
  Normalmap em Primeiro Plano/Superior.
* **NormalBG**: *Entrada de cores*\
  Mapa Normal De Fundo/Inferior.
* **Máscara**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó. Pode ser alternado com o parâmetro “Usar máscara”.

### Parâmetros

* **Opacidade**: *0.0 - 1.0*\
  Mesclar opacidade entre o primeiro plano e o plano de fundo
* **Usar máscara**: *Falso/Verdadeiro*\
  Ativa ou desativa o uso do Mapa de máscaras.

## Imagens de exemplo

![](../../../../../../assets/normalblend-ex.gif)

O formato *(.gif introduz pontilhamento no exemplo, os resultados no aplicativo são suaves)*

</td>
</tr>
</table>
