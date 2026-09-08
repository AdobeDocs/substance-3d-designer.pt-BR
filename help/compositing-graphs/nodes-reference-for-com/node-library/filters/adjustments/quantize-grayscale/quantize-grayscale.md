---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/quantize-grayscale.html"
breadcrumb-title: ''
description: Use o nó Quantificar Tons de Cinza para reduzir o número de níveis de tons de cinza para efeitos de posterização.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Quantize Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Quantificar escala de cinza
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 1%

---


# Quantificar escala de cinza

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone Quantizar Escala de Cinza](../../../../../../assets/quantize-grayscale.png "ícone Quantizar Escala de Cinza"){width="200px"}

<b>Entrada:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma única spline na forma de um círculo.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Etapas</b> *Inteiro* | O número de valores separados para os quais o intervalo de entrada deve ser aproximado. |
| <b>Deslocamento</b> *Flutuante* | Aplica um deslocamento ao intervalo de entrada, que *desloca* os resultados ao longo do intervalo. |
| <b>Inclinação</b> *Flutuante* | Aplica um gradiente de inclinação às *transições* entre valores aproximados, até o *intervalo completo de uma etapa*. |
| <b>Curva de Inclinação</b> *Inteiro* | Define o método de aquisição da curva para a inclinação definida pelo parâmetro <b>Inclinação</b>:<ul data-preserve-html="true"> <li data-preserve-html="true">*Linear*: aplica uma curva linear, resultando em uma inclinação reta</li> <li data-preserve-html="true">*Etapa suave*: aplica uma curva de etapa suave, resultando em uma inclinação suave</li> <li data-preserve-html="true">*Entrada de curva*: aplica a curva descrita pelo mapa de entrada <b>Entrada de curva</b>. Você pode usar um nó [Curva](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) para descrever esta curva com uma grande quantidade de controle.</li> </ul> |

## Exemplos

![Exemplo 1](../../../../../../assets/quantizegrayscale.gif "Exemplo 1")

![Exemplo 2](../../../../../../assets/quantizegrayscale.png "Exemplo 2")
