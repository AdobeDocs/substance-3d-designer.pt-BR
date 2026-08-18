---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-normal-blender.html"
breadcrumb-title: ''
description: Use o nó Mesclador normal de Height para mesclar mapas normais e de height para combinar informações detalhadas da superfície.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height Normal Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Misturador normal do height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Misturador normal do height

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-normal-blender.png){width="128px"}

## Misturador normal do height

**Entrada:** *Filtros/Mapa Normal*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Um nó de atalho que mescla um Heightmap em tons de cinza em um Normalmap. A entrada do Height é convertida internamente em um Normalmap e, em seguida, mesclada corretamente com a entrada Normal.

Essa é uma maneira mais rápida de mesclar detalhes do que fazer isso manualmente com nós separados, mas você pode perceber que não há controle e refinamento para determinadas necessidades.

## Parâmetros

### Entradas

* **Height**: *Entrada em Tons de Cinza*\
  Tons de cinza com os quais mesclar.
* **Normal**: *Entrada De Cores*\
  Base Normalmap para mesclagem.

### Parâmetros

* **Intensidade normal**: *0.0 - 16.0* Intensidade da conversão normal da entrada do Height.
* **Formato Normal**: *DirectX, OpenGL*\
  Alterna entre diferentes formatos de Mapas Normais (inverte o canal verde).

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
