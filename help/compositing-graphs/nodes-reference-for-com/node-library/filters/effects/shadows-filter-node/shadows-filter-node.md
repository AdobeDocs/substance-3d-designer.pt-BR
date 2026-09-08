---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shadows-filter-node.html"
breadcrumb-title: ''
description: Use o nó do filtro Sombras para gerar efeitos de sombra das texturas de entrada para adicionar profundidade e realismo aos materiais.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shadows (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sombras (Nó de filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 8%

---


# Sombras (Nó de filtro)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/shadows-1.png){width="128px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma versão raw, somente em tons de cinza, do nó [Sombra Projetada de Forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-drop-shadow/shape-drop-shadow.md). Ela usa somente formas binárias em preto e branco como entrada e retorna apenas a sombra.

Pode ser útil se você estiver logo após a sombra e não quiser trabalhar com um nó mais completo, por exemplo, ao criar seu próprio material ou iluminação feita bake.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Distância da sombra</b> <i>0.0 - 1.0</i> | Controla a distância em que a sombra deve cair. |
| <b>Ângulo de luz</b> <i>0.0 - 1.0</i> | Controla o ângulo de incidência da luz. |
| <b>Suavidade das bordas</b> <i>0.0 - 1.0</i> | Determina a intensidade ou a suavidade das bordas das sombras. |
| <b>Amostras</b> <i>1 - 16</i> | Define a qualidade da configuração de Suavidade das bordas. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/shadow-ex.png" />
        </td>
    </tr>
</table>
