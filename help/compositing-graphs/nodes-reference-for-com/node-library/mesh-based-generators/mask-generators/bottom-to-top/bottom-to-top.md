---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/bottom-to-top.html"
breadcrumb-title: ''
description: Use o nó De baixo para cima para gerar máscaras de gradiente de baixo para cima com base na posição do mundo da malha.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Bottom To Top
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: De baixo para cima
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 5%

---


# De baixo para cima

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/bottom-to-top.png){width="128px"}

<b>Entrada:</b> Geradores > Geradores de máscara Baseados em Malha

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras inteligentes](https://experienceleague.adobe.com/pt-br/docs/substance-3d-painter/using/features/smart-materials-and-masks) do [Painter](https://experienceleague.adobe.com/pt-br/docs/substance-3d-painter/using/home).

Isso gera uma transição de branco para preto da parte inferior para a parte superior de um modelo, útil para fazer falhas e seleções baseadas em geometria.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Posição</b> <i>Entrada de cores</i> | Mapa de Posição feito bake. Obrigatório! |
| <b>Aspereza</b> <i>Entrada em tons de cinza</i> | Isso não tem nada a ver com a rugosidade do PBR, mas é um mapa de variação (opcional) para quebrar a transição. Aparece somente quando a Aspereza está definida como maior que 0. |
| <b>Máscara (opcional)</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Nível</b> <i>0.0 - 1.0</i> | Desloca o nível médio do resultado entre preto ou branco, como um ajuste de brilho. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta o contraste da transição. |
| <b>Variação_Aspereza</b> <i>0.0 - 1.0</i> | Determina a quantidade do mapa de aspereza a ser mesclada para variação. Aumentar isso em 0 revela o slot do mapa. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/bottom-to-top-ex.gif" />
        </td>
    </tr>
</table>
