---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leather-wear.html"
breadcrumb-title: ''
description: Use o nó Desgaste de couro para gerar máscaras de desgaste em superfícies de couro com base na curvatura da malha e nos pontos de contato.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leather Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desgaste de couro
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 5%

---


# Desgaste de couro

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](leather-wear.resources/leather-wear-01.png){width="128px"}

<b>Entrada:</b> Geradores > Geradores de máscara Baseados em Malha

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara representa um desgaste com um padrão de couro, com mais desgaste nas bordas com base na curvatura. É semelhante à [Edge Wear de vidro de fibra](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear/fiber-glass-edge-wear.md) em funcionalidade e tem, em sua maioria, os mesmos parâmetros.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Entrada em tons de cinza</i> | Mapa baked usado para o posicionamento de bordas. Obrigatório! |
| <b>Oclusão de ambiente</b> <i>Entrada em tons de cinza</i> | Mapa baked usado para ocultar determinadas áreas. Recomendado, mas não obrigatório. |
| <b>Entrada de Desgaste</b> <i>Entrada em tons de cinza</i> | Slot de entrada opcional do mapa de Desgaste que pode ser alternado pelo parâmetro “Usar Desgaste personalizado”. |
| <b>Máscara (opcional)</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Nível de desgaste</b> <i>0.0 - 1.0</i> | Define o nível de desgaste global, revelando gradualmente. |
| <b>Usar Contraste</b> <i>0.0 - 1.0</i> | Define o contraste do efeito. |
| <b>Valor do Desgaste</b> <i>0.0 - 1.0</i> | Define a quantidade de desgaste (padrão de couro) a ser mesclada entre as bordas. |
| <b>Mascaramento de Oclusão de ambiente</b> <i>0.0 - 1.0</i> | Define a extensão em que o AO mascara os efeitos de desgaste. |
| <b>Espessura da Curvatura</b> <i>0.0 - 1.0</i> | Define a extensão em que as bordas da curvatura afetam o resultado final. Mesmo se definido como 0, você ainda precisa de um mapa de curvatura. |
| <b>Usar Desgaste Personalizado</b> <i>Falso/Verdadeiro</i> | Permite a substituição do padrão de couro incorporado. Em vez disso, use um slot de entrada personalizado. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="leather-wear.resources/leather-wear-02.gif" />
        </td>
    </tr>
</table>
