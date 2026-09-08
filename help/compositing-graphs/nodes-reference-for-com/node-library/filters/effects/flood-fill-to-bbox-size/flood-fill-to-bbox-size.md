---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-bbox-size.html"
breadcrumb-title: ''
description: Use o nó Flood Fill para tamanho de caixa para preencher regiões com valores de tamanho de caixa delimitadora a fim de obter efeitos processuais de escala.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to BBox Size
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tamanho do Flood Fill para a caixa
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---


# Tamanho do Flood Fill para a caixa

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-to-bbox-size.png){width="128px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera um mapa em tons de cinza a partir de uma base [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md), com valores vinculados ao tamanho individual de cada ladrilho.

Os valores são relativos ao tamanho total da tela de desenho (um ladrilho branco completo significaria que ela estica toda a tela de desenho), portanto, o contraste geralmente é baixo.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Saída</b> <i>max(X, Y), X, Y</i> | Define em qual métrica o valor se baseia: largura, comprimento ou ambos. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/floodbbox-ex1.png" />
        </td>
    </tr>
</table>
