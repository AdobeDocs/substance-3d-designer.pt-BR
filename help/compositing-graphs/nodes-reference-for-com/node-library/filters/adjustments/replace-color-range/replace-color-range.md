---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/replace-color-range.html"
breadcrumb-title: ''
description: Use o nó Substituir intervalo de cores para substituir cores dentro de um intervalo especificado por novas cores para a correção de cores.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Replace Color Range
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substituir gama de cores
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 5%

---


# Substituir gama de cores

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/replace-color-range.png){width="128px"}

<b>Entrada:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Substitui a cor de origem pela cor de destino, com controles adicionais. Pode, por exemplo, ser usado para recolorir partes de um mapa de ID de material (bolo).

Para uma versão mais avançada, consulte [Correspondência de cores.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-match/color-match.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Cor de origem</b> <i>(Valor da cor)</i> | Cor para substituir. |
| <b>Cor de Destino</b> <i>(Valor da cor)</i> | Cor para substituir. |
| <b>Intervalo de Origem</b> <i>0.0 - 1.0</i> | Faixa ou tolerância da Origem separada. Pode ser aumentado para que outras cores vizinhas também tenham o matiz alterado. |
| <b>Limite</b> <i>0.0 - 1.0</i> | Queda/contraste da faixa. Defina como baixo para substituir apenas a cor de origem, definido como um valor maior para substituir as cores misturadas na origem. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/replace-color-range-example.png" />
        </td>
    </tr>
</table>
