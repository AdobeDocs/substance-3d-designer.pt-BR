---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-vector-rotation.html"
breadcrumb-title: ''
description: Use o nó Rotação de vetor normal para girar vetores de mapa normais para ajustar a iluminação da superfície e a orientação dos detalhes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Vector Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rotação de vetor normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# Rotação de vetor normal

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-vector-rotation.png){width="128px"}

## Rotação de vetor normal

**Entrada:** *Filtros/Mapa Normal*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Nó utilitário normal que gira todos os vetores de um Normalmap de entrada no espaço Tangent. Na verdade, não transforma os pixels, em vez disso, modifica os valores que eles representam. Ele pode usar um mapa opcional para adicionar rotações aleatórias a facetas em tons de cinza.

## Entradas

* **Normal**: *Entrada De Cores*\
  Mapa base no qual executar rotação. Obrigatório.
* **Mapa de rotação (opcional)**: *Entrada em tons de cinza*\
  Mapa em tons de cinza que modula a Intensidade da rotação.

## Parâmetros

* **Ângulo de Rotação**: *0.0 - 1.0*\
  Define o ângulo pelo qual girar o mapa normal
* **Formato Normal**: *DirectX, OpenGL*\
  Alternar entre Formatos de mapa normais diferentes (inverte o canal verde)

## Exemplos

</td>
</tr>
</table>
