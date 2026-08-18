---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-dodge.html"
breadcrumb-title: ''
description: Use o nó de mesclagem Subexposição de Cor para clarear texturas diminuindo o contraste para criar efeitos de realce e brilho.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color Dodge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Subexposição de cor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 10%

---


# Subexposição de cor

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-dodge.png){width="128px"}

## Subexposição de cor

**Entrada:** *Filtros/Mesclagem*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Executa uma mesclagem de Subexposição de Cor. Matematicamente, a fórmula é Background / (1- Primeiro Plano).

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
