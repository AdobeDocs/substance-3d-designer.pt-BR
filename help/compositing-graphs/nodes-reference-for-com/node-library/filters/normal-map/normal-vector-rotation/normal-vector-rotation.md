---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-vector-rotation.html"
breadcrumb-title: ''
description: Use o nó Rotação de vetor normal para girar vetores de mapa normal para ajustar a iluminação de superfície e a orientação dos detalhes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Vector Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rotação de vetor normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 5%

---


# Rotação de vetor normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-vector-rotation.resources/normal-vector-rotation-01.png){width="128px"}

<b>Entrada:</b> Filtros > Mapa normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Nó utilitário normal que gira todos os vetores de um Normalmap de entrada no espaço Tangent. Na verdade, não transforma pixels. Em vez disso, modifica os valores que eles representam. Ele pode usar um mapa opcional para adicionar rotações aleatórias a facetas em tons de cinza.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Normal</b> <i>Entrada de cores</i> | Mapa base no qual executar rotação. Obrigatório. |
| <b>Mapa de rotação (opcional)</b> <i>Entrada em tons de cinza</i> | Mapa em tons de cinza que modula a Intensidade da rotação. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Ângulo de rotação</b> <i>0.0 - 1.0</i> | Define o ângulo pelo qual girar o mapa normal |
| <b>Formato Normal</b> <i>DirectX, OpenGL</i> | Alternar entre Formatos de mapa normais diferentes (inverte o canal verde) |
