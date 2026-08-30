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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 5%

---


# Mesclagem de height

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-blend.resources/height-blend.png){width="128px"}

<b>Em:</b> Filtros Materiais > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Combina dois mapas de altura com base nas informações do height. Gera um mapa de altura mesclado, mas também uma máscara em preto e branco que pode ser usada em outro lugar.

Isso é útil quando você tem dois mapas de altura de alta qualidade para combinar, mas não necessariamente um material completo, como é necessário para a [Mesclagem de Height de material](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/material-height-blend/material-height-blend.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Height Superior</b> <i>Entrada em tons de cinza</i> |  |
| <b>Parte Inferior do Height</b> <i>Entrada em tons de cinza</i> |  |
| <b>Máscara (opcional)</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Deslocamento de Height</b> <i>0.0 - 1.0</i> | Desloca mapas de altura para que o nível de mesclagem seja movido ao longo do eixo do height. Esse é o principal controle da mesclagem. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta o contraste da mesclagem, torna as transições mais nítidas. |
| <b>Modo</b> <i>height balanceado, prioridade de height inferior</i> |  |
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Mesclando a Opacidade do height de primeiro plano, ela aparece ou desaparece gradualmente. |
