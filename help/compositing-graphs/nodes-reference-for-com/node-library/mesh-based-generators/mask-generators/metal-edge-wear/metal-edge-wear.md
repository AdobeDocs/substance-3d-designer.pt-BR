---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/metal-edge-wear.html"
breadcrumb-title: ''
description: Use o nó Edge Wear de metal para gerar máscaras de desgaste em bordas de metal com base na curvatura e posição da malha.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Metal Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear de metal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 7%

---


# Edge Wear de metal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](metal-edge-wear.resources/metal-edge-wear-01.png){width="128px"}

<b>Entrada:</b> Geradores > Geradores de máscara Baseados em Malha

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara representa o desgaste de bordas em um objeto metálico, com arranhões e lascas aparecendo em bordas convexas elevadas, potencialmente mascaradas por áreas escuras feitas bake do AO.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Entrada em tons de cinza</i> | Mapa baked usado para efeitos internos e mascaramento. |
| <b>Oclusão de ambiente</b> <i>Entrada em tons de cinza</i> | Mapa baked usado para efeitos internos e mascaramento. |
| <b>Entrada de Desgaste</b> <i>Entrada em tons de cinza</i> |  |
| <b>Máscara (opcional)</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |
| <b>Espaço Mundial Normal</b> <i>Entrada de cores</i> |  |
| <b>Posição</b> <i>Entrada de cores</i> |  |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Nível de desgaste</b> <i>0.0 - 1.0</i> | Define a quantidade total de desgaste, revela gradualmente. |
| <b>Usar Contraste</b> <i>0.0 - 1.0</i> | Define o contraste do resultado final. |
| <b>Smoothness de bordas</b> <i>0.0 - 16.0</i> | Define o smoothness da queda das bordas da Curvatura. |
| <b>Valor do Desgaste</b> <i>0.0 - 1.0</i> | Define a quantidade de desgaste a ser mesclada entre as bordas. |
| <b>Escala de Desgaste</b> <i>1 - 16</i> | Define a escala do Desgaste. |
| <b>Mascaramento de Oclusão de ambiente</b> <i>0.0 - 1.0</i> | Define a quantidade de efeito que o AO tem no efeito final, com as áreas escuras sendo mascaradas. |
| <b>Espessura da Curvatura</b> <i>0.0 - 1.0</i> | Define a quantidade de efeito que as bordas convexas da curvatura têm no efeito final. |
| <b>Usar Desgaste Personalizado</b> <i>Falso/Verdadeiro</i> | Habilita um slot de entrada personalizado do mapa de Desgaste. |
| <b>Usar Triplanar</b> <i>Falso/Verdadeiro</i> | Habilite a projeção [Tripla Planar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) para ocultar costuras. |
| <b>Contraste de Mesclagem Triplanar</b> <i>0.0 - 1.0</i> | Define o contraste de mesclagem para a Projeção Triplanar. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="metal-edge-wear.resources/metal-edge-wear-02.gif" />
        </td>
    </tr>
</table>
