---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-grayscale.html"
breadcrumb-title: ''
description: Use o filtro Desfoque em Escala de Cinza MLV para aplicar efeitos de desfoque de movimento a texturas em escala de cinza para obter aparências dinâmicas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > MLV grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Escala de cinza MLV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---


# Escala de cinza MLV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Escala de cinza MLV: ícone](../../../../../../assets/MLV_Grayscale_Icon.png "Escala de cinza MLV: ícone")

<b>Entrada:</b> Filtros > Desfoques

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

MLV significa <b>&#39;Média da Menor Variação&#39;</b>. Esse filtro melhora as arestas e suaviza o ruído em uma imagem.

O filtro localiza áreas estruturantes em uma imagem e as usa para aumentar a nitidez e o nivelamento. Em alguns casos, isso pode resultar em degraus ao longo de gradientes mais largos do que as áreas de estruturação.

</td>
</tr>
</table>

>[!NOTE]
>
> Veja também [Cor do MLV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/mlv-color/mlv-color.md).

## Conectores de entrada

<b>Entrada </b>*Tons de Cinza* A imagem em tons de cinza que deve ser processada.

## Conectores de saída

<b>Saída </b>*Em Tons de Cinza* A imagem em tons de cinza filtrada.

## Parâmetros

<b>Intensidade</b> *Flutuante* A intensidade do filtro aplicado à imagem.\
Valores mais altos resultam em mais suavização de detalhes e ruído em áreas mais planas.

<b>Smoothness</b> *Flutuação* A intensidade da suavização aplicada às áreas de estruturação, que resulta em áreas mais redondas e diminui o efeito de revisão que pode ocorrer em intensidades de filtragem mais altas.

<b>Critério</b> *Inteiro* O critério usado para selecionar os valores que definirão as áreas de estruturação na imagem.\
Em outras palavras, como os pixels devem ser *agrupados* em áreas que devem ser suavizadas.\
*- Variância:* Selecione valores com a menor dispersão em torno da média, o que resulta em clusters de pixels semelhantes uns aos outros\
*- Coeficiente de variação:* Selecione valores levando em consideração a média, o que resulta em menos variação inversamente nas áreas mais brilhantes

<b>Gaussiano</b> *Booleano* Use uma distribuição Gaussiana para agrupar pixels em áreas de estruturação.\
Quando &#39;Verdadeiro&#39;, isso resulta em áreas mais suaves e um efeito de nivelamento reduzido.

<b>Iterações</b> *Inteiro* O número de vezes que o filtro é executado, onde cada iteração é aplicada ao resultado da anterior.\
Mais iterações resultam em áreas de estruturação mais planas e nítidas.

## Exemplos

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant1A.png" alt="MLV_Variant1A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant1B.png" alt="MLV_Variant1B">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant2A.png" alt="MLV_Variant2A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant2B.png" alt="MLV_Variant2B">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant2A.png" alt="MLV_Variant2A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant2C.png" alt="MLV_Variant2C">
      <br><i>Depois</i>
    </td>
  </tr>
</table>
