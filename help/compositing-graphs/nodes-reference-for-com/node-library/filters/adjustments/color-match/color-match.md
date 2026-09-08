---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-match.html"
breadcrumb-title: ''
description: Use o nó Correspondência de cores para corresponder cores entre texturas para criar paletas de cores consistentes e harmonizar texturas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color Match
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Correspondência de cores
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---


# Correspondência de cores

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/color-match-3.png){width="128px"}

<b>Entrada:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Tenta corresponder o intervalo de *Cores de Origem* definido a um intervalo de *Cores de Destino*, com suporte para slots de entrada para definir Origem e Destino.

Para versões mais simples, consulte [Substituir intervalo de cores](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color-range/replace-color-range.md) ou [Substituir cor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color/replace-color.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Entrada de cores</i> | Entrada principal a ser modificada para resultado. |
| <b>Cor de origem</b> <i>Entrada de cores</i> | Slot de entrada para cor de Origem, usado somente quando o &#39;Modo de Cor de Origem&#39; está definido como *Entrada*. |
| <b>Cor de Destino</b> <i>Entrada de cores</i> | Slot de entrada para cor de Destino, usado somente quando &#39;Modo de Cor de Destino&#39; está definido como *Entrada*. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Modo de Cores de Origem</b> <i>Média, Parâmetro, Entrada</i> | Define se a Cor de origem é definida pela média da imagem de entrada, pela definição de um parâmetro ou pelo uso de um slot de entrada. |
| <b>Cor de origem</b> <i>(Valor da cor)</i> | Se o Modo de Cores de Origem estiver definido como *Parâmetro*, esse parâmetro determinará a Cor de Origem. |
| <b>Modo de Cores de Destino</b> <i>Parâmetro, Entrada de Imagem</i> | Define se a Cor de origem é definida pela média da imagem de entrada, pela definição de um parâmetro ou pelo uso de um slot de entrada. |
| <b>Cor de Destino</b> <i>(Valor da cor)</i> | Se o Modo de Cor de Destino estiver definido como *Parâmetro*, esse parâmetro determinará a Cor de Destino. |
| <b>Variação de cor personalizada</b> <i>Falso/Verdadeiro</i> | Ativa uma variação de cor adicional. |
| <b>Variação de cor</b> | Define as variações de Matiz, Crominância ou Luminância para o resultado, se ativadas. |
| <b>Usar máscara</b> <i>Falso/Verdadeiro</i> | Alterna o uso de Entrada ou Saída de máscara, dependendo do Modo de máscara abaixo. |
| <b>Modo de máscara</b> <i>Parâmetro, Entrada</i> | O modo de parâmetro gera uma máscara que detalha como a cor foi alterada. O modo de entrada permite que uma máscara controle a intensidade do efeito Correspondência de cores. |
| <b>Máscara</b> | Gera a saída de uma máscara mostrando onde exatamente o efeito Correspondência de cores foi aplicado, com controles adicionais para suavizar e desfocar a máscara resultante. |
