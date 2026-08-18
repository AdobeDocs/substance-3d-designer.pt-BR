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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# Lista de pontos

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](../../../../../../assets/point-list-icon.png "Ícone de nó")

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

## Conectores de entrada

<b>Visualização </b>*Tons de cinza* A visualização dos pontos como uma imagem em tons de cinza.

<b>Entrada de Lista de Pontos</b> *Cor*\
Uma lista de pontos de entrada codificados nos canais RGBA de uma imagem colorida:\
    <b>R</b> - Posição X\
    <b>G</b> - posição Y\
    <b>B</b> - Height\
    <b>A</b> - Dados empacotados:\
            * Parte inteira: Smoothness;\
            * Parte fracionária: Thickness.

<b>Entrada de Número de Pontos</b> *Inteiro*\
O número de pontos de entrada.

## Conectores de saída

<b>Visualização </b>*Tons de cinza* A visualização dos pontos como uma imagem em tons de cinza.

<b>Cor </b>*da Lista de Pontos*\
A lista de saída de pontos codificados nos canais RGBA de uma imagem colorida:\
    <b>R</b> - Posição X\
    <b>G</b> - posição Y\
    <b>B</b> - Height\
    <b>A</b> - Dados empacotados:\
            * Parte inteira: Smoothness;\
            * Parte fracionária: Thickness.

<b>Número de Ponto </b>*Inteiro*\
O número de pontos de saída.

## Parâmetros

<b>Número do Ponto</b> *Inteiro* O número de pontos gerados.

<b>Ajuste de Smoothness Global</b> *Flutuante* Aplica um deslocamento uniforme ao valor de smoothness de todos os pontos.\
O valor do smoothness resultante é fixado no intervalo [0;1].

+++Propriedades de Pontos
<b>p# Propriedades</b> *Flutuante3* Define as propriedades do ponto p#.\
*- Height:* Ajusta o height do ponto onde um valor mais baixo significa um local mais baixo ou mais profundo;\
*- Smoothness:* Desloca o início da suavização da spline em p#, onde um valor de 0 resulta em uma trajetória rígida e 1 em uma totalmente suave;\
*- Thickness:* Ajusta o thickness da spline em p#. O thickness é usado por nós Spline específicos.

+++

+++Coordenadas de pontos
<b>p#</b> *Flutuante2* Define a posição do ponto p# no espaço de textura.

+++

+++Visualização
<b>Mostrar Rótulos</b> *Booleanos*\
Para cada ponto, exibe o nome do ponto ao lado dele na saída “Visualização”.

<b>Tamanho do Rótulo</b> *Flutuante* (Disponível quando &#39;Mostrar Rótulos&#39; estiver definido como &#39;Verdadeiro&#39;)\
O tamanho do rótulo para cada ponto no espaço de textura, onde 0,1 é um décimo da largura da textura.

<b>Mostrar pontos</b> *Booleano*\
Exibe os pontos na saída &#39;Preview&#39;.

<b>Tamanho dos Pontos</b> *Flutuante* (Disponível quando &#39;Mostrar Pontos&#39; estiver definido como &#39;Verdadeiro&#39;)\
O raio dos pontos no espaço de textura, onde 0,1 é um décimo da largura da textura.

+++

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 1](../../../../../../assets/PointList-Variant1.jpg "Exemplo de nó 1")

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](../../../../../../assets/PointList-Demo1.gif "Exemplo de nó 2")

</td>
</tr>
</table>
