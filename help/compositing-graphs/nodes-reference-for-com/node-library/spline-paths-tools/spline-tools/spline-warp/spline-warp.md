---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-warp.html"
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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 0%

---


# Distorção de spline

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](../../../../../../assets/spline-warp-icon.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Desloca as splines de entrada com base no Mapa de intensidade de entrada ou no Mapa de vetor.

A intensidade do efeito de distorção pode ser ajustada ao longo da spline usando controles de atenuação.

</td>
</tr>
</table>

## Conectores de entrada

<b>Visualizar</b> *Tons de cinza* A visualização das linhas divisórias de entrada como uma imagem em tons de cinza.

<b>Cordas de spline</b> *Cor* As coordenadas dos pontos das splines de entrada codificadas nos canais RGBA de uma imagem colorida:\
<b> R</b> - Posição X\
<b> G</b> - posição Y\
<b> B</b> - Height\
<b>A</b> - Dados empacotados:\
* Sinal: Spline é fechado (negativo) ou aberto (positivo);\
* Valor absoluto: Thickness + 1.

<b>Dados de Spline</b> *Cor* Dados adicionais das splines de entrada codificados nos canais RGBA de uma imagem colorida.\
<b> R</b> - Tangentes X\
<b> G</b> - Tangentes Y\
<b> B</b> - Não Usado\
<b> A</b> - Não Usado

<b>Valor da spline</b> *Inteiro* O número de splines de entrada.

<b>Mapa de Intensidade</b> *Tons de cinza* (Disponível quando “Usar Mapa Vetorial” estiver definido como “Falso”)\
A imagem em tons de cinza de entrada usada para controlar a direção e a intensidade do efeito de deformação nas splines de entrada.\
A cor de cada pixel na imagem especifica um multiplicador para deslocar os pontos da spline ao longo de seu normal (ou seja, a direção perpendicular à spline), até o intervalo completo da imagem.\
Os valores [0; 1] na imagem são remapeados para o intervalo [-1; 1] quando lidos como um multiplicador: 0 e 1 deslocam a spline pela mesma distância, mas em direções opostas. 0,5 deixa a spline no lugar.

<b>Mapa vetorial</b> *Tons de cinza* (Disponível quando a opção “Usar mapa vetorial” estiver definida como “Verdadeiro”)A imagem colorida de entrada usada para controlar a direção e a intensidade do efeito de distorção nas splines de entrada.\
A cor de cada pixel na imagem especifica o vetor (X, Y), cujas coordenadas são codificadas nos canais vermelho (X) e verde (Y). +X está à direita e +Y está para baixo.\
Os valores [0; 1] na imagem são remapeados para o intervalo [-1; 1] quando lidos como coordenadas vetoriais: 0 vermelho desloca os pontos à esquerda e 0 verde desloca os pontos para cima. 0,5 vermelho e verde deixam a spline no lugar.

<b>Curva de atenuação</b> *Tons de cinza* A imagem que descreve uma curva usando os valores da primeira linha de pixels.\
Quando o parâmetro Usar curva de atenuação é definido como Verdadeiro, essa entrada é usada para controlar a atenuação do efeito de distorção próximo ao início e ao fim da spline.\
A curva fornece um perfil para a atenuação, onde o primeiro pixel na linha é a intensidade do efeito de distorção no início da spline e o último é a intensidade no final. O valor de tons de cinza é a intensidade.\
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

<b>Intensidade de distorção</b> *Flutuação* A intensidade com que os splines são deslocados.

<b>Centro de distorção</b> *Flutuante* Especifica o valor do Mapa de Intensidade que corresponde a deixar as splines no lugar.\
Um valor de 0 ou 1 significa que os splines só podem ser deslocados de um lado.

<b>Modo de amostragem</b> *Inteiro* O método de mapear os valores no Mapa de Intensidade ou no Mapa de Vetor para os splines:\
*- Espaço de textura*: os valores são aplicados às splines nos quais estariam se fossem colocados em uma textura usando as coordenadas UV da textura. Isso aplica efetivamente o valor aos splines “in place”;\
*- Horizontal ao longo da spline*: os valores são aplicados diretamente às coordenadas das splines codificadas (consulte entrada de Coords da spline), onde cada linha é aplicada a uma spline diferente de cima para baixo;\
*- Hora. ao longo do spline (rand. deslocamento X)*: os valores são aplicados diretamente às coordenadas das splines codificadas (consulte entrada de Coords de spline), com um deslocamento horizontal aleatório no mapa de Escala para cada spline (ou seja, cada linha em Coords de spline);\
*- Hora. ao longo do spline (rand. deslocamento Y)*: os valores são aplicados diretamente às coordenadas das splines codificadas (consulte entrada de Coords de spline), com um deslocamento vertical aleatório no mapa de Escala para cada spline (ou seja, cada linha nas Coords de spline).

<b>Usar Mapa Vetorial</b> *Booleano* Alterna o método de deslocamento das splines para o uso de uma entrada do Mapa de Vetor para especificar a direção do deslocamento.\
A cor de cada pixel na imagem especifica o vetor (X, Y), cujas coordenadas são codificadas nos canais vermelho (X) e verde (Y). +X está à direita e +Y está para baixo.\
Os valores [0; 1] na imagem são remapeados para o intervalo [-1; 1] quando lidos como coordenadas vetoriais: 0 vermelho desloca os pontos à esquerda e 0 verde desloca os pontos para cima. 0,5 vermelho e verde deixam a spline no lugar.

<b>Usar curva de atenuação</b> *Booleano* Permite controlar a intensidade do efeito de distorção ao longo de uma spline usando uma curva codificada na imagem de entrada da Curva de Atenuação.<b></b>

<b>Divisão em blocos gráficos do mapa de intensidade</b> *Flutuante* (Disponível quando “Modo de Amostragem” não está definido como “Espaço de Textura”)Ajusta a divisão em blocos gráficos do Mapa de Intensidade quando mapeado para as coordenadas de spline diretamente (consulte entrada de Cordas de spline).<b></b>

<b>Iniciar Atenuação</b> *Flutuante* (Disponível quando a opção “Usar curva de atenuação” estiver definida como “Falso”)Um multiplicador para a atenuação do efeito de distorção próximo ao início da spline.\
Um valor de 1 significa que nenhuma distorção será aplicada ao início da spline.

<b>Encerrar atenuação</b> *Flutuante* (Disponível quando a opção “Usar curva de atenuação” estiver definida como “Falso”)Um multiplicador para a atenuação do efeito de distorção próximo ao final da spline.\
Um valor de 1 significa que nenhuma distorção foi aplicada ao final da spline.<b></b>

<b>Recalcular Tangentes</b> *Booleano* Quando verdadeiro, as tangentes de uma spline são recalculadas depois que o efeito de distorção é aplicado.\
Isso garante que as tangentes da spline permaneçam consistentes com sua trajetória quando usadas em nós como Dispersão na spline ou Mapeador de fluxo da spline.

+++Visualização
<b>Valor de Segmentos</b> *Inteiro* Ajusta o número de segmentos usados para desenhar a visualização de spline na saída da Visualização.\
Um valor mais alto resulta em uma linha mais suave.

<b>Mostrar Auxiliar de Direção</b> *Booleano* Exibe um ponto no início da spline e uma ponta de seta no final da saída de Visualização.

<b>Mostrar Envelope de Thickness</b> *Booleano*\
Exibe linhas adicionais nas bordas do thickness da spline.

<b>Thickness (px)</b> *Flutuante* Ajusta o thickness da visualização da spline em pixels na saída da Visualização.

<b>Intensidade de visualização do plano de fundo</b> *Flutuante*\
O valor multiplicado na imagem de entrada da Visualização de plano de fundo.

+++

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant1-Before.jpg" alt="SplineWarp-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant1-After.jpg" alt="SplineWarp-Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant2-Before.jpg" alt="SplineWarp-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineWarp-Variant2-After.jpg" alt="SplineWarp-Variant2-After">
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

![Exemplo de nó 1](../../../../../../assets/SplineWarp-Demo.gif "Exemplo de nó 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
