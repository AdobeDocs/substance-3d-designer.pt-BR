---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-sample-height.html"
breadcrumb-title: ''
description: Use o nó Height de amostra de spline para obter amostras de valores de height ao longo das splines para efeitos de deslocamento processuais.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Sample Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Height de amostra de spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4ae20991693573dd44016a411c233b071fa96df6
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---


# Height de amostra de spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](spline-sample-height.resources/spline-sample-height-icon.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Modifica o height das splines de entrada mapeando um mapa de altura de entrada nelas.

O efeito do mapa de height mapeado pode ser ajustado alterando seu modo de mesclagem e a opacidade desse efeito.

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
| <b>Mapa de Heights</b> <i>Tons de cinza</i> | A imagem em tons de cinza de entrada usada para alterar o height da spline de entrada. |

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
| <b>Modo de amostragem</b> <i>Inteiro</i> | O método de mapear os valores no Mapa de Altura para os splines:<br>- <i>espaço de Textura</i>: os valores são aplicados aos splines nos quais estariam se colocados em uma textura usando as coordenadas UV da textura. Isso aplica efetivamente o valor às linhas de spline “no local”;<br>- <i>Horizontal ao longo da linha de spline</i>: os valores são aplicados diretamente às coordenadas das linhas de spline codificadas (consulte a entrada de Palavras de spline), onde cada linha é aplicada a uma linha de spline diferente de cima para baixo;<br>- <i>Hor. ao longo do spline (rand. deslocamento X)</i>: os valores são aplicados diretamente às coordenadas das splines codificadas (consulte a entrada de Coords de spline), com um deslocamento horizontal aleatório no mapa de Escala para cada spline (ou seja, cada linha nas Coords de Spline);<br>- <i>Hora. ao longo do spline (rand. deslocamento Y)</i>: os valores são aplicados diretamente às coordenadas das splines codificadas (consulte entrada de Coords de spline), com um deslocamento vertical aleatório no mapa de Escala para cada spline (ou seja, cada linha nas Coords de spline). |
| <b>Opacidade</b> <i>Flutuante</i> | Um multiplicador da intensidade da contribuição da entrada do Mapa de altura para o height da spline. |
| <b>Modo de Mesclagem</b> <i>Inteiro</i> | O método de mesclar os dados do Mapa de Altura com o height da spline de entrada:<br>- <i>Copiar</i>: substituir o height da spline pelos valores do Mapa de Altura;<br>- <i>Adicionar</i>: adicionar os valores do Mapa de Altura ao height da spline;<br>- <i>Subtrair</i>: Subtrair os valores do Mapa de Altura ao height da spline;<br>- <i>Multiplicar</i>: multiplicar os valores do Mapa de Altura em relação ao height da spline. |
| <b>Visualizar</b> |  |
| <b>Valor de Segmentos</b> <i>Inteiro</i> | Ajusta o número de segmentos usados para desenhar a visualização de spline na saída da Visualização.<br>Um valor mais alto resulta em uma linha mais suave. |
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
      <img src="spline-sample-height.resources/SplineSampleHeight-Variant1-Before.jpg" alt="SplineSampleHeight-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-sample-height.resources/SplineSampleHeight-Variant1-After.jpg" alt="SplineSampleHeight-Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-sample-height.resources/SplineSampleHeight-Variant1-Before.jpg" alt="SplineSampleHeight-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-sample-height.resources/SplineSampleHeight-Variant1-After3.jpg" alt="SplineSampleHeight-Variant1-After3">
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

![Exemplo de nó 1](spline-sample-height.resources/SplineSampleHeight-Variant1-After4.jpg "Exemplo de nó 1")

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](spline-sample-height.resources/SplineSampleHeight-Demo.gif "Exemplo de nó 2")

</td>
</tr>
</table>
