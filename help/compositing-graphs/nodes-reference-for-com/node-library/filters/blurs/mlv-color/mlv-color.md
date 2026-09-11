---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-color.html"
breadcrumb-title: ''
description: Use o filtro Desfoque de cor MLV para aplicar efeitos de desfoque de movimento a texturas de cores para aparência visual dinâmica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > MLV color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cor MLV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5efb14d81ad72b1982785319e446d7eb318c9a03
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 1%

---


# Cor MLV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Cor do MLV: ícone](mlv-color.resources/MLV_Color_Icon.png "Cor do MLV: ícone")

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
> Consulte também [Escala de cinza MLV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/mlv-grayscale/mlv-grayscale.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Cor</i> | A imagem colorida que deve ser processada. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Saída</b> <i>Cor</i> | A imagem colorida filtrada. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Intensidade</b> *Precisão decimal* | A intensidade da filtragem aplicada à imagem.<br><br>Valores mais altos resultam em mais suavização de detalhes e ruído em áreas mais planas. |
| <b>Smoothness</b> *Precisão decimal* | A intensidade do alisamento aplicado nas áreas de estruturação, que resulta em áreas mais redondas e diminui o efeito de passo, que pode ocorrer em intensidades de filtragem mais altas. |
| <b>Critério</b> *Inteiro* | O critério usado para selecionar os valores que definirão as áreas de estruturação na imagem.<br><br>Em outras palavras, como os pixels devem ser *agrupados* em áreas que devem ser suavizadas.<br><br>*- Variação:* selecione valores com a menor dispersão ao redor da média, o que resulta em clusters de pixels semelhantes uns aos outros <br>*- Coeficiente de variação:* selecione valores considerando a média, o que resulta em menos variação de áreas mais brilhantes de forma inversa |
| <b>Gaussiano</b> *Booleano* | Use uma distribuição Gaussiana para agrupar pixels em áreas de estruturação.<br><br>Quando &#39;Verdadeiro&#39;, isso resulta em áreas mais suaves e um efeito de nivelamento reduzido. |
| <b>Afetar alfa</b> *Booleano* | Quando &#39;Verdadeiro&#39;, a filtragem também é aplicada no canal alfa da imagem.<br><br>Quando &#39;Falso&#39;, o canal alfa é totalmente ignorado e deixado como está na saída. |
| <b>Iterações</b> *Inteiro* | O número de vezes que o filtro é executado, onde cada iteração é aplicada no resultado da anterior.<br><br>Mais iterações resultam em áreas de estruturação mais planas e nítidas. |

## Exemplos

<table>
  <tr>
    <td>
      <img src="mlv-color.resources/MLV_Variant4A.png" alt="MLV_Variant4A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="mlv-color.resources/MLV_Variant4B.png" alt="MLV_Variant4B">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-color.resources/MLV_Variant5A.png" alt="MLV_Variant5A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="mlv-color.resources/MLV_Variant5B.png" alt="MLV_Variant5B">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-color.resources/MLV_Variant3A.png" alt="MLV_Variant3A">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="mlv-color.resources/MLV_Variant3B.png" alt="MLV_Variant3B">
      <br><i>Depois</i>
    </td>
  </tr>
</table>
