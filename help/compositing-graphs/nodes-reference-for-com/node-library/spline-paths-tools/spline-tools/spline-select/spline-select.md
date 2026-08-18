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
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---


# Seleção de Spline

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](../../../../../../assets/spline-select-icon.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Seleciona splines na lista de entrada de acordo com os critérios especificados e gera a saída de uma nova lista, incluindo apenas as splines selecionadas.

As splines selecionadas também podem ser cortadas.

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

<b>Modo de Seleção</b> *Inteiro* O método de seleção das linhas na lista de entrada:\
*- Primeiro*: Seleciona a primeira spline na lista;\
*- Último*: Seleciona a última spline na lista;\
*- Índice*: Seleciona a spline com o índice especificado;\
*- Intervalo*: Seleciona as splines em que os índices estão incluídos no intervalo especificado.

<b>Índice de Spline</b> *Inteiro* (Disponível quando ‘Modo de Seleção’ estiver definido como ‘Índice’)O índice da spline que deve ser selecionado.

<b>Início do Intervalo</b> *Inteiro* (Disponível quando ‘Modo de Seleção’ está definido como ‘Intervalo’)O índice mais baixo no intervalo de splines selecionados.

<b>Fim do Intervalo</b> *Inteiro* (Disponível quando ‘Modo de Seleção’ está definido como ‘Intervalo’)O índice mais alto no intervalo de splines selecionado.<b></b>

<b>Iniciar</b> *Flutuante* Desloca o início da parte da spline que deve ser selecionada. Isso apara efetivamente o spline.\
O valor representa o comprimento normalizado da spline.

<b>Fim</b> *Flutuante* Desloca a extremidade da parte da spline que deve ser selecionada. Isso apara efetivamente o spline.\
O valor representa o comprimento normalizado da spline.

+++Visualização
<b>Valor de Segmentos</b> *Inteiro* Ajusta o número de segmentos usados para desenhar a visualização de spline na saída da Visualização.\
Um valor mais alto resulta em uma linha mais suave.

<b>Mostrar Auxiliar de Direção</b> *Booleano* Exibe um ponto no início da spline e uma ponta de seta no final da saída de Visualização.

<b>Mostrar Envelope de Thickness</b> *Booleano*\
Exibe linhas adicionais nas bordas do thickness da spline.

<b>Thickness (px)</b> *Flutuante* Ajusta o thickness da visualização da spline em pixels na saída da Visualização.

+++

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineSelect-Variant1-Before.jpg" alt="SplineSelect-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineSelect-Variant1-After2.jpg" alt="SplineSelect-Variant1-After2">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineSelect-Variant2-Before.jpg" alt="SplineSelect-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineSelect-Variant2-After.jpg" alt="SplineSelect-Variant2-After">
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

![Exemplo de nó 1](../../../../../../assets/SplineSelect-Demo.gif "Exemplo de nó 1")

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
