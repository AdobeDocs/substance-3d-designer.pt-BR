---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/grease.html"
breadcrumb-title: ''
description: Use o nó Graxa para gerar máscaras de acumulação de graxa com base na geometria da malha e nas áreas de contato.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Grease
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Graxa
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 5%

---


# Graxa

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/grease.png){width="128px"}

<b>Entrada:</b> Geradores > Geradores de máscara Baseados em Malha

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara destina-se especificamente a faces de caracteres e outras áreas específicas. Gera um tipo de máscara de graxa de pele em áreas de baixo thickness.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Thickness</b> <i>Entrada em tons de cinza</i> | Mapa de Espessura feito bake no qual o efeito inteiro se baseia. Obrigatório! |
| <b>Ruído</b> <i>Entrada em tons de cinza</i> | Mapa de ruído opcional para substituir o desgaste de graxa. |
| <b>Máscara (opcional)</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Nível</b> <i>0.0 - 1.0</i> | Define a quantidade total de efeito a ser exibida. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta o contraste do resultado. |
| <b>Limite de Thicknesss</b> <i>0.0 - 1.0</i> | Define um thickness mínimo no qual o efeito deve aparecer. Igualmente importante como o Nível; ajuste-o para se ajustar ao seu mapa de Espessura. |
| <b>Substituir Ruído</b> <i>Falso/Verdadeiro</i> | Defina para substituir o mapa de desgaste de graxa interno pelo slot de entrada personalizado. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/grease-ex.gif" />
        </td>
    </tr>
</table>
