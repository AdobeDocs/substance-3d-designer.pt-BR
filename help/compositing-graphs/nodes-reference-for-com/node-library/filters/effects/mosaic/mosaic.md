---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/mosaic.html"
breadcrumb-title: ''
description: Use o nó Mosaico para criar efeitos de ladrilho do mosaico, dividindo texturas em blocos e padrões pixelados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Mosaic
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mosaico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 7%

---


# Mosaico

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](mosaic.resources/mosaic-1.png){width="128px"}

![](mosaic.resources/mosaic-grayscale.png){width="128px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Enfatiza um mapa de degradê existente, suave e em declive executando um efeito de [Distorção](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) de várias passagens. Quando o mesmo mapa é usado para ambas as entradas, ele essencialmente cresce e acentua as áreas mais brilhantes.

Isso é útil para adicionar mais definição a mapas em tons de cinza, como o Mapa de altura, pois pode introduzir mais definição em formas.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Cor</b> <i>Entrada de Cores/Tons de Cinza</i> |  |
| <b>Mapa de mosaico</b> <i>Entrada em tons de cinza</i> | Distorcer mapa de driver. Pode ser o mesmo que a primeira entrada. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Amostras</b> <i>0 - 16</i> | Determina a qualidade de várias amostras. |
| <b>Intensidade</b> <i>0.0 - 1.0</i> | Intensidade do efeito. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="mosaic.resources/mosaci-ex.png" />
        </td>
    </tr>
</table>
