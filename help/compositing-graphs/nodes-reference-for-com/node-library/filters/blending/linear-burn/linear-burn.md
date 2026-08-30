---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/linear-burn.html"
breadcrumb-title: ''
description: Use o nó Superexposição Linear para mesclar texturas usando o modo de gravação linear para criar efeitos de escurecimento e contraste.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Linear Burn
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Superexposição linear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 10%

---


# Superexposição linear

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](linear-burn.resources/linear-burn.png){width="128px"}

<b>Entrada:</b> Filtros > Mesclagem

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Executa uma mesclagem de Superexposição Linear. A fórmula matemática é Primeiro Plano + Fundo - 1.

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
