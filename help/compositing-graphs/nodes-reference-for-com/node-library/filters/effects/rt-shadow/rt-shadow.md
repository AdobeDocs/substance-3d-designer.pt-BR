---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-shadow.html"
breadcrumb-title: ''
description: Use o nó Sombras RT para calcular informações de sombra em tempo real a partir da geometria para criar efeitos de iluminação dinâmicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Shadows
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sombras RT
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---


# Sombras RT

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![Ícone do nó Sombras RT](../../../../../../assets/rt-shadow.png "Ícone do nó Sombras RT")

<b>Entrada:</b> *Filtros/Efeitos*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrição

Gera sombras traçadas de raio a partir de uma entrada de mapa de height.

Este nó não deve ser usado em combinação com o mecanismo da CPU (SSE) devido ao tempo de computação.

</td>
</tr>
</table>

## Parâmetros

<b>Amostras</b> *Inteiro*\
O número de raios usados para calcular as sombras.\
Um valor mais alto fornece um resultado mais suave e preciso, ao custo do desempenho.

<b>Modo</b> *Inteiro*\
O método de desenhar as sombras na superfície.

<b>Escala de Height</b> *Flutuante*\
Um multiplicador para a intensidade do mapa de height de entrada.

<b>Posição da Luz </b>*Flutuante2*\
Posição da fonte luminosa numa esfera que envolve a superfície:
* <b>X</b>: posição horizontal, em número de voltas;
* <b>Y</b>: posição vertical, onde 0,5 é o zênite e 0/1 é o horizonte.

<b>Intensidade da luz</b> *Flutuante*\
A intensidade da fonte de luz.

<b>Tamanho Claro</b> *Flutuante2* (Disponível quando o <b>Modo</b> está definido como *Sombreado*)\
O tamanho da fonte de luz como um retângulo.

<b>Escala Clara (Sombras Suaves)</b> *Flutuante*\
Um multiplicador para a contribuição do <b>Tamanho da Luz</b> para a direção dos raios.\
Um valor mais alto resulta em sombras mais suaves.

<b>Manter a luz acima do horizonte</b> *Booleano*\
Se a <b>Posição da Luz</b> estiver definida de forma a colocar a luz abaixo do horizonte, este parâmetro impedirá que a luz ultrapasse esse limite, o que significa que os valores de Y estão fixados no intervalo [0;1].

<b>Opacidade da sombra</b> *Flutuante*\
Um multiplicador da opacidade de sombras desenhadas na superfície.

<b>Atenuação de Sombra</b> *Flutuante*\
Um multiplicador para a atenuação das sombras quanto mais distantes estão de seu rebocador.\
Um valor de 0 resulta em sombras uniformes (as sombras suaves ainda são aplicadas).

<b>Comprimento Máximo de Sombras</b> *Flutuante*\
A distância máxima que uma sombra pode ser desenhada de seu rodízio.\
Um valor de 0 resulta em sombras não visíveis.

## Imagens de exemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Nó Sombras de ![RT - Exemplo 1](../../../../../../assets/RTShadows-01.jpg "Nó Sombras de RT - Exemplo 1")

</td>
<td style="border: 0;" valign="top">

Nó Sombras de ![RT - Exemplo 2](../../../../../../assets/RTShadows-02.jpg "Nó Sombras de RT - Exemplo 2")

</td>
<td style="border: 0;" valign="top">

Nó Sombras de ![RT - Exemplo 3](../../../../../../assets/RTShadows-03.jpg "Nó Sombras de RT - Exemplo 3")

</td>
</tr>
</table>
