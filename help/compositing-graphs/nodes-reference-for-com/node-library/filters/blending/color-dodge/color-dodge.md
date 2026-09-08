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
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 9%

---


# Subexposição de cor

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/color-dodge.png){width="128px"}

<b>Entrada:</b> Filtros > Mesclagem

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Executa uma mesclagem de Subexposição de Cor. Matematicamente, a fórmula é Background / (1- Primeiro Plano).

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
