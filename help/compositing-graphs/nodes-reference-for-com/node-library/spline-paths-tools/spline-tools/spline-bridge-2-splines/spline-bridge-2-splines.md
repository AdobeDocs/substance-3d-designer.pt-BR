---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-2-splines.html"
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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 0%

---


# Ponte Spline (2 Splines)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](spline-bridge-2-splines.resources/spline-bridge-2splines-icon.png "Ícone de nó")

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

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Visualizar #1</b> <i>Tons de cinza</i> | A visualização da entrada splines #1 como uma imagem em tons de cinza. |
| <b>Palavras de Spline #1</b> <i>Cor</i> | As coordenadas dos pontos das linhas divisórias de entrada #1 codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Posição X<br><b>G</b> - Posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br>- Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Dados de Spline #1</b> <i>Cor</i> | Dados adicionais das splines de entrada #1 codificados nos canais RGBA de uma imagem colorida.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usados<br><b>A</b> - Não Usados |
| <b>Valor da spline #1</b> <i>Inteiro</i> | O número de splines de entrada #1. |
| <b>Visualizar #2</b> <i>Tons de cinza</i> | A visualização da entrada splines #2 como uma imagem em tons de cinza. |
| <b>Palavras de Spline #2</b> <i>Cor</i> | As coordenadas dos pontos #2 das linhas divisórias de entrada codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Posição X<br><b>G</b> - Posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br>- Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Dados de Spline #2</b> <i>Cor</i> | Dados adicionais das splines de entrada #2 codificados nos canais RGBA de uma imagem colorida.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usados<br><b>A</b> - Não Usados |
| <b>Valor da spline #2</b> <i>Inteiro</i> | O número de splines de entrada #2. |
| <b>Iniciar Curva de Comprimento Tangente</b> <i>Tons de cinza</i> (Disponível quando &#39;Tipo de Splines da Ponte&#39; estiver definido como &#39;Bézier Cúbico&#39;) | A imagem que descreve uma curva usando os valores de sua primeira linha de pixels.<br>Esta entrada é usada para controlar o comprimento das tangentes &#39;out&#39; para o ponto inicial de cada spline gerada ao longo da Spline #1.<br>Você pode usar um nó de Curva para criar a curva. |
| <b>Iniciar curva de rotação tangente</b> <i>Tons de cinza</i> (Disponível quando &#39;Tipo de Splines da Ponte&#39; estiver definido como &#39;Bézier Cúbico&#39;) | A imagem que descreve uma curva usando os valores de sua primeira linha de pixels.<br>Esta entrada é usada para controlar a rotação das tangentes &#39;out&#39; para o ponto inicial de cada spline gerada ao longo da spline #1.<br>O valor em tons de cinza da imagem representa um número de voltas.<br>Você pode usar um nó de curva para criar a curva. |
| <b>Curva de comprimento tangente final</b> <i>Tons de cinza</i> (Disponível quando &#39;Tipo de Splines da Ponte&#39; estiver definido como &#39;Bézier Cúbico&#39;) | A imagem que descreve uma curva usando os valores de sua primeira linha de pixels.<br>Esta entrada é usada para controlar o comprimento das tangentes &#39;in&#39; para o ponto final de cada spline gerada ao longo da Spline #2.<br>Você pode usar um nó de Curva para criar a curva. |
| <b>Curva de rotação tangente final</b> <i>Tons de cinza</i> (Disponível quando &#39;Tipo de Splines da Ponte&#39; estiver definido como &#39;Bézier Cúbico&#39;) | A imagem que descreve uma curva usando os valores de sua primeira linha de pixels.<br>Esta entrada é usada para controlar a rotação das tangentes &#39;in&#39; para o ponto final de cada spline gerada ao longo da spline #2.<br>O valor em tons de cinza da imagem representa um número de curvas.<br>Você pode usar um nó de curva para criar a curva. |

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
| <b>Quantidade de Splines da Ponte</b> <i>Inteiro</i> | O número de splines gerados ao longo da spline #1 até a spline #2. |
| <b>Tipo de Splines de Ponte</b> <i>Inteiro</i> | O tipo de spline gerado:<br><br>- Linear: uma spline reta do Início ao Fim;<br>- Bézier Cúbico: uma spline curva do Início ao Fim, sendo a curva controlada pelo comprimento e ângulo dos pontos de Início e Fim. |
| <b>Iniciar Spline #1</b> <i>Flutuante</i> | Desloca o local ao longo da spline #1 de onde as splines são geradas. O valor é o comprimento normalizado da spline #1.<br>Um valor mais alto resulta no mesmo número de splines sendo compactados com mais precisão. |
| <b>Iniciar Spline #2</b> <i>Flutuante</i> | Desloca o local ao longo da spline #2 de onde as splines são geradas. O valor é o comprimento normalizado da spline #2.<br>Um valor mais alto resulta no mesmo número de splines sendo compactados com mais precisão. |
| <b>Fim da Spline #1</b> <i>Flutuante</i> | Desloca o local ao longo da spline #1 para onde as splines são geradas. O valor é o comprimento normalizado da spline #1.<br>Um valor mais baixo resulta no mesmo número de splines sendo compactados com mais precisão. |
| <b>Fim da Spline #1</b> <i>Flutuante</i> | Desloca o local ao longo da spline #2 para onde as splines são geradas. O valor é o comprimento normalizado da spline #2.<br>Um valor mais baixo resulta no mesmo número de splines sendo compactados com mais precisão. |
| <b>Deslocamento da spline #1</b> <i>Flutuante</i> | Aplica um deslocamento ao ponto inicial de todas as splines ao longo da spline #1. O valor é o comprimento normalizado da spline #1.<br>As splines que correspondem ao início ou ao fim da spline são deixadas lá. |
| <b>Deslocamento da spline #2</b> <i>Flutuante</i> | Aplica um deslocamento ao ponto inicial de todas as splines ao longo da spline #2. O valor é o comprimento normalizado da spline #2.<br>As splines que correspondem ao início ou ao fim da spline são deixadas lá. |
| <b>Início Aleatório do Deslocamento</b> <i>Flutuante</i> | Aplica um deslocamento aleatório ao ponto inicial de cada spline ao longo da spline #1. O valor é a distância normalizada entre as splines no Spline #1.<br>Quando deixadas em 0, as splines ficam espaçadas igualmente entre os pontos de Spline inicial #1 e Spline final #1. |
| <b>Fim Aleatório do Deslocamento</b> <i>Flutuante</i> | Aplica um deslocamento aleatório ao ponto final de cada spline ao longo da spline #2. O valor é a distância normalizada entre as splines no Spline #2.<br>Quando deixadas em 0, as splines ficam espaçadas igualmente entre os pontos de Spline inicial #2 e Spline final #2. |
| <b>Início do Comprimento Tangente</b> <i>Precisão decimal</i> (Disponível quando &#39;Tipo de Splines da Ponte&#39; estiver definido como &#39;Bézier Cúbico&#39;) | O comprimento da tangente “out” do ponto inicial na spline #1 de todas as splines geradas. |
| <b>Fim do Comprimento Tangente</b> <i>Precisão decimal</i> (Disponível quando &#39;Tipo de Splines da Ponte&#39; estiver definido como &#39;Bézier Cúbico&#39;) | O comprimento da tangente &#39;in&#39; para o ponto final na spline #2 de todas as splines geradas. |
| <b>Início da Rotação Tangente</b> <i>Precisão decimal</i> (Disponível quando &#39;Tipo de Splines da Ponte&#39; estiver definido como &#39;Bézier Cúbico&#39;) | A rotação da tangente “out” para o ponto inicial na spline #1 de todas as splines geradas.<br>O valor é um número de voltas. |
| <b>Fim da Rotação Tangente</b> <i>Precisão decimal</i> (Disponível quando &#39;Tipo de Splines da Ponte&#39; estiver definido como &#39;Bézier Cúbico&#39;) | A rotação da tangente “in” para o ponto final na spline #2 de todas as splines geradas.<br>O valor é um número de voltas. |
| <b>Visualizar</b> |  |
| <b>Valor de Segmentos</b> <i>Inteiro</i> | Ajusta o número de segmentos usados para desenhar a visualização de spline na saída da Visualização. Um valor mais alto resulta em uma linha mais suave. |
| <b>Mostrar Auxiliar de Direção</b> <i>Booleano</i> | Exibe um ponto no início da spline e uma ponta de seta no final da saída de Visualização. |
| <b>Mostrar Envelope de Thickness</b> <i>Booleano</i> | Exibe linhas adicionais nas bordas do thickness da spline. |
| <b>Thickness (px)</b> <i>Flutuante</i> | Ajusta o thickness da visualização da spline em pixels na saída da Visualização. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-bridge-2-splines.resources/SplineBridge-2Splines_Variant1-Before.jpg" alt="SplineBridge-2Splines_Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-bridge-2-splines.resources/SplineBridge-2Splines_Variant1-After.jpg" alt="SplineBridge-2Splines_Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](spline-bridge-2-splines.resources/SplineBridge-2Splines_Demo.gif "Exemplo de nó 2")

</td>
</tr>
</table>
