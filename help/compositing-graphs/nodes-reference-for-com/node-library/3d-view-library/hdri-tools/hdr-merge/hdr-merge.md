---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/hdr-merge.html"
breadcrumb-title: ''
description: Use o nó Mesclagem por HDR para mesclar várias imagens de HDR em um único panorama para criar mapas de ambiente composto.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > HDR Merge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mesclar HDR
user-guide-description: ''
user-guide-title: ''
source-git-commit: 43dd5433948c89f68426040a2a2d76282072c75d
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 13%

---


# Mesclar HDR

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/hdr-merge.png){width="200px"}

<b>Entrada:</b> Visualização 3D > Ferramenta HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Mescle várias exposições fotográficas para criar uma imagem de Intervalo dinâmico. A primeira entrada é a imagem mais subexposta.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada 1-16</b> <i>Entrada de cores</i> | Imagens de entrada. O valor disponível depende do parâmetro. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Entradas</b> <i>2 - 16</i> | Define a quantidade de entradas disponíveis. |
| <b>Delta De Exposição (EV)</b> <i>0.0 - 4.0</i> | Define a diferença na exposição para interpretar entre imagens. |
| <b>Ponto branco</b> <i>0.0 - 13.0</i> | Defina ponto branco para executar alguns ajustes no resultado final. |
