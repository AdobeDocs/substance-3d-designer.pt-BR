---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/paint-wear.html"
breadcrumb-title: ''
description: Use o nó Desgaste de Tinta para gerar máscaras de desgaste de tinta com base na geometria da malha para criar efeitos realistas de lascas de tinta.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Paint Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desgaste de tinta
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 6%

---


# Desgaste de tinta

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](paint-wear.resources/paint-wear-01.png){width="128px"}

<b>Entrada:</b> Geradores > Geradores de máscara Baseados em Malha

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara representa a lasca de tinta e o desgaste nas bordas.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Oclusão de ambiente</b> <i>Entrada em tons de cinza</i> | Mapa baked usado para efeitos internos e mascaramento. |
| <b>Curvatura</b> <i>Entrada em tons de cinza</i> | Mapa baked usado para efeitos internos e mascaramento. |
| <b>Máscara de Variação</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |
| <b>Máscara (opcional)</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Nível</b> <i>0.0 - 1.0</i> | Define a quantidade total de desgaste de tinta, revelando gradualmente. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta o contraste do resultado. |
| <b>Oclusão</b> <i>0.0 - 1.0</i> | Define a quantidade de efeito que o AO feito bake tem ao impedir o desgaste em áreas mais escuras. |
| <b>Raio</b> <i>0.0 - 2.0</i> | Define até onde o efeito de lasca se espalha a partir das bordas convexas. |
| <b>Variação</b> <i>0.0 - 1.0</i> | Defina o valor de variação (desgaste) para mesclar no efeito. |
| <b>Substituir máscara de variação</b> <i>Falso/Verdadeiro</i> | Habilita o slot de entrada do mapa de variação personalizada (desgaste). |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="paint-wear.resources/paint-wear-02.gif" />
        </td>
    </tr>
</table>
