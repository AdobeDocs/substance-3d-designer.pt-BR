---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-quadratic.html"
breadcrumb-title: ''
description: Use o nó Quadrático de spline para criar splines quadráticos suaves com três pontos de controle.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Quadratic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline (quadrática)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '824'
ht-degree: 0%

---


# Spline (quadrática)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Spline (Quadrático): ícone](spline-quadratic.resources/spline-quadratic-01.png "Spline (Quadrático): ícone")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma única spline entre dois pontos <b>p1</b> e <b>p3</b> em locais arbitrários.

A trajetória da spline é controlada pela tangente “out” de <b>p1</b> e pela tangente “in” de <b>p3</b>, *ambos* controlados por um único ponto <b>p3</b>.

A extensão do arco formado pela spline é *ajustável*, de modo que parte de sua trajetória a partir de suas extremidades pode permanecer reta.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Visualizar</b> <i>Tons de cinza</i> | A visualização das linhas de entrada como uma imagem em tons de cinza. |
| <b>Cordas de spline</b> <i>Cor</i> | As coordenadas dos pontos das linhas divisórias de entrada codificadas nos canais RGBA de uma imagem colorida:<br><b>R</b> - posição X<br><b>G</b> - posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br> - Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br> - Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> <i>Cor</i> | Dados adicionais das linhas de entrada codificadas nos canais RGBA de uma imagem colorida:<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Tangentes Z<br><b>A</b> - Não Usados |
| <b>Valor da spline</b> <i>Inteiro</i> | O número de splines de entrada. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Visualizar</b> <i>Tons de cinza</i> | A visualização das linhas de saída como uma imagem em tons de cinza. |
| <b>Cordas de spline</b> <i>Cor</i> | As coordenadas dos pontos das linhas divisórias de saída codificadas nos canais RGBA de uma imagem colorida:<br><b>R</b> - posição X<br><b>G</b> - posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br> - Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br> - Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> <i>Cor</i> | Dados adicionais das splines de saída codificadas nos canais RGBA de uma imagem colorida:<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Tangentes Z<br><b>A</b> - Não Usados |
| <b>Valor da spline</b> <i>Inteiro</i> | O número de splines de saída. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Inverter direção</b> <i>Booleano</i> | Inverte a direção da spline. |
| <b>Distribuição uniforme</b> <i>Booleano</i> | Quando <i>Verdadeiro</i>, os pontos da spline ficam com espaçamento uniforme do início ao fim. |
| <b>Acrescentar spline de entrada</b> <i>Booleano</i> | Adiciona a spline gerada ao final da lista de splines conectadas às entradas de <b>spline</b>. |
| <b>Correção não quadrada</b> <i>Booleano</i> | Ajuste a posição e o thickness dos pontos para manter a forma de spline em resoluções não quadradas. Isso também afeta a distribuição uniforme. |
| <b>Smoothness</b> <i>Flutuante</i> | Ajusta a <i>extensão do arco</i> formado pela spline, onde 1 significa que o comprimento total da spline está arqueado e 0 significa que a spline está totalmente reta. O arco progride do ponto <b>p3</b> ao longo da spline até suas extremidades. |
| <b>Height</b> |  |
| <b>Iniciar height</b> <i>Flutuante</i> | Ajusta o height do ponto <b>p1</b> onde um valor mais baixo significa um local mais baixo ou mais profundo.<br>Isso afeta o height da spline em <b>p1</b>. |
| <b>Encerrar height</b> <i>Flutuante</i> | Ajusta o height do ponto <b>p3</b> onde um valor mais baixo significa um local mais baixo ou mais profundo.<br>Isso afeta o thickness da spline em <b>p3</b>. |
| <b>height de tangente automática</b> <i>Booleano</i> | Ajusta o height do ponto <b>p3</b> onde um valor mais baixo significa um local mais baixo ou mais profundo.<br>Isso afeta o thickness da spline em <b>p3</b>. |
| <b>height Tangente</b> <i>Flutuante</i> | Ajusta o height orientado pelas tangentes controladas pelo ponto <b>p2</b>.<br>Isso afeta o height ao longo da spline, pois afasta-se de <b>p1</b> e vai para <b>p3</b>.<br><i>Observação:</i> este parâmetro só está disponível quando o <b>height tangente automático</b> está definido como &#39;Falso&#39;. |
| <b>Thickness</b> |  |
| <b>Iniciar thickness</b> <i>Flutuante</i> | Ajusta o thickness do ponto <b>p1</b>. Isso afeta o thickness da spline em <b>p1</b>.<br><i>Observação: o Thickness </i> é usado por nós de spline específicos. |
| <b>Encerrar thickness</b> <i>Flutuante</i> | Ajusta o thickness do ponto <b>p3</b>. Isso afeta o thickness da spline em <b>p3</b>.<br><i>Observação: o Thickness </i> é usado por nós de spline específicos. |
| <b>thickness de tangente automática</b> <i>Booleano</i> | Define automaticamente o thickness das tangentes da spline para interpolar linearmente do <b>Thickness Inicial</b> para o <b>Thickness Final</b>.<br><i>Observação: o Thickness </i> é usado por nós de spline específicos. |
| <b>thickness Tangente</b> <i>Flutuante</i> | Ajusta o thickness orientado pelas tangentes controladas pelo ponto <b>p2</b>.<br>Isso afeta o thickness ao longo da spline, pois afasta-se de <b>p1</b> e vai para <b>p3</b>.<br><i>Observação: o Thickness </i> é usado por nós de spline específicos.<br><i>Observação 2:</i> este parâmetro só está disponível quando o <b>thickness de tangente automática</b> está definido como &#39;False&#39;. |
| <b>Coordenadas de pontos</b> |  |
| <b>p1</b> <i>Flutuante2</i> | Define a posição do ponto <b>p1</b> no espaço de textura. |
| <b>p2</b> <i>Flutuante2</i> | Define a posição do ponto <b>p2</b> no espaço de textura.<br>O ponto <b>p2</b> controla as <i>tangentes</i> dos pontos <b>p1</b> e <b>p3</b>. |
| <b>p3</b> <i>Flutuante2</i> | Define a posição do ponto <b>p3</b> no espaço de textura. |
| <b>Visualizar</b> |  |
| <b>Mostrar tangentes</b> <i>Booleano</i> | Exibe a tangente <b>p1</b> point &#39;out&#39; e a tangente <b>p3</b> point &#39;in&#39; na saída <b>Visualizar</b>. Inverte a direção da spline. |
| <b>Mostrar auxiliar de direção</b> <i>Booleano</i> | Exibe um ponto no início da spline e uma ponta de seta no final da saída de <b>Visualização</b>. |
| <b>Mostrar envelope do thickness</b> <i>Booleano</i> | Exibe linhas adicionais nas bordas do thickness da spline. |
| <b>Valor dos segmentos</b> <i>Inteiro</i> | Ajusta o número de segmentos usados para desenhar a visualização de spline na saída de <b>Visualização</b>.<br>Um valor mais alto resulta em uma linha mais suave. |
| <b>Thickness (px)</b> <i>Flutuante</i> | Ajusta o thickness em pixels da visualização de spline na saída de <b>Visualização</b>. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (Quadrático): Exemplo 1](spline-quadratic.resources/spline-quadratic-02.png "Spline (Quadrático): Exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Spline (Quadrático): Exemplo 2](spline-quadratic.resources/spline-quadratic-03.png "Spline (Quadrático): Exemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (Quadrática): Demonstração](spline-quadratic.resources/spline-quadratic-04.gif "Spline (Quadrática): Demonstração"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
