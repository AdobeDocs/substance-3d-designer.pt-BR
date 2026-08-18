---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-transform.html"
breadcrumb-title: ''
description: Use o nó Transformação normal para aplicar transformações a mapas normais, preservando as direções vetoriais corretamente.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformação normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# Transformação normal

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-transform.png){width="128px"}

## Transformação normal

**Entrada:** *Filtros/Mapa Normal*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Semelhante ao nó 2D de Transformação atômica, isso permite a transformação de Normalmaps sem quebrar o espaço Tangent, em vez disso, é recalculado na hora, resultando em Normalmaps sempre corretos.

## Parâmetros

* **Matrix2x2**: *(Matriz de Transformação):*\
  Gire ou dimensione a entrada.
* **Deslocamento**: *-0.5 - 0.5*\
  Move ou traduz o resultado. Quando o controle de Transformação está presente, o resultado pode ser modificado ao interagir diretamente com a tela.
* **Formato Normal**: *DirectX, OpenGL*\
  Alternar entre Formatos de mapa normais diferentes (inverte o canal verde)

</td>
</tr>
</table>
