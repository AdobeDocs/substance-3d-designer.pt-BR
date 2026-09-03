---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-merge-list.html"
breadcrumb-title: ''
description: Use o nó Lista de mesclagem de spline para mesclar várias splines em uma única lista de spline para operações combinadas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Merge List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lista de mesclagem de spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 1%

---


# Lista de mesclagem de spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](spline-merge-list.resources/spline-merge-list-01.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Mescla todas as linhas na lista de entrada em uma única linha.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Cordas de spline</b> <i>Cor</i> | As coordenadas dos pontos das linhas divisórias de entrada codificadas nos canais RGBA de uma imagem colorida:<br><b>R</b> - posição X<br><b>G</b> - posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br> - Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br> - Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> <i>Cor</i> | Dados adicionais das splines de entrada codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usadas<br><b>A</b> - Não Usadas |
| <b>Valor da spline</b> <i>Inteiro</i> | O número de splines de entrada. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Visualizar</b> <i>Tons de cinza</i> | A visualização das splines mescladas como uma imagem em tons de cinza. |
| <b>Cordas de spline</b> <i>Cor</i> | As coordenadas dos pontos das splines mescladas codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Posição X<br><b>G</b> - Posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br> - Sinal: a spline está fechada (negativa) ou aberta (positiva);<br> - Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> <i>Cor</i> | Dados adicionais das splines mescladas codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usadas<br><b>A</b> - Não Usadas |
| <b>Valor da spline</b> <i>Inteiro</i> | O número de splines mesclados. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Limite de Distância da Curva Fechada</b> <i>Flutuante</i> | A distância no espaço de textura abaixo da qual duas extremidades de um mesmo spline são processadas como um único ponto fechando esse spline.<br>Isso evita sobreposições ao espalhar formas ou mapear imagens ao longo das splines. |
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
      <img src="spline-merge-list.resources/spline-merge-list-02.jpg" alt="SplineMergeList-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-merge-list.resources/spline-merge-list-03.jpg" alt="SplineMergeList-Variant2-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-merge-list.resources/spline-merge-list-04.jpg" alt="SplineMergeList-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-merge-list.resources/spline-merge-list-05.jpg" alt="SplineMergeList-Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![Demonstração de nó](spline-merge-list.resources/spline-merge-list-06.gif "Demonstração de nó")
