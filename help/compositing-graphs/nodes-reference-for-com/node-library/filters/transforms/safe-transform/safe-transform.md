---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/safe-transform.html"
breadcrumb-title: ''
description: Use o nó Transformação segura para aplicar transformações enquanto preserva os limites da textura e evita artefatos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Safe Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformação segura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 5%

---


# Transformação segura

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](safe-transform.resources/safe-transform-01.png)

![](safe-transform.resources/safe-transform-02.png)

<b>Entrada:</b> Filtros > Transformas

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Versão lado a lado de [Transformar 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Permite dimensionar, girar e deslocar sem quebrar a divisão em blocos gráficos e sem perder os detalhes de pixels (perda de nitidez) devido a pequenos deslocamentos e rotações.

Útil para transformar o ruído quando o controle máximo ou a nitidez perfeita são necessários.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Bloco</b> <i>1 - 16</i> | Reduz a entrada colocando-a lado a lado. |
| <b>Modo de Deslocamento</b> <i>Manual, Aleatório</i> | Alterna para um deslocamento aleatório em vez de um definido manualmente. |
| <b>Deslocamento</b> <i>0.0 - 1.0</i> | Move ou traduz o resultado. Verifica se os pixels são encaixados e não interpolados. |
| <b>Rotação</b> <i>0.0 - 1.0</i> | Gira a entrada na horizontal. |
| <b>Rotação Segura de Blocos</b> <i>Falso/Verdadeiro</i> | Determina o comportamento da Rotação, se ela deve aderir a valores seguros que não desfocam nenhum pixel. |
| <b>Simetria</b> <i>nenhum, X, Y, X+Y</i> |  |
| <b>Cor do plano de fundo</b> <i>(Valor da cor) (Somente Versão da Cor)</i> |  |
| <b>Modo Mipmap</b> <i>Automático, Manual</i> | Determina o modo mipmapping. Defini-lo como Manual leva a resultados mais nítidos. |
| <b>Nível do mipmap</b> <i>0 - 10</i> | Quando o modo Mipmap está definido como Manual, isso permite escolher um Mipmap diferente. |
