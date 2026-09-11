---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-sobel.html"
breadcrumb-title: ''
description: Use o nó Curvatura Sobel para detectar bordas de curvatura usando operadores Sobel para criar máscaras baseadas em bordas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Curvatura Sobel
user-guide-description: ''
user-guide-title: ''
source-git-commit: 07f136ebd89fbe737b6c042f1275bd348b2be514
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 4%

---


# Curvatura Sobel

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](curvature-sobel.resources/curvature-sobel.png){width="128px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Executa uma conversão de curvatura de passagem única simples e áspera para a entrada [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md). O mapa resultante tem tons brancos para áreas convexas e tons pretos para côncavas. A curvatura sempre produzirá linhas mais espessas e transições nítidas.

Esse nó é útil para realce ou escurecimento rápido de determinadas bordas. É um pouco diferente da [Curvatura](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md), pois produz resultados de melhor qualidade, mas ainda é nítida e áspera.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Intensidade</b> <i>0.0 - 1.0</i> | Intensidade do efeito, ajusta o contraste. |
| <b>Tipo normal</b> <i>DirectX, OpenGL</i> |  |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="curvature-sobel.resources/curv-sobel-ex.png" />
        </td>
    </tr>
</table>
