---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/point-list.html"
breadcrumb-title: ''
description: Use o nó Lista de pontos para criar e gerenciar listas de pontos para spline e geração de caminho.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Point List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lista de pontos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 1%

---


# Lista de pontos

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](point-list.resources/point-list-icon.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma lista de pontos a serem atravessados por uma spline.

Se uma lista de pontos existente for fornecida para as entradas de <b>Ponto</b>, a lista gerada será anexada à lista de entrada.

</td>
</tr>
</table>

>[!TIP]
>
> Este nó pode ser usado para fornecer pontos para o nó [Spline (Poly Quadratic)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md) para criar splines.

>[!IMPORTANT]
>
> Os conectores da <b>Lista de Pontos</b> e do <b>Número de Pontos</b> são *incompatíveis* com os conectores da <b>Coluna de Spline</b>, dos <b>Dados de Spline</b> e da <b>Quantidade de Spline</b>, pois eles dependem de dados diferentes.

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Visualizar</b> <i>Tons de cinza</i> | A visualização dos pontos como uma imagem em tons de cinza. |
| <b>Entrada de Lista de Pontos</b> <i>Cor</i> | Uma lista de pontos de entrada codificados nos canais RGBA de uma imagem colorida:<br><b>R</b> - Posição X<br><b>G</b> - Posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br> * Parte inteira: Smoothness;<br> * Parte fracionária: Thickness. |
| <b>Entrada de Número de Pontos</b> <i>Inteiro</i> | O número de pontos de entrada. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Visualizar</b> <i>Tons de cinza</i> | A visualização dos pontos como uma imagem em tons de cinza. |
| <b>Lista de pontos</b> <i>Cor</i> | A lista de saída de pontos codificados nos canais RGBA de uma imagem colorida:<br><b>R</b> - Posição X<br><b>G</b> - Posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br> * Parte inteira: Smoothness;<br> * Parte fracionária: Thickness. |
| <b>Número do Ponto</b> <i>Inteiro</i> | O número de pontos de saída. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Número do Ponto</b> <i>Inteiro</i> | O número de pontos gerados. |
| <b>Ajuste de Smoothness Global</b> <i>Flutuante</i> | Aplica um deslocamento uniforme ao valor de smoothness de todos os pontos.<br>O valor do smoothness resultante é fixado ao intervalo [0;1]. |
| <b>Propriedades de Pontos</b> |  |
| <b>p# Propriedades</b> <i>Flutuante3</i> | Define as propriedades do ponto p#.<br>*- Height:* Ajusta o height do ponto onde um valor mais baixo significa um local mais baixo ou mais profundo;<br>*- Smoothness:* Desloca o início da suavização da spline em p#, onde um valor de 0 resulta em uma trajetória rígida e 1 em uma totalmente suave;<br>*- Thickness:* Ajusta o thickness da spline em p#. O thickness é usado por nós Spline específicos. |
| <b>Coordenadas de pontos</b> |  |
| <b>p#</b> <i>Flutuante2</i> | Define a posição do ponto p# no espaço de textura. |
| <b>Visualizar</b> |  |
| <b>Mostrar rótulos</b> <i>Booleano</i> | Para cada ponto, exibe o nome do ponto ao lado dele na saída “Visualização”. |
| <b>Tamanho do Rótulo</b> <i>Precisão decimal</i> (Disponível quando &#39;Mostrar Rótulos&#39; estiver definido como &#39;Verdadeiro&#39;) | O tamanho do rótulo para cada ponto no espaço de textura, onde 0,1 é um décimo da largura da textura. |
| <b>Mostrar pontos</b> <i>Booleano</i> | Exibe os pontos na saída &#39;Preview&#39;. |
| <b>Tamanho de pontos</b> <i>Flutuante</i> (Disponível quando &#39;Mostrar Pontos&#39; estiver definido como &#39;Verdadeiro&#39;) | O raio dos pontos no espaço de textura, onde 0,1 é um décimo da largura da textura. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 1](point-list.resources/PointList-Variant1.jpg "Exemplo de nó 1")

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](point-list.resources/PointList-Demo1.gif "Exemplo de nó 2")

</td>
</tr>
</table>
