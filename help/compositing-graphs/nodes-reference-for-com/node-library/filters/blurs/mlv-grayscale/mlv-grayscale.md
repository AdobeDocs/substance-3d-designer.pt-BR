---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-grayscale.html"
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
source-git-commit: 5efb14d81ad72b1982785319e446d7eb318c9a03
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 1%

---


# Escala de cinza MLV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Escala de cinza MLV: ícone](mlv-grayscale.resources/MLV_Grayscale_Icon.png "Escala de cinza MLV: ícone")

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

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Tons de cinza</i> | A imagem em tons de cinza que deve ser processada. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Saída</b> <i>Tons de cinza</i> | A imagem em tons de cinza filtrada. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Intensidade</b> *Flutuante* | A intensidade da filtragem aplicada à imagem.<br><br>Valores mais altos resultam em mais suavização de detalhes e ruído em áreas mais planas. |
| <b>Smoothness</b> *Flutuante* | A intensidade do alisamento aplicado nas áreas de estruturação, que resulta em áreas mais redondas e diminui o efeito de passo, que pode ocorrer em intensidades de filtragem mais altas. |
| <b>Critério</b> *Inteiro* | O critério usado para selecionar os valores que definirão as áreas de estruturação na imagem.<br><br>Em outras palavras, como os pixels devem ser *agrupados* em áreas que devem ser suavizadas.<br><br>*- Variação:* selecione valores com a menor dispersão ao redor da média, o que resulta em clusters de pixels semelhantes uns aos outros <br>*- Coeficiente de variação:* selecione valores considerando a média, o que resulta em menos variação de áreas mais brilhantes de forma inversa |
| <b>Gaussiano</b> *Booleano* | Use uma distribuição Gaussiana para agrupar pixels em áreas de estruturação.<br><br>Quando &#39;Verdadeiro&#39;, isso resulta em áreas mais suaves e um efeito de nivelamento reduzido. |
| <b>Iterações</b> *Inteiro* | O número de vezes que o filtro é executado, onde cada iteração é aplicada no resultado da anterior.<br><br>Mais iterações resultam em áreas de estruturação mais planas e nítidas. |

## Exemplos

<table>
  <tr>
    <td>
      <img src="mlv-grayscale.resources/MLV_Variant1A.png" alt="MLV_Variant1A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="mlv-grayscale.resources/MLV_Variant1B.png" alt="MLV_Variant1B">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-grayscale.resources/MLV_Variant2A.png" alt="MLV_Variant2A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="mlv-grayscale.resources/MLV_Variant2B.png" alt="MLV_Variant2B">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-grayscale.resources/MLV_Variant2A.png" alt="MLV_Variant2A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="mlv-grayscale.resources/MLV_Variant2C.png" alt="MLV_Variant2C">
      <br><i>Depois</i>
    </td>
  </tr>
</table>
