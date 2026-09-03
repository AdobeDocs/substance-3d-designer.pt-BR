---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-uncombine.html"
breadcrumb-title: ''
description: Use o nó Descombinar normal para separar dados de mapa normal combinados em componentes X, Y e Z individuais.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal map > Normal uncombine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Não Combinar Normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 2%

---


# Não Combinar Normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de descombinação normal](normal-uncombine.resources/normal-uncombine-01.png "Ícone de descombinação normal"){width="200px"}

<b>Entrada:</b> Filtros > Mapa normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Remove de um mapa normal os detalhes da superfície descritos por um mapa de height.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Combinado normal</b> <i>Cor</i> PRIMÁRIA | O mapa normal do qual os detalhes devem ser removidos. |
| <b>Height</b> <i>Tons de cinza</i> | O mapa de heights que representa os detalhes da superfície que devem ser removidos do mapa normal combinado. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Não combinado normal</b> <i>Cor</i> | O mapa normal onde os detalhes da superfície descritos pelo mapa de height de entrada foram removidos. |
| <b>Intensidade estimada</b> <i>Flutuante</i> | Uma estimativa da intensidade que deve ser definida para um nó [Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) conectado ao mapa de height de entrada, para corresponder à intensidade do mapa normal de entrada. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Formato normal</b> *Inteiro* | O formato do mapa normal de entrada. Inverte efetivamente o canal de verde.<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX:</b> o eixo Y aponta para cima</li> <li data-preserve-html="true"><b>OpenGL:</b> o eixo Y aponta para baixo</li> </ul> |

## Exemplos

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-02.jpg" alt="normal_uncombine_example_3_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-03.jpg" alt="normal_uncombine_example_3_after">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

![Normal não combinado: Exemplo 2](normal-uncombine.resources/normal-uncombine-04.png "Normal não combinado: Exemplo 2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-05.jpg" alt="normal_uncombine_example_1_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-06.jpg" alt="normal_uncombine_example_1_after">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

![Normal não combinado: Exemplo 4](normal-uncombine.resources/normal-uncombine-07.png "Normal não combinado: Exemplo 4"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-08.jpg" alt="normal_uncombine_example_2_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-09.jpg" alt="normal_uncombine_example_2_after">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

![Normal não combinado: Exemplo 6](normal-uncombine.resources/normal-uncombine-10.png "Normal não combinado: Exemplo 6"){zoomable="yes"}
