---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/dissolve.html"
breadcrumb-title: ''
description: Use o nó Dissolver para mesclar texturas usando o modo Dissolver para criar efeitos de transição e atenuação entre texturas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Dissolve
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dissolver
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 7%

---


# Dissolver

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dissolve.resources/dissolve-2.png){width="128px"}

<b>Entrada:</b> Filtros > Mesclagem

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Mescla duas entradas com o Ruído branco como máscara para a transição.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Primeiro Plano</b> <i>Entrada de cores</i> |  |
| <b>Fundo</b> <i>Entrada de cores</i> |  |
| <b>Máscara</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Mesclar opacidade entre primeiro plano e plano de fundo. |
| <b>Mesclagem de alfa</b> <i>Falso/Verdadeiro</i> | Alterna a mesclagem dos canais alfa Primeiro plano e Plano de fundo. Se definido como Falso, o canal alfa do primeiro plano é ignorado. |
