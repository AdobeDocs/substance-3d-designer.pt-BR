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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---


# Acrescentar Spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](../../../../../../assets/spline-append-icon.png "Ícone de nó")

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

## Conectores de entrada

<b>Visualizar #1</b> *Tons de cinza* A visualização do primeiro conjunto de splines de entrada como uma imagem em tons de cinza.

<b>Spline #1 Coords</b> *Cor* As coordenadas do primeiro conjunto de pontos de splines de entrada codificadas nos canais RGBA de uma imagem colorida.\
<b>R</b> - Posição X\
<b>G</b> - posição Y\
<b>B</b> - Height\
<b>A</b> - Dados empacotados:\
* Sinal: Spline é fechado (negativo) ou aberto (positivo);\
* Valor absoluto: Thickness + 1.

<b>Dados de Spline #1</b> *Cor* Dados adicionais do primeiro conjunto de splines de entrada codificados nos canais RGBA de uma imagem colorida.\
<b>R</b> - Tangentes X\
<b>G</b> - Tangentes Y\
<b>B</b> - Não Usado\
<b>A</b> - Não Usado

<b>Valor de Spline #1</b> *Inteiro* O número de splines de entrada no primeiro conjunto.

<b>Visualizar #2</b> *Tons de cinza* A visualização do segundo conjunto de splines de entrada como uma imagem em tons de cinza.

<b>Spline #2 Coords</b> *Cor* As coordenadas do segundo conjunto de pontos de splines de entrada codificadas nos canais RGBA de uma imagem colorida.\
<b>R</b> - Posição X\
<b>G</b> - posição Y\
<b>B</b> - Height\
<b>A</b> - Dados empacotados:\
* Sinal: Spline é fechado (negativo) ou aberto (positivo);\
* Valor absoluto: Thickness + 1.

<b>Dados de Spline #2</b> *Cor* Dados adicionais do segundo conjunto de splines de entrada codificados nos canais RGBA de uma imagem colorida.\
<b>R</b> - Tangentes X\
<b>G</b> - Tangentes Y\
<b>B</b> - Não Usado\
<b>A</b> - Não Usado

<b>Valor de Spline #2</b> *Inteiro* O número de splines de entrada no segundo conjunto.

## Conectores de saída

<b>Visualizar</b> *Tons de cinza* A visualização das linhas divisórias de saída como uma imagem em tons de cinza.

<b>Cordas de spline</b> *Cor* As coordenadas dos pontos das linhas divisórias de saída codificadas nos canais RGBA de uma imagem colorida.\
<b>R</b> - Posição X\
<b>G</b> - posição Y\
<b>B</b> - Height\
<b>A</b> - Dados empacotados:\
* Sinal: Spline é fechado (negativo) ou aberto (positivo);\
* Valor absoluto: Thickness + 1.

<b>Dados de Spline</b> *Cor* Dados adicionais das splines de saída codificados nos canais RGBA de uma imagem colorida.\
<b>R</b> - Tangentes X\
<b>G</b> - Tangentes Y\
<b>B</b> - Não Usado\
<b>A</b> - Não Usado

<b>Valor da spline</b> *Inteiro* O número de splines de saída.

## Parâmetros

<b>Inverter spline #1 Direção </b>*Booleano* Inverte a direção das splines no primeiro conjunto.

<b>Inverter spline #2 Direção </b>*Booleano* Inverte a direção das splines no segundo conjunto.

+++Visualização
<b>Valor de Segmentos</b> *Inteiro* Ajusta o número de segmentos usados para desenhar a visualização de spline na saída da Visualização.\
Um valor mais alto resulta em uma linha mais suave.

<b>Mostrar Auxiliar de Direção</b> *Booleano* Exibe um ponto no início da spline e uma ponta de seta no final da saída de Visualização.

<b>Mostrar Envelope de Thickness</b> *Booleano*\
Exibe linhas adicionais nas bordas do thickness da spline.

<b>Thickness (px)</b> *Flutuante* Ajusta o thickness da visualização da spline em pixels na saída da Visualização.

+++

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 1](../../../../../../assets/SplineAppend-Demo.jpg "Exemplo de nó 1")

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](../../../../../../assets/SplineAppend-Graph.jpg "Exemplo de nó 2")

</td>
</tr>
</table>

![Demonstração de nó](../../../../../../assets/SplineAppend-Demo2.gif "Demonstração de nó")
