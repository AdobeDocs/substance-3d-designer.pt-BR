---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/light.html"
breadcrumb-title: ''
description: Use o nó Luz para gerar máscaras com base nas condições de iluminação de malha a fim de criar variações de material realistas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luz
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 9%

---


# Luz

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](light.resources/light-01.png){width="128px"}

<b>Entrada:</b> Geradores > Geradores de máscara Baseados em Malha

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara é um pouco diferente de outros Geradores: ela faz puramente iluminação falsa, com base no World Space Normalmap, retornando uma máscara “lightmap” em preto e branco.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Ângulo Horizontal</b> <i>0.0 - 1.0</i> | Define o ângulo horizontal da luz falsa. |
| <b>Ângulo Vertical</b> <i>0.0 - 1.0</i> | Define o ângulo vertical da luz falsa. |
| <b>Brilho do destaque</b> <i>0.0 - 0.999</i> | Define a página espelhada invertida da área realçada. |
| <b>Nível de realce</b> <i>0.0 - 1.0</i> | Define o nível de brilho da área realçada. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="light.resources/light-02.gif" />
        </td>
    </tr>
</table>
