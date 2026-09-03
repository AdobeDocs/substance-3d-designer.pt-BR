---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-render.html"
breadcrumb-title: ''
description: Use o nó Renderização de spline para renderizar splines como texturas com largura, cor e modos de mesclagem personalizáveis.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Renderização de spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 0%

---


# Renderização de spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](spline-render.resources/spline-render-01.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Desenha cadeias de segmentos ao longo das <b>Splines</b> de entrada sobre o <b>Fundo</b> de entrada.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Fundo</b> <i>Tons de cinza</i> | A imagem em tons de cinza sobre a qual as splines devem ser desenhadas. |
| <b>Cordas de spline</b> <i>Cor</i> | As coordenadas dos pontos das linhas divisórias de entrada codificadas nos canais RGBA de uma imagem colorida:<br><b>R</b> - posição X<br><b>G</b> - posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br> - Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br> - Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> <i>Cor</i> | Dados adicionais das splines de entrada codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usadas<br><b>A</b> - Não Usadas |
| <b>Valor da spline</b> <i>Inteiro</i> | O número de splines de entrada. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Saída</b> <i>Tons de cinza</i> | A imagem resultante do desenho dos splines de entrada sobre o plano de fundo. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Modo</b> <i>Inteiro</i> | O método de seleção de linhas de spline a serem desenhadas:<br>- <i>Desenhar lista de linhas de spline</i>: desenhar todas as linhas de spline na lista de entrada;<br>- <i>Desenhar linha de spline única</i>: desenhar somente a linha de spline especificada na lista de entrada;<br>- <i>Desenhar intervalo de linhas de spline</i>: desenhar somente as linhas de spline no intervalo especificado da lista de entrada. |
| <b>Desenhar Índice de Spline</b> <i>Inteiro</i> | (Disponível quando “Modo” estiver definido como “Desenhar spline único”) O índice da spline que deve ser desenhado. |
| <b>Desenhar Intervalo De Spline</b> <i>Inteiro2</i> | (Disponível quando “Modo” estiver definido como “Desenhar intervalo de spline”) O intervalo de índices das splines que deve ser desenhado. |
| <b>Mostrar Auxiliar de Direção</b> <i>Booleano</i> | Para cada spline, desenha um ponto no início da spline e uma ponta de seta no final. |
| <b>Valor de Segmentos</b> <i>Inteiro</i> | Ajusta o número de segmentos desenhados ao longo das splines.<br>Um valor mais alto resulta em linhas mais suaves. |
| <b>Quantidade de spline do envelope</b> <i>Inteiro</i> | O número de segmentos duplicados que devem ser desenhados ao longo do thickness de cada spline. |
| <b>Iniciar</b> <i>Flutuante</i> | Desloca o início da parte da spline que deve ser desenhada.<br>O valor representa o comprimento normalizado da spline. |
| <b>Fim</b> <i>Flutuante</i> | Desloca a extremidade da parte da spline que deve ser desenhada.<br>O valor representa o comprimento normalizado da spline. |
| <b>Modo de Tamanho de Thickness</b> <i>Inteiro</i> | O método de calcular o thickness dos segmentos desenhados:<br>- <i>Imagem</i>: o valor é normalizado no espaço de textura, onde 1 é a largura total da imagem. Thickness é relativo à resolução da textura;<br>- <i>Pixel</i>: o valor é um número absoluto de pixels na textura, onde 1 é um pixel completo. O thickness é separado da resolução da textura. |
| <b>Thickness (imagem)</b> <i>Flutuante</i> | (disponível quando o “Modo do tamanho do Thickness” está definido como Imagem) O thickness dos segmentos desenhados normalizados no espaço de textura, onde 1 é a largura total da imagem. |
| <b>Thickness (px)</b> <i>Flutuante</i> | (disponível quando o “Modo de tamanho de Thickness” estiver definido como Pixel) O thickness dos segmentos desenhados como um número absoluto de pixels na textura, onde 1 é um pixel completo. |
| <b>Habilitar Junções</b> <i>Booleano</i> | Preenche as lacunas entre os segmentos individuais desenhados ao longo das splines usando discos. |
| <b>Correção Não Quadrada</b> <i>Booleano</i> | Ajuste a posição e o thickness dos pontos para manter a forma de spline em resoluções não quadradas.<br>Isso também afeta a distribuição uniforme. |
| <b>Cor</b> |  |
| <b>Intensidade de fundo</b> <i>Flutuante</i> | O valor multiplicado em relação à imagem de entrada do plano de fundo. |
| <b>Estilo de Spline</b> <i>Inteiro</i> | O método usado para colorir as splines:<br>- <i>Sólidas</i>: os segmentos são desenhados usando um valor uniforme em tons de cinza;<br>- <i>Gradiente</i>: um gradiente de preto para branco é aplicado a cada sequência de segmentos do início ao fim;<br>- <i>Height</i>: o height das splines é usado como o valor em tons de cinza para desenhar os segmentos. |
| <b>Cor da spline</b> <i>Flutuante</i> | O valor uniforme de tons de cinza usado para desenhar os segmentos.<br>Quando um Estilo de Spline diferente de “Sólido” é selecionado, essa cor é multiplicada pela cor estilizada. |
| <b>Luminância aleatória</b> <i>Flutuante</i> | Para cada sequência de segmentos não cortados em uma spline, o aplica um deslocamento aleatório no intervalo especificado ao valor de tons de cinza usado para desenhar essa sequência. |
| <b>Modo de Mesclagem</b> <i>Inteiro</i> | O método de mesclar as cores do plano de fundo e os segmentos sobrepostos desenhados ao longo das linhas de spline:<br>- <i>Máx</i>: o valor mais claro é usado;<br>- <i>Adicionar</i>: os valores são adicionados juntos. |
| <b>Segmentos aleatórios</b> |  |
| <b>Início de Segmentos Aleatórios</b> <i>Flutuante</i> | Ajusta a probabilidade de corte da sequência de segmentos próxima ao início da spline. |
| <b>Fim de Segmentos Aleatórios</b> <i>Flutuante</i> | Ajusta a probabilidade de corte da sequência de segmentos próxima ao final da spline. |
| <b>Deslocamento Aleatório</b> <i>Flutuante</i> | Define a quantidade máxima de deslocamento aplicada a cada segmento cortado ao longo de seu normal.<br>Este parâmetro não tem efeito quando Start e End estão definidos como 0. |
| <b>Centro de Deslocamento Aleatório</b> <i>Flutuante</i> | Desloca o centro do deslocamento aleatório aplicado a cada segmento cortado ao longo de seu normal. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-render.resources/spline-render-02.jpg" alt="SplineRender-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-render.resources/spline-render-03.jpg" alt="SplineRender-Variant2-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-render.resources/spline-render-04.jpg" alt="SplineRender-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-render.resources/spline-render-05.jpg" alt="SplineRender-Variant1-After">
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

<table>
  <tr>
    <td>
      <img src="spline-render.resources/spline-render-04.jpg" alt="SplineRender-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-render.resources/spline-render-06.jpg" alt="SplineRender-Variant3">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 1](spline-render.resources/spline-render-07.gif "Exemplo de nó 1")

</td>
</tr>
</table>
