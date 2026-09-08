---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/cloth-wear.html"
breadcrumb-title: ''
description: Use o nó Desgaste de pano para gerar máscaras de desgaste em superfícies de pano com base na curvatura da malha e nas áreas de contato.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Cloth Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desgaste de pano
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---


# Desgaste de pano

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/cloth-wear.png){width="128px"}

<b>Entrada:</b> Geradores > Geradores de máscara Baseados em Malha

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

A máscara representa bordas congeladas em materiais de tecido. Ele usa um mapa de altura de detalhe de pano que determina a maior parte da aparência; sem um mapa apropriado, o efeito parece muito básico.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Height de pano</b> <i>Entrada em tons de cinza</i> | Height somente para o padrão de tecido. Esse não é o height do objeto (feito bake), mas sim um padrão de detalhes lado a lado. |
| <b>Máscara (opcional)</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |
| <b>Curvatura</b> <i>Entrada em tons de cinza</i> | Curvatura feita bake/gerada para determinar arestas elevadas. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Quantidade de bordas sólidas</b> <i>0.0 - 1.0</i> |  |
| <b>Usar Suavidade</b> <i>0.0 - 5.0</i> | Determina o nível de desfoque/suavidade das bordas gastas. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/cloth-wear-ex.gif" />
        </td>
    </tr>
</table>
