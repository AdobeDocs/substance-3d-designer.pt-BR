---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/difference.html"
breadcrumb-title: ''
description: Use o nó de mesclagem Diferença para mesclar texturas usando o modo de diferença para criar efeitos de inversão e contraste.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Difference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Diferença
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 6%

---


# Diferença

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/difference.png){width="128px"}

## Diferença

**Entrada:** *Filtros/Mesclagem*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Executa um modo de mesclagem Diferença entre as entradas de Primeiro Plano e Plano de Fundo. Subtrai o plano de fundo do primeiro plano, retornando um resultado absoluto (nunca um valor negativo).

## Parâmetros

### Entradas

* **Fundo**: *Entrada de Cores*
* **Primeiro Plano**: *Entrada de Cores*
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
