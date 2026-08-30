---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/multi-switch.html"
breadcrumb-title: ''
description: Use o nó Multiswitch para alternar entre várias texturas de entrada com base em um seletor para seleção de textura condicional.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Multi Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Comutador múltiplo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# Comutador múltiplo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-switch.resources/multi-switch-greyscale.png){width="128px"}

![](multi-switch.resources/multi-switch.png){width="128px"}

<b>Entrada:</b> Filtros > Mesclagem

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Atua como uma switch-box, apenas passando pela entrada definida pelo parâmetro &#39;Input Selection&#39;. Portanto, se duas entradas estiverem conectadas, somente uma delas será retornada (sem modificações), dependendo da escolha do usuário.

Muito útil para adicionar muitas opções diferentes em um gráfico. Combinado com a [exposição](../../../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)(de preferência como uma Lista Suspensa), é possível muita personalização.

Importante: certifique-se de usar a versão apropriada para sua entrada! Use “Múltiplo switch” para entradas de cor, “Múltiplo switch de tons de cinza” para entradas de tons de cinza.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada 1-20</b> <i>Entrada de cores</i> |  |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Número de Entrada</b> <i>2 - 20</i> | Quantidade de entradas a serem expostas. Importante: não remove conexões quando o número é reduzido! |
| <b>Seleção de Entrada</b> <i>1 - 20</i> | A entrada a ser retornada como resultado. |
