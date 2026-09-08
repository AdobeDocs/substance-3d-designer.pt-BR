---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-selector.html"
breadcrumb-title: ''
description: Use o nó Seletor de material para selecionar materiais com base em dados de malha para criar efeitos de textura multimateriais.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Selector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Seletor de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: fbf066c7185f74dcbf35156afc3873d192f77abc
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 5%

---


# Seletor de material

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/material-selector.png){width="128px"}

<b>Entrada:</b> Geradores Baseados Em Malha > Utilitários

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Converte um mapa de ID de cor completa em uma máscara binária, preta e branca. Permite a mesclagem e a combinação de diferentes cores em uma máscara.

Isso é útil se você não quiser usar o [Combinar de vários materiais](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md) e preferir usar a máscara manualmente ou, como alternativa, se quiser usar manualmente essas mesmas máscaras em outros locais.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Materiais</b> <i>1 - 16</i> | Define o número de materiais para os quais a combinação está habilitada. |
| <b>Habilitar material #1-16</b> <i>Falso/Verdadeiro</i> | Alterna a mesclagem e a combinação de cores na máscara de saída final. Pode ser ativada para quantas cores você deseja combinar. |
| <b>Material #1-16</b> <i>(Valor da cor)</i> | Seletor de cores para a cor dos materiais que serão convertidos em preto e branco. |
| <b>Parâmetros do Seletor de Cores</b> | Modifica a mesclagem e a conversão da cor em preto e branco. |
| <b>Grau de seleção</b> <i>0.01 - 1.0</i> | O quanto misturar com cores vizinhas. |
| <b>Preenchimento</b> <i>0.0 - 1.0</i> | Nitidez da transição, como Contraste. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/matselector-ex.png" />
        </td>
    </tr>
</table>
