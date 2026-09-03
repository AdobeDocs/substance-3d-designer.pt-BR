---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dirt.html"
breadcrumb-title: ''
description: Use o nó Dirt para gerar máscaras de acúmulo de dirt com base na curvatura, posição e oclusão da malha.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Terra
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 7%

---


# Terra

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dirt.resources/dirt-01.png){width="128px"}

<b>Entrada:</b> Geradores > Geradores de máscara Baseados em Malha

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara representa dirt em bordas e cantos ocultos e afundados, com base no AO e na curvatura feitos bake.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Curvatura</b> <i>Entrada em tons de cinza</i> | Mapa baked usado para efeitos internos e mascaramento. Obrigatório! |
| <b>Oclusão de ambiente</b> <i>Entrada em tons de cinza</i> | Mapa baked usado para efeitos internos e mascaramento. Obrigatório! |
| <b>Entrada de Desgaste</b> <i>Entrada em tons de cinza</i> | Entrada do mapa de desgaste personalizado, opcional, ativada por parâmetro. |
| <b>Máscara (opcional)</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |
| <b>Espaço Mundial Normal</b> <i>Entrada de cores</i> | Usado apenas para Triplanar. |
| <b>Posição</b> <i>Entrada de cores</i> | Usado apenas para Triplanar. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Nível de Dirt</b> <i>0.0 - 1.0</i> | Controle principal para a quantidade de dirt. |
| <b>Contraste de Dirt</b> <i>0.0 - 1.0</i> | Controla o contraste principal da dirt na máscara. |
| <b>Valor do Desgaste</b> <i>0.0 - 1.0</i> | Define o quão sujo o dirt é. Defina como 0 para um dirt perfeitamente suave. |
| <b>Mascaramento de bordas</b> <i>0.0 - 1.0</i> | Quantidade de dirt a ser removida das bordas elevadas (com base no mapa de curvatura). |
| <b>Usar Desgaste Personalizado</b> <i>Falso/Verdadeiro</i> | Habilita o uso da entrada do mapa de desgaste personalizado em vez do Desgaste interno. |
| <b>Escala de Desgaste</b> <i>1 - 16</i> | Define a escala lado a lado do detalhe de Desgaste. |
| <b>Usar Triplanar</b> <i>Falso/Verdadeiro</i> | Use a [projeção triplanar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) para mapeamento de Desgaste e remova costuras. |
| <b>Contraste de Mesclagem Triplanar</b> <i>0.001 - 1.0</i> | Define o contraste da projeção Triplanar. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dirt.resources/dirt-02.gif" />
        </td>
    </tr>
</table>
