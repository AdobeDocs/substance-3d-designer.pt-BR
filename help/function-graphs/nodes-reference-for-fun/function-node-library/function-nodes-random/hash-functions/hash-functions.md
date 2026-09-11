---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/function-node-library/function-nodes-random/hash-functions.html"
breadcrumb-title: ''
description: Use funções hash em gráficos de função para gerar valores aleatórios determinísticos com base em coordenadas de entrada.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Function node library > Random > Hash
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Funções de hash
user-guide-description: ''
user-guide-title: ''
source-git-commit: 81c39001686736d41614fd59247d53e6d8438def
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 1%

---


# Funções de hash

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó de hash: ícone](hash-functions.resources/hash-icon.png "Nó de hash: ícone"){width="200px"}

<b>Em:</b> Funções > Aleatório

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Calcula um valor pseudo-aleatório entre 0 e 1, com base em um valor de entrada usado como uma semente.

O número no título mostra o tipo de valor de entrada e saída. Por exemplo: Hash 23 assume um valor float2 como entrada e gera um valor float3.

</td>
</tr>
</table>

Quando um nó Hash gera um valor de vários componentes, cada componente tem um valor pseudo-aleatório diferente.

Versões disponíveis, com seu tipo de entrada e tipo de saída:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Hash 11:</b> Precisão decimal → Precisão decimal

<b>Hash 14:</b> Precisão decimal → Precisão decimal 4

<b>Hash 21:</b> Precisão decimal 2 → Precisão decimal

<b>Hash 22:</b> Precisão decimal2 → Precisão decimal2

</td>
<td style="border: 0;" valign="top">

<b>Hash 24:</b> Precisão decimal2 → Precisão decimal4

<b>Hash31:</b> Precisão decimal 3 → Precisão decimal

<b>Hash 32:</b> Precisão decimal3 → Precisão decimal2

</td>
</tr>
</table>

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> | O valor usado como uma semente para calcular a saída pseudo-aleatória. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de hash 14](hash-functions.resources/hash14-example.png "Exemplo de hash 14"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Exemplo de hash 32](hash-functions.resources/hash32-example.png "Exemplo de hash 32"){zoomable="yes"}

</td>
</tr>
</table>
