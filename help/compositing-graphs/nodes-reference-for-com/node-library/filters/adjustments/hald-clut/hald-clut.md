---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/hald-clut.html"
breadcrumb-title: ''
description: Use o nó Hald CLUT para aplicar tabelas de pesquisa de cores usando o formato Hald CLUT para correção e correção de cores.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Hald CLUT
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Hald CLUT
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 4%

---


# Hald CLUT

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/hald-clut.png){width="128px"}

<b>Entrada:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Aplica uma LUT na imagem de entrada. A LUT deve estar no formato Hald na resolução 4096\*4096. Consulte <http://www.quelsolaar.com/technology/clut.html> para obter mais informações.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>entrada</b> <i>Entrada de cores</i> | Imagem na qual aplicar o LUT. |
| <b>lut</b> <i>Entrada de cores</i> | Slot de entrada Lut. Deve ser de 4096 x 4096. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Intensidade LUT por Alpha</b> <i>Falso/Verdadeiro</i> | Define se o efeito LUT é ponderado pelo canal alfa. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/content-hald-clut.jpg" />
        </td>
    </tr>
</table>
