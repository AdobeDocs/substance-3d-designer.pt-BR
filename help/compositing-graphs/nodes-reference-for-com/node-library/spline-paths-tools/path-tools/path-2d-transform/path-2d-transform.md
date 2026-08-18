---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/path-2d-transform.html"
breadcrumb-title: ''
description: Use o nó Transformação 2D de caminho para transformar caminhos com operações de tradução, rotação e dimensionamento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Path 2D Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformação do caminho 2D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# Transformação do caminho 2D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](../../../../../../assets/path-2d-transform-icon.png "Ícone de nó")

<b>Ferramentas de Spline e Caminho </b> > Ferramentas de Caminho

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Transforma caminhos usando um cursor.

</td>
</tr>
</table>

## Conectores de entrada

<b>Caminhos</b> *Cor*\
Uma lista de caminhos de segmentos codificados. Conecte esta entrada ao resultado de uma [Máscara para Caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) ou a outro nó de processamento de Caminho.

## Conectores de saída

<b>Caminhos</b> *Cor*\
Os caminhos transformados. Você pode usar [Visualizar Caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) para ter uma ideia do que o resultado representa, usar outro nó de processamento de Caminhos ou inseri-lo em um [Caminhos para Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) para processá-lo posteriormente como Splines.

## Parâmetros

<b>Matriz de transformação</b> *Flutuante4*\
A matriz de transformação aplicada aos splines. Três modos de edição dos parâmetros da matriz estão disponíveis:\
*- Gizmo de transformação:* ajuste as alças do gizmo exibidas na [Exibição 2D](../../../../../../interface/2d-view/2d-view.md) quando o nó Transformação 2D de spline é selecionado;\
*- Rotação/Amplificação:* Controle individualmente a rotação e amplificação das splines. Observe que os valores sempre são aplicados relativamente à transformação atual. Por exemplo, aplicar 50% de largura duas vezes resulta em uma largura de 25%;\
*- Valores de matriz:* Clique no botão <b>Editar Valores de Matriz</b> para inserir diretamente os valores numéricos brutos da matriz.

<b>Deslocamento</b> *Flutuante2*\
Aplica um deslocamento de posição às linhas em X (horizontal) e Y (vertical).

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/Paths2DTransform-Variant1.jpg" alt="Paths2DTransform-Variant1">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/Paths2DTransform-Variant2.jpg" alt="Paths2DTransform-Variant2">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
