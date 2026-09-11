---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dripping-rust.html"
breadcrumb-title: ''
description: Use o nó Ferrugem de gotejamento para gerar padrões de gotejamento de ferrugem com base na geometria da malha e na direção da gravidade.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dripping Rust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ferrugem de gotejamento
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 7%

---


# Ferrugem de gotejamento

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dripping-rust.resources/dripping-rust.png){width="128px"}

<b>Entrada:</b> Geradores > Geradores de máscara Baseados em Malha

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara representa lascas e manchas de ferrugem, com vazamentos diminuindo.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Entrada em tons de cinza</i> | Mapa feito bake ou gerado para ajudar com o posicionamento das ferrugens. |
| <b>Oclusão de ambiente</b> <i>Entrada em tons de cinza</i> | Mapa feito bake ou gerado para ajudar com o posicionamento das ferrugens. |
| <b>Posição</b> <i>Entrada em tons de cinza</i> | Mapa feito bake ou gerado para direções de gotejamento. |
| <b>Máscara (opcional)</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Propagação de Ferrugem</b> <i>0.0 - 1.0</i> | Controle principal para a quantidade de ferrugem. |
| <b>Contraste de Ferrugem</b> <i>0.0 - 1.0</i> | Define a quantidade de contraste nas manchas de ferrugem geradas (não afeta as gotas). |
| <b>Espalhando Smoothness</b> <i>0.0 - 1.0</i> | Quantidade de efeito de desfoque/mancha a ser aplicada às manchas de ferrugem. |
| <b>Intensidade de gotas</b> <i>0.0 - 1.0</i> | Define a intensidade e o comprimento das gotas de manchas. |
| <b>Smoothness de gotas</b> <i>0.0 - 1.0</i> | Quantidade de desfoque e suavização a ser aplicada a gotas. |
| <b>Quantidade de Amostras de Gotas</b> <i>0 - 32</i> | Define o nível de qualidade (etapas) do efeito gotas. Tem um pequeno efeito na velocidade. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dripping-rust.resources/dripping-rust-ex3.gif" />
        </td>
    </tr>
</table>
