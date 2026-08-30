---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-append.html"
breadcrumb-title: ''
description: Use o nó Acrescentar spline para anexar várias splines para criar caminhos contínuos mais longos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Append
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Acrescentar Spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---


# Acrescentar Spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](spline-append.resources/spline-append-icon.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

As splines são empacotadas como uma lista. Este nó acrescenta uma lista de splines de entrada (set #2) a uma lista existente (set #1).

A ordem das listas é preservada, o que significa acrescentar uma lista D-E-F a uma lista A-B-C resulta em uma lista A-B-C-D-E-F.

</td>
</tr>
</table>

>[!TIP]
>
> Esteja ciente da ordem na qual você acrescenta splines, pois essa ordem é levada em consideração em outros nós, como [Dispersão em splines](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-on-spline-color/scatter-on-spline-color.md), [Ponte de spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md), etc.

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Visualizar #1</b> <i>Tons de cinza</i> | A visualização do primeiro conjunto de splines de entrada como uma imagem em tons de cinza. |
| <b>Spline #1 Coords</b> <i>Cor</i> | As coordenadas do primeiro conjunto de pontos das linhas divisórias de entrada codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Posição X<br><b>G</b> - Posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br>- Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Dados de Spline #1</b> <i>Cor</i> | Dados adicionais do primeiro conjunto de splines de entrada codificados nos canais RGBA de uma imagem colorida.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usadas<br><b>A</b> - Não Usadas |
| <b>Valor de Spline #1</b> <i>Inteiro</i> | O número de splines de entrada no primeiro conjunto. |
| <b>Visualizar #2</b> <i>Tons de cinza</i> | A visualização do segundo conjunto de splines de entrada como uma imagem em tons de cinza. |
| <b>Spline #2 Coords</b> <i>Cor</i> | As coordenadas do segundo conjunto de pontos das linhas divisórias de entrada codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Posição X<br><b>G</b> - Posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br>- Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Dados de Spline #2</b> <i>Cor</i> | Dados adicionais do segundo conjunto de splines de entrada codificados nos canais RGBA de uma imagem colorida.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usadas<br><b>A</b> - Não Usadas |
| <b>Valor de Spline #2</b> <i>Inteiro</i> | O número de splines de entrada no segundo conjunto. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Visualizar</b> <i>Tons de cinza</i> | A visualização das linhas de saída como uma imagem em tons de cinza. |
| <b>Cordas de spline</b> <i>Cor</i> | As coordenadas dos pontos das linhas divisórias de saída codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Posição X<br><b>G</b> - Posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br>- Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> <i>Cor</i> | Dados adicionais das splines de saída codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usadas<br><b>A</b> - Não Usadas |
| <b>Valor da spline</b> <i>Inteiro</i> | O número de splines de saída. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Inverter Spline #1 Direção</b> <i>Booleano</i> | Inverte a direção das linhas no primeiro conjunto. |
| <b>Inverter Spline #2 Direção</b> <i>Booleano</i> | Inverte a direção das linhas no segundo conjunto. |
| <b>Visualizar</b> |  |
| <b>Valor de Segmentos</b> <i>Inteiro</i> | Ajusta o número de segmentos usados para desenhar a visualização de spline na saída da Visualização. Um valor mais alto resulta em uma linha mais suave. |
| <b>Mostrar Auxiliar de Direção</b> <i>Booleano</i> | Exibe um ponto no início da spline e uma ponta de seta no final da saída de Visualização. |
| <b>Mostrar Envelope de Thickness</b> <i>Booleano</i> | Exibe linhas adicionais nas bordas do thickness da spline. |
| <b>Thickness (px)</b> <i>Flutuante</i> | Ajusta o thickness da visualização da spline em pixels na saída da Visualização. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 1](spline-append.resources/SplineAppend-Demo.jpg "Exemplo de nó 1")

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](spline-append.resources/SplineAppend-Graph.jpg "Exemplo de nó 2")

</td>
</tr>
</table>

![Demonstração de nó](spline-append.resources/SplineAppend-Demo2.gif "Demonstração de nó")
