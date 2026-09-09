---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/slope-blur.html"
breadcrumb-title: ''
description: Use o nó Desfoque de Inclinação para aplicar efeitos de desfoque direcional com base nas inclinações do mapa de height para criar desfoque de movimento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Slope Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desfoque de inclinação
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5efb14d81ad72b1982785319e446d7eb318c9a03
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 3%

---


# Desfoque de inclinação

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](slope-blur.resources/slope-blur.png){width="128px"}

![](slope-blur.resources/slope-blur-grayscale.png){width="128px"}

<b>Entrada:</b> Filtros > Desfoques

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Executa um desfoque avançado de Alta Qualidade em que a Anisotropia/Direção é orientada por um “Mapa de Inclinação” em Tons de Cinza. Imagine-o como o efeito Desfoque de Inclinação seguindo as inclinações do seu Mapa de Inclinação como se ele fosse um Heightmap, semelhante à [Distorção direcional](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) (na qual ele se baseia internamente).

Este é um dos desfoques mais interessantes e poderosos do Designer. Ele pode ser usado para obter alguns efeitos muito interessantes e inesperados, como lascas e bordas de intemperismo ou manchas e vazamento de dirt ou ferrugem.

Importante: certifique-se de usar a versão apropriada para sua entrada! Use “Desfoque de Inclinação” para entradas de Cor ou “Desfoque de Inclinação em Tons de Cinza” para entradas de Tons de Cinza.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Inclinação</b> <i>Entrada em tons de cinza</i> | Inclinação o mapa para determinar o ângulo da anisotropia. O ideal é conter gradientes em declive; transições ásperas e nítidas não funcionarão bem! |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Amostras</b> <i>0 - 32</i> | A quantidade de amostras afeta a qualidade em detrimento da velocidade. |
| <b>Intensidade</b> <i>0.0 - 16.0</i> | Quantidade ou intensidade de desfoque. |
| <b>Modo</b> <i>Desfoque, Mín, Máx</i> | Modo de mesclagem para passagens de desfoque subsequentes. “Desfoque” se comporta mais como um [Desfoque anisotrópico](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md) padrão, enquanto Min “corroerá” as áreas existentes e Max “manchará” as áreas brancas. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="slope-blur.resources/slopeblur01.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="slope-blur.resources/slopeblur02.gif" />
        </td>
    </tr>
</table>
