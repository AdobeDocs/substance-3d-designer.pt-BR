---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-blend.html"
breadcrumb-title: ''
description: Use o nó Combinar normal para mesclar mapas normais para criar transições suaves entre os detalhes da superfície.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Combinar normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 3%

---


# Combinar normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-blend.resources/normal-blend.png){width="128px"}

<b>Entrada:</b> Filtros > Mapa normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O Combinar normal permite mesclar dois Mapas normais com uma máscara opcional, garantindo que todos os valores permaneçam normalizados. Ele não difere muito de um [nó de Combinar atômico](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md), mas adicionou cálculos internos para Normalmaps.

O Combinar normal não se destina a combinar (sobrepor) mapas normais, onde o mapa superior adiciona detalhes ao mapa inferior. Para isso, use a [Combinação normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-combine/normal-combine.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>NormalFG</b> <i>Entrada de cores</i> | Normalmap em Primeiro Plano/Superior. |
| <b>NormalBG</b> <i>Entrada de cores</i> | Mapa Normal De Fundo/Inferior. |
| <b>Máscara</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. Pode ser alternado com o parâmetro “Usar máscara”. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Mesclar opacidade entre o primeiro plano e o plano de fundo |
| <b>Usar máscara</b> <i>Falso/Verdadeiro</i> | Ativa ou desativa o uso do Mapa de máscaras. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            O formato <img src="normal-blend.resources/normalblend-ex.gif" /><br><i>(.gif introduz pontilhamento no exemplo, os resultados no aplicativo são suaves)</i>
        </td>
    </tr>
</table>
