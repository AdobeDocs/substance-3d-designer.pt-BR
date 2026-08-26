---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-2-splines.html"
breadcrumb-title: ''
description: Use o nó Ponte de spline para fazer a ponte de texturas entre duas splines para criar conexões perfeitas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge (2 Splines)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ponte Spline (2 Splines)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1247'
ht-degree: 0%

---


# Ponte Spline (2 Splines)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](../../../../../../assets/spline-bridge-2splines-icon.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera splines de <b>Spline #1</b> para <b>Spline #2</b> ao longo dessas splines. As splines geradas podem ser lineares (retas) ou bézier cúbico (curvas).

</td>
</tr>
</table>

>[!IMPORTANT]
>
> Se os dados fornecidos para as entradas <b>Spline #1</b> e <b>Spline #2</b> contiverem mais de uma spline, somente a última spline em cada lista será usada.

## Conectores de entrada

<b>Visualizar #1</b> *Tons de cinza* A visualização das linhas de entrada #1 como uma imagem em tons de cinza.

<b>Palavras de Spline #1</b> *Cor* As coordenadas dos pontos de splines de entrada #1 codificados nos canais RGBA de uma imagem colorida.\
<b>R</b> - Posição X\
<b>G</b> - posição Y\
<b>B</b> - Height\
<b>A</b> - Dados empacotados:\
* Sinal: Spline é fechado (negativo) ou aberto (positivo);\
* Valor absoluto: Thickness + 1.

<b>Dados de Spline #1</b> *Cor* Dados adicionais das splines de entrada #1 codificados nos canais RGBA de uma imagem colorida.\
<b>R</b> - Tangentes X\
<b>G</b> - Tangentes Y\
<b>B</b> - Não Usado\
<b>A</b> - Não Usado

<b>Valor da spline #1</b> *Inteiro* O número de splines de entrada #1.

<b>Visualizar #2</b> *Tons de cinza* A visualização das linhas de entrada #2 como uma imagem em tons de cinza.

<b>Palavras de Spline #2</b> *Cor* As coordenadas das linhas divisórias de entrada #2 pontos codificados nos canais RGBA de uma imagem colorida.\
<b>R</b> - Posição X\
<b>G</b> - posição Y\
<b>B</b> - Height\
<b>A</b> - Dados empacotados:\
* Sinal: Spline é fechado (negativo) ou aberto (positivo);\
* Valor absoluto: Thickness + 1.

<b>Dados de Spline #2</b> *Cor* Dados adicionais das splines de entrada #2 codificados nos canais RGBA de uma imagem colorida.\
<b>R</b> - Tangentes X\
<b>G</b> - Tangentes Y\
<b>B</b> - Não Usado\
<b>A</b> - Não Usado

<b>Valor da spline #2</b> *Inteiro* O número de splines de entrada #2.

<b>Iniciar Curva de Comprimento Tangente</b> *Tons de cinza* (Disponível quando “Tipo de Splines da Ponte” estiver definido como “Bézier Cúbico”)A imagem que descreve uma curva usando os valores da primeira linha de pixels.\
Essa entrada é usada para controlar o comprimento das tangentes “out” para o ponto inicial de cada spline gerada ao longo da spline #1.\
Você pode usar um nó de curva para criar a curva.

<b>Iniciar curva de rotação tangente</b> *Tons de cinza* (Disponível quando “Tipo de Splines da Ponte” estiver definido como “Bézier Cúbico”)A imagem que descreve uma curva usando os valores da primeira linha de pixels.\
Essa entrada é usada para controlar a rotação das tangentes de saída para o ponto inicial de cada spline gerada ao longo da spline #1.\
O valor em tons de cinza da imagem representa um número de voltas.\
Você pode usar um nó de curva para criar a curva.

<b>Curva de comprimento tangente final</b> *Tons de cinza* (Disponível quando “Tipo de Splines da Ponte” estiver definido como “Bézier Cúbico”)A imagem que descreve uma curva usando os valores da primeira linha de pixels.\
Essa entrada é usada para controlar o comprimento das tangentes “in” para o ponto final de cada spline gerada ao longo da spline #2.\
Você pode usar um nó de curva para criar a curva.

<b>Curva de rotação tangente final</b> *Tons de cinza* (Disponível quando “Tipo de Splines da Ponte” estiver definido como “Bézier Cúbico”)A imagem que descreve uma curva usando os valores da primeira linha de pixels.\
Essa entrada é usada para controlar a rotação das tangentes “in” para o ponto final de cada spline gerada ao longo da spline #2.\
O valor em tons de cinza da imagem representa um número de voltas.\
Você pode usar um nó de curva para criar a curva.

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

<b>Quantidade de Splines da Ponte</b> *Inteiro* O número de splines gerados ao longo do Spline #1 até o Spline #2.

<b>Tipo de Splines de Ponte</b> *Inteiro* O tipo de spline gerado:
* Linear: uma linha reta do Início ao Fim;
* Bezier cúbico: uma spline curva do início ao fim, sendo a curva controlada pelo comprimento e ângulo dos pontos inicial e final.

<b>Iniciar Spline #1</b> *Flutuante* Desloca o local ao longo da spline #1 de onde as splines são geradas. O valor é o comprimento normalizado do Spline #1.\
Um valor mais alto resulta em um mesmo número de splines compactados com mais precisão.

<b>Iniciar Spline #2</b> *Flutuante* Desloca o local ao longo da spline #2 de onde as splines são geradas. O valor é o comprimento normalizado do Spline #2.\
Um valor mais alto resulta em um mesmo número de splines compactados com mais precisão.

<b>Fim da Spline #1</b> *Flutuante* Desloca o local ao longo da spline #1 até onde as splines são geradas. O valor é o comprimento normalizado do Spline #1.\
Um valor mais baixo resulta em um empacotamento mais preciso do mesmo número de splines.

<b>Fim da Spline #1</b> *Flutuante* Desloca o local ao longo da spline #2 até onde as splines são geradas. O valor é o comprimento normalizado do Spline #2.\
Um valor mais baixo resulta em um empacotamento mais preciso do mesmo número de splines.

<b>Deslocamento da spline #1</b> *Flutuante* Aplica um deslocamento ao ponto inicial de todas as splines ao longo da spline #1. O valor é o comprimento normalizado do Spline #1.\
Os splines que correspondem ao início ou ao fim do spline são deixados lá.

<b>Deslocamento da spline #2</b> *Flutuante* Aplica um deslocamento ao ponto inicial de todas as splines ao longo da spline #2. O valor é o comprimento normalizado do Spline #2.\
Os splines que correspondem ao início ou ao fim do spline são deixados lá.

<b>Início Aleatório do Deslocamento</b> *Flutuante* Aplica um deslocamento aleatório ao ponto inicial de cada spline ao longo da spline #1. O valor é a distância normalizada entre as splines em Spline #1.\
Quando deixados em 0, os splines ficam espaçados igualmente entre os pontos Spline inicial #1 e Spline final #1.

<b>Fim Aleatório do Deslocamento</b> *Flutuante* Aplica um deslocamento aleatório ao ponto final de cada spline ao longo da spline #2. O valor é a distância normalizada entre as splines em Spline #2.\
Quando deixados em 0, os splines ficam espaçados igualmente entre os pontos Spline inicial #2 e Spline final #2.

<b>Início do Comprimento Tangente</b> *Flutuante* (Disponível quando ‘Bridge Splines Type’ estiver definido como ‘Cubic Bezier’)O comprimento da tangente ‘out’ para o ponto inicial na Spline #1 de todas as splines geradas.

<b>Fim do Comprimento Tangente</b> *Flutuante* (Disponível quando ‘Bridge Splines Type’ estiver definido como ‘Cubic Bezier’)O comprimento da tangente ‘in’ para o ponto final na Spline #2 de todas as splines geradas.

<b>Início da Rotação Tangente</b> *Flutuante* (Disponível quando “Tipo de Splines de Ponte” estiver definido como “Bézier Cúbico”)A rotação da tangente “out” para o ponto inicial na Spline #1 de todas as splines geradas.\
O valor é um número de voltas.

<b>Fim da Rotação Tangente</b> *Flutuante* (Disponível quando ‘Bridge Splines Type’ estiver definido como ‘Cubic Bezier’)A rotação da tangente ‘in’ para o ponto final na Spline #2 de todas as splines geradas.\
O valor é um número de voltas.

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

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineBridge-2Splines_Variant1-Before.jpg" alt="SplineBridge-2Splines_Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineBridge-2Splines_Variant1-After.jpg" alt="SplineBridge-2Splines_Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](../../../../../../assets/SplineBridge-2Splines_Demo.gif "Exemplo de nó 2")

</td>
</tr>
</table>
