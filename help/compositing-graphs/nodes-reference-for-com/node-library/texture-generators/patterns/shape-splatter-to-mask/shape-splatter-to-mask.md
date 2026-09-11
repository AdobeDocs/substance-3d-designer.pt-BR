---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter-to-mask.html"
breadcrumb-title: ''
description: Use o nó respingos de forma para máscara para converter padrões de respingos de forma em máscaras para mesclagem de material e efeitos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter to Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dispersão de forma para máscara
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 4%

---


# Dispersão de forma para máscara

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-splatter-to-mask.resources/shape-splatter-to-mask.png){width="128px"}

<b>Em:</b> Geradores De Textura > Padrões

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Converte Dados de [Respingo de Forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md) em uma máscara preto e branco com base na ID de Padrão. Permite, por exemplo, criar uma máscara com apenas um determinado tipo de padrão. Tem opções extras para selecionar um intervalo de IDs de padrão e ocultar aleatoriamente algumas das formas.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Intervalo Inicial de ID de Padrão</b> <i>1 - 8</i> | Defina a primeira ID de padrão no intervalo a ser selecionado. |
| <b>Intervalo Final de ID de Padrão</b> <i>1 - 8</i> | Defina a última ID do padrão no intervalo a ser selecionado. |
| <b>Máscara aleatória</b> <i>0.0 - 1.0</i> | Defina a proporção de Padrões para mascarar aleatoriamente. |
| <b>Saída</b> <i>Máscara Binária, Máscara Inteira, Valores Em Tons De Cinza</i> | Determine o tipo de valores de saída. A Máscara binária retorna apenas valores em preto e branco, 0-ou-1, a Máscara de inteiro codificará valores mais altos até 8 para cada Padrão no formato HDR e os Valores em tons de cinza propagarão o intervalo proporcionalmente entre 0 e 1. |
