---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-cubic.html"
breadcrumb-title: ''
description: Use o nó Cúbico de spline para criar splines cúbicas suaves com quatro pontos de controle para caminhos curvos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Cubic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline (cúbico)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---


# Spline (cúbico)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](spline-cubic.resources/spline-cubic-01.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma única spline entre dois pontos <b>p1 </b>e <b>p2</b> em locais arbitrários.

A trajetória da spline é controlada pela tangente “out” de <b>p1</b> e pela tangente “in” de <b>p2</b>.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Visualizar</b> <i>Tons de cinza</i> | A visualização das linhas de entrada como uma imagem em tons de cinza. |
| <b>Cordas de spline</b> <i>Cor</i> | As coordenadas dos pontos das linhas divisórias de entrada codificadas nos canais RGBA de uma imagem colorida:<br><b>R</b> - Posição X<br><b>G</b> - Posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br>- Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> <i>Cor</i> | Dados adicionais das splines de entrada codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usadas<br><b>A</b> - Não Usadas |
| <b>Valor da spline</b> <i>Inteiro</i> | O número de splines de entrada. |

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
| <b>Inverter Direção</b> <i>Booleano</i> | Inverte a direção da spline. |
| <b>Acrescentar Spline de Entrada</b> <i>Booleano</i> | Adiciona a spline gerada ao final da lista de splines conectadas às entradas de <b>spline</b>. |
| <b>Correção Não Quadrada</b> <i>Booleano</i> | Ajuste as posições e o thickness dos pontos para manter a forma de spline em resoluções não quadradas. Isso também afeta a distribuição uniforme. |
| <b>Height</b> |  |
| <b>Iniciar Height</b> <i>Flutuante</i> | Ajusta o height do ponto p1 onde um valor mais baixo significa um local mais baixo ou mais profundo. Isso afeta o height da spline em p1. |
| <b>Encerrar Height</b> <i>Precisão decimal</i> | Ajusta o height do ponto p2 onde um valor mais baixo significa um local mais baixo ou mais profundo. Isso afeta o thickness da spline em p2. |
| <b>Height Tangente Automático</b> <i>Booleano</i> | Define automaticamente o height das tangentes de spline para interpolar linearmente do Height inicial ao Height final. |
| <b>Height de Tangente p1</b> <i>Precisão decimal</i> (disponível quando &#39;Auto Tangent Height&#39; é True) | Ajusta o height da tangente “out” do ponto p1, onde um valor mais baixo significa um local mais baixo ou mais profundo. Isso afeta o height ao longo da spline à medida que se afasta do p1. |
| <b>Height de Tangente p2</b> <i>Precisão decimal</i> (disponível quando &#39;Auto Tangent Height&#39; é True) | Ajusta o height da tangente “in” do ponto p2, onde um valor mais baixo significa um local mais baixo ou mais profundo. Isso afeta o height ao longo da spline à medida que se afasta do p2. |
| <b>Thickness</b> |  |
| <b>Iniciar Thickness</b> <i>Flutuante</i> | Ajusta o thickness do ponto p1. Isso afeta o thickness da spline em p1.<br>Observação: o Thickness é usado por nós de spline específicos. |
| <b>Encerrar Thickness</b> <i>Flutuante</i> | Ajusta o thickness do ponto p2. Isso afeta o thickness da spline em p2.<br>Observação: o Thickness é usado por nós de spline específicos. |
| <b>Thickness Tangente Automático</b> <i>Booleano</i> | Define automaticamente o thickness das tangentes da spline para interpolar linearmente do Thickness inicial ao Thickness final.<br>Observação: o Thickness é usado por nós de spline específicos. |
| <b>Thickness de Tangente p1</b> <i>Precisão decimal</i> (disponível quando &#39;Auto Tangent Thickness&#39; é True) | Ajusta o thickness da tangente “out” do ponto p1. Isso afeta o thickness ao longo da spline à medida que se afasta do p1.<br>Observação: o Thickness é usado por nós de spline específicos. |
| <b>Thickness de Tangente p2</b> <i>Precisão decimal</i> (disponível quando &#39;Auto Tangent Thickness&#39; é True) | Ajusta o thickness da tangente “in” do ponto p2. Isso afeta o thickness ao longo da spline à medida que se afasta do p2.<br>Observação: o Thickness é usado por nós de spline específicos. |
| <b>Coordenadas de pontos</b> |  |
| <b>p1</b> <i>Flutuante2</i> | Define a posição do ponto p1 no espaço de textura. |
| <b>p1 Tangente</b> <i>Flutuante2</i> | Define a posição da alça tangente p1 point &#39;out&#39; no espaço de textura. |
| <b>p2</b> <i>Flutuante2</i> | Define a posição do ponto p2 no espaço de textura. |
| <b>Tangente p2</b> <i>Flutuante2</i> | Define a posição da alça tangente “in” do ponto p2 no espaço de textura. |
| <b>Visualizar</b> |  |
| <b>Mostrar Tangentes</b> <i>Booleano</i> | Exibe a tangente &#39;out&#39; de ponto p1 e a tangente &#39;in&#39; de ponto p2 na saída da Visualização. |
| <b>Mostrar Auxiliar de Direção</b> <i>Booleano</i> | Exibe um ponto no início da spline e uma ponta de seta no final da saída de Visualização. |
| <b>Valor de Segmentos</b> <i>Inteiro</i> | Ajusta o número de segmentos usados para desenhar a visualização de spline na saída da Visualização. Um valor mais alto resulta em uma linha mais suave. |
| <b>Thickness (px)</b> <i>Flutuante</i> | Ajusta o thickness em pixels da visualização de spline na saída da Visualização. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 1](spline-cubic.resources/spline-cubic-02.jpg "Exemplo de nó 1")

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](spline-cubic.resources/spline-cubic-03.jpg "Exemplo de nó 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 3](spline-cubic.resources/spline-cubic-04.gif "Exemplo de nó 3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
