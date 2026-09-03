---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/trapezoid-transform.html"
breadcrumb-title: ''
description: Use o nó Transformação trapezoide para aplicar distorção trapezoidal às texturas para criar efeitos de correção de perspectiva.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Trapezoid Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformação Trapezoide
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 6%

---


# Transformação Trapezoide

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](trapezoid-transform.resources/trapezoid-transform-01.png){width="128px"}

![](trapezoid-transform.resources/trapezoid-transform-02.png){width="128px"}

<b>Entrada:</b> Filtros > Transformas

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Nó de transformação especial que modifica a entrada em uma maneira de distorção de perspectiva/trapezoide. Tem controle para alongamento superior e inferior. Os valores podem ser ultrapassados os limites para efeitos mais fortes.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Esticamento Superior</b> <i>0.0 - 1.0</i> | Defina a quantidade de esticar ou esmagar na parte superior. |
| <b>Esticamento inferior</b> <i>0.0 - 1.0</i> | Defina a quantidade de esticar ou esmagar na parte inferior. |
| <b>Cor do plano de fundo</b> <i>(Valor de tons de cinza/cor)</i> | Defina a cor do plano de fundo sólido caso a divisão em blocos gráficos esteja desativada. |
| <b>Amostragem</b> <i>Bilinear, Mais Próximo</i> | Defina a qualidade da amostragem. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="trapezoid-transform.resources/trapezoid-transform-03.gif" />
        </td>
    </tr>
</table>
