---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-filter-node.html"
breadcrumb-title: ''
description: Use o nó do filtro Curvatura para gerar mapas de curvatura de mapas de altura para detectar superfícies convexas e côncavas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Curvatura (Nó de filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 07f136ebd89fbe737b6c042f1275bd348b2be514
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# Curvatura (Nó de filtro)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](curvature-filter-node.resources/curvature-1.png){width="128px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Executa uma conversão de curvatura de passagem única simples e áspera para a entrada [Normalmap](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md). O mapa resultante tem tons brancos para áreas convexas e tons pretos para côncavas. A curvatura sempre produzirá linhas finas em pixels e transições nítidas.

Esse nó é útil para um rápido realce ou escurecimento de determinadas bordas. É limitado em comparação à [Curvatura suave](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md) (que produz resultados de maior qualidade) e à [Curvatura sólida](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md) (que tem mais opções).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Intensidade</b> <i>0.0 - 10.0</i> | Intensidade do efeito. Aumenta o contraste do resultado. |
| <b>Formato Normal</b> <i>DirectX, OpenGL</i> | Alterna entre diferentes formatos de Mapas Normais (inverte o canal Verde). |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="curvature-filter-node.resources/curvature-ex.png" />
        </td>
    </tr>
</table>
