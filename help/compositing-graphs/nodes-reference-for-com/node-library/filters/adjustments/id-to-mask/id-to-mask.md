---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/id-to-mask.html"
breadcrumb-title: ''
description: Use o nó ID para máscara de tons de cinza para converter valores de mapa de ID em máscaras de tons de cinza para seleção de material.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > ID To Mask Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ID para mascarar tons de cinza
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7f15827b198bfbc133601581dc54ed894e98d89d
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---


# ID para mascarar tons de cinza

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone Identificar para Mascarar Tons de Cinza](id-to-mask.resources/IDToMask.png "ícone Identificar para Mascarar Tons de Cinza"){width="200px"}

<b>Entrada:</b> Filtros > Ajustes

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Cria uma máscara a partir de um mapa de ID em que os pixels com os valores de pixel selecionados são brancos.

Um mapa de ID é uma imagem na qual os pixels que fazem parte de um todo (por exemplo, uma forma) têm o mesmo valor de identificação exclusivo. Nesse caso, o valor é um inteiro.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>ID</b> <i>Tons de cinza</i> PRIMÁRIO | O mapa de ID de entrada do qual uma máscara deve ser extraída. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Saída</b> <i>Tons de cinza</i> | A máscara binária extraída do mapa de ID de entrada. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Modo de seleção</b> *Inteiro* | O método de selecionar os valores de pixel no mapa de ID que devem ser brancos na máscara:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Isolar:</b> selecione um único valor de pixel</li> <li data-preserve-html="true"><b>Intervalo:</b> selecione um intervalo de valores de pixel</li> </ul> |
| <b>Inteiro de ID</b> *Inteiro* *Disponível quando o &#39;Modo de seleção&#39; está definido como &#39;Individual&#39;* | O valor de pixel no mapa de ID que deve ser branco na máscara de saída. |
| <b>Intervalo de ID</b> *Inteiro2* *Disponível quando o &#39;Modo de seleção&#39; está definido como &#39;Intervalo&#39;* | O intervalo de valores de pixel no mapa de ID, do início ao fim, que deve ser branco na máscara de saída. |

## Exemplos

<table>
  <tr>
    <td>
      <img src="id-to-mask.resources/id_to_mask_grayscale_example_1_before.jpg" alt="id_to_mask_grayscale_example_1_before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="id-to-mask.resources/id_to_mask_grayscale_example_1_after.jpg" alt="id_to_mask_grayscale_example_1_after">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ID para máscara: Exemplo 2](id-to-mask.resources/id_to_mask_example_2.gif "ID para máscara: Exemplo 2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![ID para máscara: Exemplo 3](id-to-mask.resources/id_to_mask_example_3.png "ID para máscara: Exemplo 3"){zoomable="yes"}

</td>
</tr>
</table>
