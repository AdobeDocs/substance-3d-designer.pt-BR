---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-color.html"
breadcrumb-title: ''
description: Use o nó Cor do mapeador da ponte de spline para conectar texturas entre duas splines com o mapeamento de cores.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cor do mapeador da ponte de spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---


# Cor do mapeador da ponte de spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](../../../../../../assets/spline-bridge-mapper-color-icon.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Mapeia uma imagem colorida em uma lista de splines de entrada para que a imagem atravesse as splines na ordem.

</td>
</tr>
</table>

>[!TIP]
>
> O mapeamento vai do primeiro spline na lista até o último e atravessa os splines intermediários seguindo estritamente a ordem desses splines na lista.
> 
> Portanto, você deve ter cuidado com a ordem na qual você acrescenta splines com antecedência.

>[!NOTE]
>
> Consulte também [Escala de cinza do mapeador da ponte de spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-gra/spline-bridge-mapper-grayscale.md).

## Conectores de entrada

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

<b>Mapa de cores </b>*Cor* A imagem de cores de entrada que deve ser mapeada nas linhas de entrada.

## Conectores de saída

<b>Cor</b> *Tons de cinza* Resultado do mapeamento da imagem colorida de entrada pelas linhas sobre o plano de fundo como uma imagem colorida.

<b>Height</b> *Tons de cinza* O height das splines mapeadas através delas, como uma imagem em tons de cinza.

<b>UV</b> *Cor* Os UVs (isto é, as coordenadas) da imagem mapeada, codificados nos canais vermelho (U) e verde (V) de uma imagem colorida.

<b>Máscara</b> *Tons de cinza* Uma máscara do mapeamento nas linhas.

## Parâmetros

<b>Valor de Segmentos</b> *Inteiro* As splines são simplificadas em segmentos antes que as coordenadas da imagem os atravessem.\
Uma quantidade maior de segmentos resulta em um mapeamento mais suave ao longo das curvas.

<b>Reduzir Ampliação de UVs</b> *Booleano* Ajusta o método usado para interpolar as coordenadas da imagem de uma spline para a próxima para minimizar o alongamento quando a distância entre as splines é irregular.

<b>Escala UV</b> *Flutuante2* Ajusta a escala das coordenadas da imagem. Valores mais altos resultam em uma imagem ladrilhada mais densa.

<b>Rotação UV</b> *Flutuar* Gira as coordenadas da imagem em torno de seu centro.

<b>Cor do plano de fundo</b> *Flutuante4* A cor do plano de fundo na imagem de saída.

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineBridgeMapperGrayscale-Variant1-Before.jpg" alt="SplineBridgeMapperGrayscale-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineBridgeMapperColor-Variant1-After.jpg" alt="SplineBridgeMapperColor-Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](../../../../../../assets/SplineBridgeMapperColor-Demo.gif "Exemplo de nó 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 1](../../../../../../assets/SplineBridgeMapperColor-Variant1-After1.jpg "Exemplo de nó 1")

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](../../../../../../assets/SplineBridgeMapperColor-Graph.jpg "Exemplo de nó 2")

</td>
</tr>
</table>
