---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-select.html"
breadcrumb-title: ''
description: Use o nó Seleção de spline para selecionar e mascarar regiões específicas com base nos caminhos de spline nos seus gráficos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Seleção de Spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: e23f692fa31d1e7b9eeac692bb41186441fdda53
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---


# Seleção de Spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](spline-select.resources/spline-select-icon.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Seleciona splines na lista de entrada de acordo com os critérios especificados e gera a saída de uma nova lista, incluindo apenas as splines selecionadas.

As splines selecionadas também podem ser cortadas.

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
| <b>Modo de Seleção</b> <i>Inteiro</i> | O método de seleção de splines na lista de entrada:<br>- <i>Primeiro</i>: seleciona a primeira spline na lista;<br>- <i>Último</i>: seleciona a última spline na lista;<br>- <i>Índice</i>: seleciona a spline com o índice especificado;<br>- <i>Intervalo</i>: seleciona as splines cujos índices estão incluídos no intervalo especificado. |
| <b>Índice de Spline</b> <i>Inteiro</i> | (Disponível quando o “Modo de seleção” está definido como “Índice”) O índice da spline que deve ser selecionado. |
| <b>Início do Intervalo</b> <i>Inteiro</i> | (Disponível quando o “Modo de seleção” está definido como “Intervalo”) O índice mais baixo no intervalo de splines selecionados. |
| <b>Fim do Intervalo</b> <i>Inteiro</i> | (Disponível quando o “Modo de seleção” está definido como “Intervalo”) O índice mais alto no intervalo de splines selecionados. |
| <b>Iniciar</b> <i>Flutuante</i> | Desloca o início da parte da spline que deve ser selecionada. Isso apara efetivamente o spline.<br>O valor representa o comprimento normalizado da spline. |
| <b>Fim</b> <i>Flutuante</i> | Desloca a extremidade da parte da spline que deve ser selecionada. Isso apara efetivamente o spline.<br>O valor representa o comprimento normalizado da spline. |
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
      <img src="spline-select.resources/SplineSelect-Variant1-Before.jpg" alt="SplineSelect-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-select.resources/SplineSelect-Variant1-After2.jpg" alt="SplineSelect-Variant1-After2">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-select.resources/SplineSelect-Variant2-Before.jpg" alt="SplineSelect-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-select.resources/SplineSelect-Variant2-After.jpg" alt="SplineSelect-Variant2-After">
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

![Exemplo de nó 1](spline-select.resources/SplineSelect-Demo.gif "Exemplo de nó 1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
