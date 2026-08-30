---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/value-processor.html"
breadcrumb-title: ''
description: Use o nó Processador de valores para processar e manipular valores de textura usando operações matemáticas para ajustes personalizados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Value processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Processador de valor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 4%

---


# Processador de valor

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: processador de valor](value-processor.resources/comp_valueprocessor_1.png "Nó atômico: processador de valor"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Computa um [gráfico de função de Substance](../../../../function-graphs/the-function-graph/the-function-graph.md) e gera o resultado.

É comparável a um [processador de pixels](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), com a diferença de que ele não calcula uma função para cada pixel, mas sim um único valor e o torna [disponível em um gráfico de Substance](../../../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md).

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> Este nó é um bom ponto de partida para aprender sobre [gráficos de função Substance](../../../../function-graphs/the-function-graph/the-function-graph.md).
> 
> Considere também que trabalhar com esse tipo de gráfico e executar operações matemáticas é obrigatório para tirar qualquer coisa desse nó.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Conectores de saída

</td>
<td style="border: 0;" valign="top">

### Exemplos

</td>
</tr>
</table>

## Parâmetros

|  |  |
| --- | --- |
| <b>Função de processador de valor</b> *Qualquer tipo de valor disponível* | [gráfico de função Substance](../../../../function-graphs/the-function-graph/the-function-graph.md) avaliado para calcular o valor de saída. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Imagem de entrada #</b> *Tons de cinza/Cor* | Use um nó [Cor de exemplo](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) ou [Tons de cinza de amostra](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) para acessar os valores na entrada do índice especificado. |

## Conectores de saída

|  |  |
| --- | --- |
| <b>Saída</b> *Qualquer tipo de valor disponível* |  |

## Exemplos

*Em breve.*
