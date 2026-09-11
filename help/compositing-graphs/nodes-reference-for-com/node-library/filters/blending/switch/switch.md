---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/switch.html"
breadcrumb-title: ''
description: Use o nó Alternar para alternar entre duas texturas de entrada com base em uma máscara para seleção de textura condicional.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Alterar
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 3%

---


# Alterar

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](switch.resources/switch-1.png){width="128px"}

![](switch.resources/switch-grayscale.png){width="128px"}

<b>Entrada:</b> Filtros > Mesclagem

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Um nó de chave simples de duas posições. Retorna a Entrada 1 ou a Entrada 2 com base na configuração do parâmetro Switch. O resultado não foi modificado. Consulte [Chave Múltipla](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md) para obter uma versão mais avançada.

Muito útil para expor uma opção booleana (Verdadeiro/Falso) em um gráfico, em que você só precisa de um único botão e não de uma lista suspensa complexa para uma seleção inteira de opções.

Importante: certifique-se de usar a versão apropriada para sua entrada! Use “Alternar” para entradas de cor e “Alternar escala de cinza” para entradas de escala de cinza.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada 1 (Verdadeira)</b> <i>Entrada colorida ou em tons de cinza</i> |  |
| <b>Entrada 2 (Falso)</b> <i>Entrada colorida ou em tons de cinza</i> |  |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Alternar</b> <i>Falso/Verdadeiro</i> | Alterna entre a Entrada 1 (True) e a Entrada 2 (False). |
