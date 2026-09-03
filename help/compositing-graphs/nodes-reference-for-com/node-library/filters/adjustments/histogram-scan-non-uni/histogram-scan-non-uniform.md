---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan-non-uniform.html"
breadcrumb-title: ''
description: Use o nó Não uniforme de varredura do histograma para executar a varredura não uniforme do histograma para correção avançada de cores.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan Non-Uniform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Varredura de histograma não uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 3%

---


# Varredura de histograma não uniforme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-scan-non-uniform.resources/histogram-scan-non-uniform-01.png){width="128px"}

<b>Entrada:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Versão avançada do [Varredura de histograma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), com controles e entrada adicionais para orientar o efeito em um nível por pixel, em vez de uniformemente em toda a imagem. Pode ser usado para obter contraste e transições ainda mais complexos em máscaras.

É muito mais complexo de usar do que a [Verificação do histograma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) comum, portanto, certifique-se de estar familiarizado antes de tentar usar a versão Não Uniforme.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Entrada em tons de cinza</i> | Resultado de origem a ser modificado. |
| <b>Mapa de posições</b> <i>Entrada em tons de cinza</i> | Slot de entrada para o parâmetro de posição da unidade. Ativado quando “Usar entrada de posição” estiver definido como Verdadeiro. O intervalo de valores efetivo é pequeno e depende do mapa e da configuração de Contraste. |
| <b>Mapa de Contraste</b> <i>Entrada em tons de cinza</i> | Slot de entrada para definir o parâmetro de contraste. Ativado quando “Usar entrada de contraste” estiver definido como Verdadeiro. O intervalo de valor efetivo é pequeno. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Usar Entrada de Posição</b> <i>Falso/Verdadeiro</i> | Alternar o uso do slot de entrada do Mapa de Posição. |
| <b>posição</b> <i>0.0 - 1.0</i> | Controla ou modifica os resultados do mapa para orientar a configuração de posição. |
| <b>Usar entrada de contraste</b> <i>Falso/Verdadeiro</i> | Alterna o uso do slot de entrada do Mapa de Contraste. |
| <b>contraste</b> <i>0.0 - 1.0</i> | Controla ou modifica os resultados do mapa para orientar a configuração de contraste. |
