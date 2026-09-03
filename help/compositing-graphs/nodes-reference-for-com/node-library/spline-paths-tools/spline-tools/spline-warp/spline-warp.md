---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-warp.html"
breadcrumb-title: ''
description: Use o nó Distorção de spline para distorcer texturas ao longo de caminhos de spline e criar padrões curvos e orgânicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Distorção de spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1135'
ht-degree: 0%

---


# Distorção de spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](spline-warp.resources/spline-warp-01.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Desloca as splines de entrada com base no Mapa de intensidade de entrada ou no Mapa de vetor.

A intensidade do efeito de distorção pode ser ajustada ao longo da spline usando controles de atenuação.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Visualizar</b> <i>Tons de cinza</i> | A visualização das linhas de entrada como uma imagem em tons de cinza. |
| <b>Cordas de spline</b> <i>Cor</i> | As coordenadas dos pontos das linhas divisórias de entrada codificadas nos canais RGBA de uma imagem colorida:<br><b>R</b> - posição X<br><b>G</b> - posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br> - Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br> - Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> <i>Cor</i> | Dados adicionais das splines de entrada codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usadas<br><b>A</b> - Não Usadas |
| <b>Valor da spline</b> <i>Inteiro</i> | O número de splines de entrada. |
| <b>Mapa de Intensidade</b> <i>Tons de cinza</i> | (Disponível quando a opção “Usar mapa vetorial” estiver definida como “Falso”) A imagem em tons de cinza de entrada usada para controlar a direção e a intensidade do efeito de distorção nos splines de entrada.<br>A cor de cada pixel na imagem especifica um multiplicador para deslocar os pontos da spline ao longo de seu normal (ou seja, a direção perpendicular à spline), até o intervalo completo da imagem.<br>Os valores [0; 1] na imagem são remapeados para o intervalo [-1; 1] quando lidos como um multiplicador: 0 e 1 deslocam a spline pela mesma distância, mas em direções opostas. 0,5 deixa a spline no lugar. |
| <b>Mapa vetorial</b> <i>Tons de cinza</i> | (Disponível quando a opção “Usar mapa vetorial” estiver definida como “Verdadeiro”) A imagem colorida de entrada usada para controlar a direção e a intensidade do efeito de distorção nos splines de entrada.<br>A cor de cada pixel na imagem especifica o vetor (X, Y), cujas coordenadas são codificadas nos canais vermelho (X) e verde (Y). +X está à direita e +Y está para baixo.<br>Os valores [0; 1] na imagem são remapeados para o intervalo [-1; 1] quando lidos como coordenadas vetoriais: 0 vermelho desloca os pontos para a esquerda e 0 verde desloca os pontos para cima. 0,5 vermelho e verde deixam a spline no lugar. |
| <b>Curva de atenuação</b> <i>Tons de cinza</i> | A imagem que descreve uma curva usando os valores de sua primeira linha de pixels.<br>Quando o parâmetro Usar curva de atenuação for definido como Verdadeiro, essa entrada será usada para controlar a atenuação do efeito de distorção próximo ao início e ao fim da spline.<br>A curva fornece um perfil para a atenuação, onde o primeiro pixel na linha é a intensidade do efeito de distorção no início da spline e o último é a intensidade no final. O valor de tons de cinza é a intensidade.<br>Você pode usar um nó de curva para criar a curva. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Visualizar</b> <i>Tons de cinza</i> | A visualização das linhas de saída como uma imagem em tons de cinza. |
| <b>Cordas de spline</b> <i>Cor</i> | As coordenadas dos pontos das linhas divisórias de saída codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Posição X<br><b>G</b> - Posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br> - Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br> - Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> <i>Cor</i> | Dados adicionais das splines de saída codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usadas<br><b>A</b> - Não Usadas |
| <b>Valor da spline</b> <i>Inteiro</i> | O número de splines de saída. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Intensidade de distorção</b> <i>Flutuante</i> | A intensidade com que os splines são deslocados. |
| <b>Centro de distorção</b> <i>Flutuante</i> | Especifica o valor do Mapa de Intensidade que corresponde a deixar as splines no lugar.<br>Um valor de 0 ou 1 significa que as splines só podem ser deslocadas de um lado. |
| <b>Modo de amostragem</b> <i>Inteiro</i> | O método de mapear os valores no Mapa de Intensidade ou no Mapa de Vetor para os splines:<br>- <i>espaço de Textura</i>: os valores são aplicados aos splines nos quais estariam se colocados em uma textura usando as coordenadas UV da textura. Isso aplica efetivamente o valor às linhas de spline “no local”;<br>- <i>Horizontal ao longo da linha de spline</i>: os valores são aplicados diretamente às coordenadas das linhas de spline codificadas (consulte a entrada de Palavras de spline), onde cada linha é aplicada a uma linha de spline diferente de cima para baixo;<br>- <i>Hor. ao longo do spline (rand. deslocamento X)</i>: os valores são aplicados diretamente às coordenadas das splines codificadas (consulte a entrada de Coords de spline), com um deslocamento horizontal aleatório no mapa de Escala para cada spline (ou seja, cada linha nas Coords de Spline);<br>- <i>Hora. ao longo do spline (rand. deslocamento Y)</i>: os valores são aplicados diretamente às coordenadas das splines codificadas (consulte entrada de Coords de spline), com um deslocamento vertical aleatório no mapa de Escala para cada spline (ou seja, cada linha nas Coords de spline). |
| <b>Usar Mapa Vetorial</b> <i>Booleano</i> | Alterna o método de deslocamento das splines para o uso de uma entrada do Mapa de vetor para especificar a direção da deslocamento.<br>A cor de cada pixel na imagem especifica o vetor (X, Y), cujas coordenadas são codificadas nos canais vermelho (X) e verde (Y). +X está à direita e +Y está para baixo.<br>Os valores [0; 1] na imagem são remapeados para o intervalo [-1; 1] quando lidos como coordenadas vetoriais: 0 vermelho desloca os pontos para a esquerda e 0 verde desloca os pontos para cima. 0,5 vermelho e verde deixam a spline no lugar. |
| <b>Usar curva de atenuação</b> <i>Booleano</i> | Permite controlar a intensidade do efeito de distorção ao longo de uma spline usando uma curva codificada na imagem de entrada da Curva de atenuação. |
| <b>Divisão em blocos gráficos do mapa de intensidade</b> <i>Flutuante</i> | (Disponível quando o “Modo de amostragem” não está definido como “Espaço de Textura”) Ajusta a divisão em blocos gráficos do Mapa de intensidade quando mapeado para as coordenadas de spline diretamente (consulte Entrada das coordenadas de spline ). |
| <b>Iniciar Atenuação</b> <i>Flutuante</i> | (Disponível quando a opção “Usar curva de atenuação” estiver definida como “Falso”) Um multiplicador para a atenuação do efeito de deformação próximo ao início da spline.<br>Um valor de 1 significa que nenhuma deformação é aplicada ao início da spline. |
| <b>Encerrar atenuação</b> <i>Flutuante</i> | (Disponível quando a opção “Usar curva de atenuação” estiver definida como “Falso”) Um multiplicador para a atenuação do efeito de deformação próximo ao final da spline.<br>Um valor de 1 significa que nenhuma deformação é aplicada ao final da spline. |
| <b>Recalcular Tangentes</b> <i>Booleano</i> | Quando verdadeiro, as tangentes de uma spline são recalculadas depois que o efeito de distorção é aplicado.<br>Isso garante que as tangentes da spline permaneçam consistentes com sua trajetória quando usadas em nós como Dispersão na spline ou Mapeador de fluxo da spline. |
| <b>Visualizar</b> |  |
| <b>Valor de Segmentos</b> <i>Inteiro</i> | Ajusta o número de segmentos usados para desenhar a visualização de spline na saída da Visualização.<br>Um valor mais alto resulta em uma linha mais suave. |
| <b>Mostrar Auxiliar de Direção</b> <i>Booleano</i> | Exibe um ponto no início da spline e uma ponta de seta no final da saída de Visualização. |
| <b>Mostrar Envelope de Thickness</b> <i>Booleano</i> | Exibe linhas adicionais nas bordas do thickness da spline. |
| <b>Thickness (px)</b> <i>Flutuante</i> | Ajusta o thickness da visualização da spline em pixels na saída da Visualização. |
| <b>Intensidade de visualização do plano de fundo</b> <i>Flutuante</i> | O valor multiplicado na imagem de entrada da Visualização de plano de fundo. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-warp.resources/spline-warp-02.jpg" alt="SplineWarp-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-warp.resources/spline-warp-03.jpg" alt="SplineWarp-Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-warp.resources/spline-warp-04.jpg" alt="SplineWarp-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-warp.resources/spline-warp-05.jpg" alt="SplineWarp-Variant2-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 1](spline-warp.resources/spline-warp-06.gif "Exemplo de nó 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
