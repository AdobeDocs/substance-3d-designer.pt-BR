---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/quad-transform.html"
breadcrumb-title: ''
description: Use o nó Transformo Quad para aplicar transformações quadrilaterais ao textura para correção e distorção de Perspectiva.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Quad Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformação quádrupla
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---


# Transformação quádrupla

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](quad-transform.resources/quad-transform-01.png){width="128px"}

![](quad-transform.resources/quad-transform-02.png){width="128px"}

<b>Entrada:</b> Filtros > Transformas

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Nó de transformo especial que permite a transformação de uma forma quádrupla por meio da interação com seus pontos de vértice. Permite transformas muito específicas de maneira prática.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>p00</b> | Ponto superior esquerdo. |
| <b>p01</b> | Ponto inferior esquerdo |
| <b>p10</b> | Ponto Superior Direito. |
| <b>p11</b> | Ponto inferior direito. |
| <b>Selecionando</b> <i>Somente frente, somente trás, frente sobre trás, frente sobre frente</i> | Definir remoção/ocultação de forma quando os pontos se cruzam. |
| <b>Habilitar divisão em blocos</b> <i>Falso/Verdadeiro</i> |  |
| <b>Cor do plano de fundo</b> <i>(Valor em tons de cinza)</i> | Cor de fundo sólida se a divisão em blocos gráficos estiver desativada. |
| <b>Amostragem</b> <i>Bilinear, Mais Próximo</i> | Defina a qualidade da amostragem. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="quad-transform.resources/quad-transform-03.gif" />
        </td>
    </tr>
</table>
