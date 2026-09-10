---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-grayscale.html"
breadcrumb-title: ''
description: Use o nó Tons de cinza do mapeador da ponte de spline para fazer a ponte de texturas entre duas splines com o mapeamento de tons de cinza.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mapeador da ponte de spline em tons de cinza
user-guide-description: ''
user-guide-title: ''
source-git-commit: 86e504c9dfe76516c56a7950f0bf70090270a60c
workflow-type: tm+mt
source-wordcount: '370'
ht-degree: 1%

---


# Mapeador da ponte de spline em tons de cinza

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](spline-bridge-mapper-grayscale.resources/spline-bridge-mapper-grayscale-icon.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Mapeia uma imagem em tons de cinza em uma lista de splines de entrada para que a imagem atravesse as splines na ordem.

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
> Consulte também [Cor do mapeador da ponte de spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-col/spline-bridge-mapper-color.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Cordas de spline</b> <i>Cor</i> | As coordenadas dos pontos das linhas divisórias de entrada codificadas nos canais RGBA de uma imagem colorida:<br><b>R</b> - Posição X<br><b>G</b> - Posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br>- Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> <i>Cor</i> | Dados adicionais das splines de entrada codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usadas<br><b>A</b> - Não Usadas |
| <b>Valor da spline</b> <i>Inteiro</i> | O número de splines de entrada. |
| <b>Mapa de cores</b> <i>Tons de cinza</i> | A imagem em tons de cinza de entrada que deve ser mapeada nas splines de entrada. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Cor</b> <i>Tons de cinza</i> | O resultado do mapeamento da imagem da Cor de entrada nas linhas, como uma imagem em tons de cinza. |
| <b>Height</b> <i>Tons de cinza</i> | O height dos splines mapeados através deles, como uma imagem em tons de cinza. |
| <b>UV</b> <i>Cor</i> | Os UVs (isto é, coordenadas) da imagem mapeada, codificados nos canais vermelho (U) e verde (V) de uma imagem colorida. |
| <b>Máscara</b> <i>Tons de cinza</i> | Uma máscara do mapeamento através das splines. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Valor de Segmentos</b> <i>Inteiro</i> | As splines são simplificadas em segmentos antes que as coordenadas da imagem os atravessem. Uma quantidade maior de segmentos resulta em um mapeamento mais suave ao longo das curvas. |
| <b>Reduzir Ampliação de UVs</b> <i>Booleano</i> | Ajusta o método usado para interpolar as coordenadas da imagem de uma spline para a próxima para minimizar o esticamento quando a distância entre as splines for irregular. |
| <b>Escala UV</b> <i>Flutuante2</i> | Ajusta a escala das coordenadas da imagem. Valores mais altos resultam em uma imagem ladrilhada mais densa. |
| <b>Rotação UV</b> <i>Flutuante</i> | Gira as coordenadas da imagem em torno do centro. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-bridge-mapper-grayscale.resources/SplineBridgeMapperGrayscale-Variant1-Before.jpg" alt="SplineBridgeMapperGrayscale-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-bridge-mapper-grayscale.resources/SplineBridgeMapperGrayscale-Variant1-After.jpg" alt="SplineBridgeMapperGrayscale-Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](spline-bridge-mapper-grayscale.resources/SplineBridgeMapper-Demo.gif "Exemplo de nó 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 1](spline-bridge-mapper-grayscale.resources/SplineBridgeMapperGrayscale-Variant1-After1.jpg "Exemplo de nó 1")

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](spline-bridge-mapper-grayscale.resources/SplineBridgeMapperGrayscale-Graph.jpg "Exemplo de nó 2")

</td>
</tr>
</table>
