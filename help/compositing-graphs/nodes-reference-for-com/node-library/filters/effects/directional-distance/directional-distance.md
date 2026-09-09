---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/directional-distance.html"
breadcrumb-title: ''
description: Use o nó Distância direcional para calcular campos de distância em direções específicas para efeitos de procedimento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Directional distance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Distância direcional
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5c9ae53c1de18b1c09789a480cba6b1d70bd350d
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---


# Distância direcional

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone Anisotrópico de Escala de Cinza Kuwahara](directional-distance.resources/directional_distance.png "Ícone Anisotrópico de Escala de Cinza Kuwahara"){width="200px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Desenha um gradiente de distância a partir das bordas de uma máscara em uma direção especificada.

Os gradientes sobrepostos são classificados por distância normalizada invertida para que a distância até a borda mais próxima seja desenhada.

A distância do gradiente pode ser ajustada dinamicamente ao longo da borda usando um mapa de distância.

</td>
</tr>
</table>

>[!TIP]
>
> O nó [Suavização de chanfro](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/bevel-smooth/bevel-smooth.md) oferece recursos semelhantes, em que a dilatação é executada em todas as direções.

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Tons de cinza</i> PRIMÁRIO | A imagem da qual a máscara deve ser extraída.   Todos os valores acima de 0,5 são brancos nessa máscara. |
| <b>Mapa de distância</b> <i>Tons de cinza</i> | Uma entrada opcional usada quando o valor do parâmetro &#39;Mapa de distância Multiplier&#39; é maior que 0.   É usado para ajustar a distância de chanfro/dilatação ao longo das bordas da máscara, onde um valor mais escuro resulta em uma distância mais curta. |
| <b>Mapa de ângulo</b> <i>Tons de cinza</i> | Uma entrada opcional usada quando o valor do parâmetro &#39;Angle Map Multiplier&#39; é maior que 0.   É usado para ajustar a direção do gradiente de distância adicionando seu valor ao ângulo de direção, em número de voltas.   O parâmetro &#39;Deslocamento do mapa de ângulo&#39; permite remapear os valores especificando qual valor é 0. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Saída</b> <i>Tons de cinza</i> | A imagem resultante de acordo com o &#39;Modo de saída&#39; selecionado. |
| <b>UV</b> <i>Cor</i> | Um mapa de UV em que os UVs são dilatados das bordas da máscara ao longo da direção especificada.   Isso pode ser conectado a um nó [Mapeador UV](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-color/uv-mapper-color.md) para mapear qualquer outra imagem usando esses UVs dilatados. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Modo de saída</b> *Inteiro* | O método de desenhar o gradiente de distância das bordas da máscara:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Distância Normalizada Invertida:</b> um gradiente de 1 a 0, em que 0 é atingido na &#39;Distância Máxima&#39;, multiplicado pelo &#39;Mapa de distância&#39;, se conectado</li> <li data-preserve-html="true"><b>Distância:</b> um gradiente de valores de distância brutos da borda da máscara, onde 1 é o comprimento do lado mais curto da imagem de entrada</li> </ul> |
| <b>Distância máxima</b> *Flutuante* | A distância percorrida pelo gradiente de distância, no espaço normalizado da imagem, em que 1 é o comprimento do lado mais curto da imagem de entrada. |
| <b>Ângulo</b> *Flutuante* | A direção do gradiente de distância em número de voltas, onde 0 é horizontal e à direita - ou seja, um vetor (1,0). |
| <b>Multiplicador de Mapa de distância</b> *Flutuante* | Ajusta o impacto do &#39;Mapa de distância&#39; sobre a &#39;Distância máxima&#39;.   Observação: este parâmetro não tem efeito quando a entrada &#39;Mapa de distância&#39; não está conectada. |
| <b>Multiplicador de mapa de ângulo</b> *Flutuante* | Ajusta o impacto do “Mapa de ângulo” sobre o “Ângulo”. |
| <b>Deslocamento do mapa de ângulos</b> *Flutuante* | Mapeia novamente os valores no “Mapa de ângulo” especificando qual valor nesse mapa deve ser 0.   Por exemplo, um deslocamento de 0,5 significa que um valor de 0,75 é 0,25 voltas, e um valor de 0,3 é -0,2 voltas. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="directional-distance.resources/directional_distance_example_1_before.jpg" alt="directional_distance_example_1_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional_distance_example_1_after.jpg" alt="directional_distance_example_1_after">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="directional-distance.resources/directional_distance_example_3_before.jpg" alt="directional_distance_example_3_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional_distance_example_3_after.jpg" alt="directional_distance_example_3_after">
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

<table>
  <tr>
    <td>
      <img src="directional-distance.resources/directional_distance_example_2_before.jpg" alt="directional_distance_example_2_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional_distance_example_2_after.jpg" alt="directional_distance_example_2_after">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="directional-distance.resources/directional_distance_example_5_before.jpg" alt="directional_distance_example_5_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional_distance_example_5_after.jpg" alt="directional_distance_example_5_after">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
  <tr>
    <td>
      <img src="directional-distance.resources/directional_distance_example_4_before.jpg" alt="directional_distance_example_4_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="directional-distance.resources/directional_distance_example_4_after.jpg" alt="directional_distance_example_4_after">
      <br><i>Depois</i>
    </td>
  </tr>
</table>
