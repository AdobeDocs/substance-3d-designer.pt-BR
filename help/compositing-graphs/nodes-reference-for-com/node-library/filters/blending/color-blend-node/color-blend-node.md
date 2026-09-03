---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-blend-node.html"
breadcrumb-title: ''
description: Use o nó Mesclagem de cores para mesclar texturas usando o modo de cores para preservar a luminância ao alterar o matiz e a saturação.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color (Blend Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cor (Nó de mesclagem)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---


# Cor (Nó de mesclagem)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](color-blend-node.resources/color-blend-node-01.png){width="128px"}

<b>Entrada:</b> Filtros > Mesclagem

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Executa um modo de mesclagem de cores, que preserva a luminância do plano de fundo, ao adotar o matiz e a crominância do primeiro plano.

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
