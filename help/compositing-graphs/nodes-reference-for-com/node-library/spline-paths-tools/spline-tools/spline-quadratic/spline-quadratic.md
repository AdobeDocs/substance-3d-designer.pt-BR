---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-quadratic.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---


# Spline (quadrática)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Spline (Quadrático): ícone](../../../../../../assets/spline-quadratic-icon.png "Spline (Quadrático): ícone")

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

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Visualizar</b> *Tons de cinza* | A visualização das linhas de entrada como uma imagem em tons de cinza. |
| <b>Cordas de spline</b> *Cor* | As coordenadas dos pontos das splines de entrada codificadas nos canais RGBA de uma imagem colorida: <b>R</b> - posição X <b>G</b> - posição Y <b>B</b> - Height <b>A</b> - Dados empacotados: - Sinal: a spline está fechada (negativa) ou aberta (positiva); - Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> *Cor* | Dados adicionais das splines de entrada codificadas nos canais RGBA de uma imagem colorida: <b>R</b> - Tangentes X <b>G</b> - Tangentes Y <b>B</b> - Tangentes Z <b>A</b> - Não Usados |
| <b>Valor da spline</b> *Inteiro* | O número de splines de entrada. |

## Conectores de saída

|  |  |
| --- | --- |
| <b>Visualizar</b> *Tons de cinza* | A visualização das linhas de saída como uma imagem em tons de cinza. |
| <b>Cordas de spline</b> *Cor* | As coordenadas dos pontos das linhas divisórias de saída codificadas nos canais RGBA de uma imagem colorida: <b>R</b> - posição X <b>G</b> - posição Y <b>B</b> - Height <b>A</b> - Dados empacotados: - Sinal: a linha divisória está fechada (negativa) ou aberta (positiva); - Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> *Cor* | Dados adicionais das splines de saída codificadas nos canais RGBA de uma imagem colorida: <b>R</b> - Tangentes X <b>G</b> - Tangentes Y <b>B</b> - Tangentes Z <b>A</b> - Não Usados |
| <b>Valor da spline</b> *Inteiro* | O número de splines de saída. |

## Parâmetros

|  |  |
| --- | --- |
| <b>Inverter direção</b> *Booleano* | Inverte a direção da spline. |
| <b>Distribuição uniforme</b> *Booleano* | Quando *Verdadeiro*, os pontos da spline ficam com espaçamento uniforme do início ao fim. |
| <b>Acrescentar spline de entrada</b> *Booleano* | Adiciona a spline gerada ao final da lista de splines conectadas às entradas de <b>spline</b>. |
| <b>Correção não quadrada</b> *Booleano* | Ajuste a posição e o thickness dos pontos para manter a forma de spline em resoluções não quadradas. Isso também afeta a distribuição uniforme. |
| <b>Smoothness</b> *Flutuante* | Ajusta a *extensão do arco* formado pela spline, onde 1 significa que o comprimento total da spline está arqueado e 0 significa que a spline está totalmente reta. O arco progride do ponto <b>p3</b> ao longo da spline até suas extremidades. |

+++Altura

|  |  |
| --- | --- |
| <b>Iniciar height</b> *Flutuante* | Ajusta o height do ponto <b>p1</b> onde um valor mais baixo significa um local mais baixo ou mais profundo.  Isso afeta o height da spline em <b>p1</b>. |
| <b>Encerrar height</b> *Flutuante* | Ajusta o height do ponto <b>p3</b> onde um valor mais baixo significa um local mais baixo ou mais profundo.  Isso afeta o thickness da spline em <b>p3</b>. |
| <b>height de tangente automática</b> *Booleano* | Ajusta o height do ponto <b>p3</b> onde um valor mais baixo significa um local mais baixo ou mais profundo.  Isso afeta o thickness da spline em <b>p3</b>. |
| <b>height Tangente</b> *Flutuante* | Ajusta o height orientado pelas tangentes controladas pelo ponto <b>p2</b>.  Isso afeta o height ao longo da spline à medida que ele se afasta de <b>p1</b> e vai para <b>p3</b>.   *Observação:* este parâmetro só está disponível quando o <b>height de tangente automática</b> está definido como &#39;False&#39;. |


+++

+++Espessura

|  |  |
| --- | --- |
| <b>Iniciar thickness</b> *Flutuante* | Ajusta o thickness do ponto <b>p1</b>. Isso afeta o thickness da spline em <b>p1</b>.   *Observação: o Thickness* é usado por nós Spline específicos. |
| <b>Encerrar thickness</b> *Flutuante* | Ajusta o thickness do ponto <b>p3</b>. Isso afeta o thickness da spline em <b>p3</b>.   *Observação: o Thickness* é usado por nós Spline específicos. |
| <b>thickness de tangente automática</b> *Booleano* | Define automaticamente o thickness das tangentes da spline para interpolar linearmente do <b>Thickness inicial</b> para o <b>Thickness final</b>.   *Observação: o Thickness* é usado por nós Spline específicos. |
| <b>thickness Tangente</b> *Flutuante* | Ajusta o thickness orientado pelas tangentes controladas pelo ponto <b>p2</b>.  Isso afeta o thickness ao longo da spline à medida que ele se afasta de <b>p1</b> e vai para <b>p3</b>.   *Observação: o Thickness* é usado por nós Spline específicos.  *Observação 2:* este parâmetro só está disponível quando o <b>thickness de tangente automática</b> está definido como &#39;False&#39;. |


+++

+++Coordenadas de pontos

|  |  |
| --- | --- |
| <b>p1</b> *Flutuante2* | Define a posição do ponto <b>p1</b> no espaço de textura. |
| <b>p2</b> *Flutuante2* | Define a posição do ponto <b>p2</b> no espaço de textura.  O ponto <b>p2</b> controla as *tangentes* dos pontos <b>p1</b> e <b>p3</b>. |
| <b>p3</b> *Flutuante2* | Define a posição do ponto <b>p3</b> no espaço de textura. |


+++

+++Visualização

|  |  |
| --- | --- |
| <b>Mostrar tangentes</b> *Booleano* | Exibe a tangente <b>p1</b> point &#39;out&#39; e a tangente <b>p3</b> point &#39;in&#39; na saída <b>Visualizar</b>. Inverte a direção da spline. |
| <b>Mostrar auxiliar de direção</b> *Booleano* | Exibe um ponto no início da spline e uma ponta de seta no final da saída de <b>Visualização</b>. |
| <b>Mostrar envelope do thickness</b> *Booleano* | Exibe linhas adicionais nas bordas do thickness da spline. |
| <b>Valor dos segmentos</b> *Inteiro* | Ajusta o número de segmentos usados para desenhar a visualização de spline na saída de <b>Visualização</b>.  Um valor mais alto resulta em uma linha mais suave. |
| <b>Thickness (px)</b> *Flutuante* | Ajusta o thickness em pixels da visualização de spline na saída de <b>Visualização</b>. |


+++

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (Quadrático): Exemplo 1](../../../../../../assets/spline-quadratic-example-1.png "Spline (Quadrático): Exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Spline (Quadrático): Exemplo 2](../../../../../../assets/spline-quadratic-example-2.png "Spline (Quadrático): Exemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Spline (Quadrática): Demonstração](../../../../../../assets/spline-quadratic-demo.gif "Spline (Quadrática): Demonstração"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
