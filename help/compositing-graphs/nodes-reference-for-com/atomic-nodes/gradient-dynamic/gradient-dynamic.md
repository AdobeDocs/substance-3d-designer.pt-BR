---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/gradient-dynamic.html"
breadcrumb-title: ''
description: Use o nó Gradiente (dinâmico) para criar gradientes dinâmicos que podem ser controlados por valores e parâmetros de entrada.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Gradient (Dynamic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gradiente (dinâmico)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 9%

---


# Gradiente (dinâmico)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: dinâmico do gradiente](gradient-dynamic.resources/gradient-dynamic-01.png "Nó atômico: dinâmico do gradiente"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Remapeia os valores de tons de cinza em uma imagem, usando um gradiente fornecido por uma linha ou coluna de pixels em outra imagem.

Ele serve como uma ligeira alternativa ao Nó Gradiente, mas, diferentemente do nó Gradiente, as chaves de cor de Gradiente não são definidas internamente, mas vêm de uma entrada externa.

</td>
</tr>
</table>

Isso permite principalmente evitar o problema em que os parâmetros não podem ser expostos, pois os parâmetros de cor são movidos para fora do nó. Isso é o que o torna “dinâmico”.

Embora Gradiente (dinâmico) não seja um nó difícil de usar por si só, seus casos de uso são um pouco mais avançados: a maioria dos usos padrão pode ser coberta pelo nó Gradiente normal.

Esse nó entra em ação quando você está muito limitado pelo sistema de chaves do editor de Degradê e deseja que as cores e as posições da rampa sejam orientadas por outras entradas, parâmetros e partes do seu gráfico.

Como alternativa, o controle deslizante Posição de entrada de gradiente pode ser usado para alternar entre vários gradientes armazenados em uma única entrada de Degradê.

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

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Parâmetros

</td>
<td style="border: 0;" valign="top">

### Conectores de entrada

</td>
<td style="border: 0;" valign="top">

### Conectores de saída

</td>
<td style="border: 0;" valign="top">

### Exemplos

</td>
</tr>
</table>

## Parâmetros

|  |  |
| --- | --- |
| <b>Endereçamento de gradiente</b> *Booleano* | Define se o Gradiente se repete (blocos) ou grampos.   Esse parâmetro determina como os pixels HDR do intervalo [0, 1] da entrada em tons de cinza são tratados: apertados ou dobrados até [0, 1]. |
| <b>Orientação do gradiente</b> *Inteiro* | Define o eixo ao longo do qual a “Entrada de gradiente” deve ser amostrada:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Horizontal:</i> faça uma amostra de uma linha de pixels no eixo X.</li> <li data-preserve-html="true"><i>Vertical:</i> faça uma amostra de uma coluna de pixels no eixo Y.</li> </ul> |
| <b>Posição de entrada do gradiente</b> *Flutuante* | A posição normalizada da linha ou coluna de pixels a serem amostrados em &#39;Entrada de gradiente&#39;. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada em tons de cinza</b> *Tons de cinza* PRIMÁRIO | A imagem em tons de cinza para remapear. |
| <b>Entrada de gradiente</b> *Cores/Tons de Cinza* | O gradiente é amostrado a partir desta imagem |

## Conectores de saída

|  |  |
| --- | --- |
| <b>Saída</b> *Cores/Tons de Cinza* |  |

## Exemplos

*Em breve.*
