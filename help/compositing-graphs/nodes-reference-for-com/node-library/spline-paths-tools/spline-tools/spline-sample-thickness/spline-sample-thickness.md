---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-sample-thickness.html"
breadcrumb-title: ''
description: Use o nó Thickness de amostra de spline para obter amostras de valores de thickness ao longo das splines para efeitos de procedimento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Sample Thickness
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Thickness de amostra de spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---


# Thickness de amostra de spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](spline-sample-thickness.resources/spline-sample-thickness-01.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Modifica o thickness das splines de entrada mapeando um mapa de Thickness de entrada nelas.

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
| <b>Mapa de Espessura</b> <i>Tons de cinza</i> | A imagem em tons de cinza de entrada usada para alterar o thickness da spline de entrada. |

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
| <b>Modo de amostragem</b> <i>Inteiro</i> | O método de mapear os valores no Mapa de Espessura para os splines:<br>- <i>espaço de Textura</i>: os valores são aplicados aos splines nos quais estariam se colocados em uma textura usando as coordenadas UV da textura. Isso aplica efetivamente o valor às linhas de spline “no local”;<br>- <i>Horizontal ao longo da linha de spline</i>: os valores são aplicados diretamente às coordenadas das linhas de spline codificadas (consulte a entrada de Palavras de spline), onde cada linha é aplicada a uma linha de spline diferente de cima para baixo;<br>- <i>Hor. ao longo do spline (rand. deslocamento X)</i>: os valores são aplicados diretamente às coordenadas das splines codificadas (consulte a entrada de Coords de spline), com um deslocamento horizontal aleatório no mapa de Escala para cada spline (ou seja, cada linha nas Coords de Spline);<br>- <i>Hora. ao longo do spline (rand. deslocamento Y)</i>: os valores são aplicados diretamente às coordenadas das splines codificadas (consulte entrada de Coords de spline), com um deslocamento vertical aleatório no mapa de Escala para cada spline (ou seja, cada linha nas Coords de spline). |
| <b>Opacidade</b> <i>Flutuante</i> | Um multiplicador da intensidade da contribuição da entrada do Mapa de espessura para o thickness do spline. |
| <b>Modo de Mesclagem</b> <i>Inteiro</i> | O método de mesclar os dados do Mapa de Espessura com o <span id="_Hlk135820484"></span>thickness:<br>- <i>Copiar</i> da spline de entrada: substitua o thickness da spline pelos valores do Mapa de Altura;<br>- <i>Adicionar</i>: adicione os valores do Mapa de Espessura ao thickness da spline;<br>- <i>Subtrair</i>: Subtrair os valores do Mapa de Espessura para o thickness da spline;<br>- <i>Multiplicar</i>: multiplique os valores do Mapa de Espessura com os thickness de spline. |
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
      <img src="spline-sample-thickness.resources/spline-sample-thickness-02.jpg" alt="SplineSampleThickness-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-sample-thickness.resources/spline-sample-thickness-03.jpg" alt="EspessuraAmostraEspessura-Variante1-Depois">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-sample-thickness.resources/spline-sample-thickness-04.jpg" alt="SplineSampleThickness-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-sample-thickness.resources/spline-sample-thickness-05.jpg" alt="SplineSampleThickness-Variant2-After">
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

![Exemplo de nó 1](spline-sample-thickness.resources/spline-sample-thickness-06.jpg "Exemplo de nó 1")

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](spline-sample-thickness.resources/spline-sample-thickness-07.gif "Exemplo de nó 2")

</td>
</tr>
</table>
