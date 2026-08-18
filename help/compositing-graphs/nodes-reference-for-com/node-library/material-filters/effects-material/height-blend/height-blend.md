---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/height-blend.html"
breadcrumb-title: ''
description: Use o nó Mesclagem de Height para mesclar texturas com base em mapas de height a fim de criar transições de material realistas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mesclagem de height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Mesclagem de height

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-blend.png){width="128px"}

## Mesclagem de height

**Entrada:** *Filtros/Efeitos de Material*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Combina dois mapas de altura com base nas informações do height. Gera um mapa de altura mesclado, mas também uma máscara em preto e branco que pode ser usada em outro lugar.

Isso é útil quando você tem dois mapas de altura de alta qualidade para combinar, mas não necessariamente um material completo, como é necessário para a [Mesclagem de Height de material](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/material-height-blend/material-height-blend.md).

## Parâmetros

### Entradas

* **Parte Superior do Height**: *Entrada em Tons de Cinza*
* **Parte Inferior do Height**: *Entrada em Tons de Cinza*
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Deslocamento de Height**: *0.0 - 1.0* Desloca mapas de altura para que o nível de mesclagem seja movido ao longo do eixo de height. Esse é o principal controle da mesclagem.
* **Contraste**: *0.0 - 1.0*\
  Ajusta o contraste da mesclagem, torna as transições mais nítidas.
* **Modo**: *height Equilibrado, Prioridade de height inferior* Alterna entre dois modos de mesclagem diferentes.
* **Opacidade**: *0.0 - 1.0*\
  Mesclando a Opacidade do height de primeiro plano, ela aparece ou desaparece gradualmente.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
