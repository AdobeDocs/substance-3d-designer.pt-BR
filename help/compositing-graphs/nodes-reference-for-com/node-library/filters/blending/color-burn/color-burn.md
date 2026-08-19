---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-burn.html"
breadcrumb-title: ''
description: Use o nó de mesclagem Superexposição de cores para escurecer texturas aumentando o contraste para criar efeitos de sombra e superexposição.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color Burn
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Superexposição de cor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 9%

---


# Superexposição de cor

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-burn.png){width="128px"}

## Superexposição de cor

**Entrada:** *Filtros/Mesclagem*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Executa uma mesclagem de Superexposição de Cor entre o Primeiro Plano e o Plano de Fundo. Matematicamente, a fórmula é 1 - (1-Background) / Primeiro Plano.

## Parâmetros

### Entradas

* **Primeiro Plano**: *Entrada de Cores*
* **Fundo**: *Entrada de Cores*
* **Máscara**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Opacidade**: *0.0 - 1.0*\
  Mesclar opacidade entre primeiro plano e plano de fundo.
* **Mesclagem de Alpha**: *Falso/Verdadeiro*\
  Alterna a mesclagem dos canais alfa Primeiro plano e Plano de fundo. Se definido como Falso, o canal alfa do primeiro plano é ignorado.

## Imagens de exemplo

</td>
</tr>
</table>
