---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/difference.html"
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
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 7%

---


# Diferença

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/difference.png){width="128px"}

<b>Entrada:</b> Filtros > Mesclagem

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Executa um modo de mesclagem Diferença entre as entradas de Primeiro Plano e Plano de Fundo. Subtrai o plano de fundo do primeiro plano, retornando um resultado absoluto (nunca um valor negativo).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Fundo</b> <i>Entrada de cores</i> |  |
| <b>Primeiro Plano</b> <i>Entrada de cores</i> |  |
| <b>Máscara</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Mesclar opacidade entre primeiro plano e plano de fundo. |
| <b>Mesclagem de alfa</b> <i>Falso/Verdadeiro</i> | Alterna a mesclagem dos canais alfa Primeiro plano e Plano de fundo. Se definido como Falso, o canal alfa do primeiro plano é ignorado. |
