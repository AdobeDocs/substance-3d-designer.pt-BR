---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-wear.html"
breadcrumb-title: ''
description: Use o nó Edge Wear para gerar máscaras de desgaste nas bordas da malha a fim de criar efeitos realistas de danos nas bordas e de intemperismo.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 7%

---


# Edge Wear

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/edge-wear.png){width="128px"}

<b>Entrada:</b> Geradores > Geradores de máscara Baseados em Malha

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Este nó representa desgaste nas bordas do objeto. Tem alguns parâmetros, mas não é o mais fácil de usar: recomendamos que você brinque e tenha uma ideia das coisas. O nó é bastante poderoso, embora nenhuma máscara de substituição personalizada possa ser feita.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Entrada em tons de cinza</i> | Mapa baked usado para efeitos internos e mascaramento |
| <b>Máscara (opcional)</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Nível</b> <i>0.0 - 1.0</i> | Define a propagação total do efeito. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta o contraste do resultado. |
| <b>Limite</b> <i>0.0 - 1.0</i> | Semelhante ao Nível, define a propagação total do efeito. |
| <b>Largura das Bordas</b> <i>0.0 - 1.0</i> | Define a plenitude do efeito de realce. Reduza para torná-los mais dispersos. |
| <b>Desordem</b> <i>0.0 - 1.0</i> | Define a quantidade de ruído a ser mesclada para quebrar o smoothness. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/edge-wear-ex.gif" />
        </td>
    </tr>
</table>
