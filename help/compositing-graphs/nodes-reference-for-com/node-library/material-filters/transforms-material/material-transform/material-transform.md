---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/transforms-material/material-transform.html"
breadcrumb-title: ''
description: Use o nó Transformação de material para aplicar transformações às saídas de material, incluindo rotação, escala e deslocamento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Transforms (Material) > Material Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformação de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---


# Transformação de material

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-transform.resources/material-transforms.png){width="128px"}

<b>Em:</b> Filtros Materiais > Transformas

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

A transformação de material é simplesmente a versão de materiais “multicanal” do [nó 2D de transformação atômica](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Ele transforma todos os canais de um material de entrada ao mesmo tempo, com a mesma interface que o Transform 2D.

Apenas certifique-se de configurar os canais corretamente! Por padrão, as opções Metálico/Aspereza e Specular/Textura reluzente estão ativadas, o que pode levar a alguma confusão.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Transformação</b> <i>(Matriz de Transformação)</i> | Gira e dimensiona o resultado. A movimentação/deslocamento é feita por meio do parâmetro Deslocamento |
| <b>Deslocamento</b> <i>-0.5 - 0.5</i> | Move ou traduz o resultado. Quando o controle de Transformação está presente, o resultado pode ser modificado por meio da interação direta com a tela. |
| <b>Formato Normal</b> | Escolha entre os formatos DirectX e OpenGL (vire o verde). |
| <b>Canais</b> | Ative e desative os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza. |
