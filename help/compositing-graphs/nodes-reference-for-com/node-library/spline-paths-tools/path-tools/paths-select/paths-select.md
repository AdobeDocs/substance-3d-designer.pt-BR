---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-select.html"
breadcrumb-title: ''
description: Use o nó Seleção de caminhos para selecionar e filtrar caminhos específicos de uma lista de caminhos com base em critérios.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Seleção de demarcadores
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---


# Seleção de demarcadores

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](../../../../../../assets/paths-select-icon.png "Ícone de nó")

<b>Ferramentas de Spline e Caminho </b> > Ferramentas de Caminho

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Isole um caminho entre vários contidos em Caminhos.

</td>
</tr>
</table>

## Conectores de entrada

<b>Rótulo</b> *Tipo*\
Uma lista de caminhos de segmentos codificados. Conecte esta entrada ao resultado de uma [Máscara para Caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) ou a outro nó de processamento de Caminho.

## Conectores de saída

<b>Caminhos</b> *Cor*\
A entrada Caminhos com apenas um caminho. Você pode usar [Visualizar Caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) para ter uma ideia do que o resultado representa, usar outro nó de processamento de Caminhos ou inseri-lo em um [Caminhos para Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) para processá-lo posteriormente como Splines.

## Parâmetros

<b>Modo de Seleção</b> *Inteiro* O método usado para selecionar os Caminhos:\
*- Por ID:* Seleciona o caminho na lista cujo índice corresponde ao especificado em <b>ID do Caminho</b>;\
*- Por Comprimento:* Seleciona os caminhos cujo comprimento está acima ou abaixo do limite especificado em <b>Comprimento de Destino</b>.

<b>ID do Caminho</b> *Inteiro* (Disponível quando o <b>Modo de Seleção</b> está definido como *Por ID*)\
O índice do caminho selecionado.\
Um valor maior que o número de caminhos em <b>Caminhos *resulta em*</b> uma saída em branco.

<b>Comprimento Maior ou Menor?</b> *Booleano* (Disponível quando o <b>Modo de Seleção</b> está definido como *Por Comprimento*)\
Controla se a seleção deve incluir um comprimento maior ou menor que <b>Tamanho de Destino</b>.

<b>Comprimento de Destino</b> *Flutuante*(Disponível quando o <b>Modo de Seleção</b> está definido como *Por Comprimento*)\
O limite de comprimento usado para selecionar splines.

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/PathsSelect-Variant1.jpg" alt="PathsSelect-Variant1">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/PathsSelect-Variant2.jpg" alt="PathsSelect-Variant2">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
