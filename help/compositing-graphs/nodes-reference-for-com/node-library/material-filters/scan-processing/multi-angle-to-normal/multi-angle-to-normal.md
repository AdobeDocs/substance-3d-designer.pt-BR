---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-angle-to-normal.html"
breadcrumb-title: ''
description: Use o nó Multiângulo para normal para gerar mapas normais de imagens digitalizadas multiangulares para obter detalhes precisos da superfície.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi-Angle to Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Multiângulo para normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 3%

---


# Multiângulo para normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-angle-to-normal.resources/multi-angle-to-normal.png){width="128px"}

<b>Entrada:</b> Filtros Materiais > Processamento de materiais escaneados

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Este nó constrói um mapa normal a partir de um conjunto de fotografias/digitalizações feitas sob diferentes condições de iluminação. Permite uma conversão de Normalmap muito mais precisa do que ao tentar extrair Normais de uma única imagem de albedo.

É mais complicado do que [Vários ângulos para Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md), pois exige que você use ângulos de iluminação definidos e precisos para suas entradas. Cada ângulo de iluminação da amostra deve ser espaçado uniformemente e as amostras precisam ser inseridas em sequência. Portanto, para três amostras, os ângulos de iluminação devem ser obtidos em: 0, 120, 240 - ou qualquer deslocamento uniforme disso (como 90, 210, 330).

>[!NOTE]
>
> Consulte [Vários ângulos para Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) para obter a versão de albedo deste nó. Se você quiser pré-processar suas entradas, o [Multi Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md), o [Multi Crop](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md) e o [Multi Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md) podem ser úteis, pois devem ser combinados com esses nós.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada 1-8</b> <i>Entrada de cores</i> |  |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Formato Normal</b> <i>DirectX, OpenGL</i> | Alterna entre diferentes formatos de Mapas Normais (inverte o canal verde). |
| <b>Quantidade de Amostras</b> <i>2 - 8</i> | Define a quantidade de amostras (entradas) a serem processadas. |
| <b>Intensidade</b> <i>0.0 - 1.0</i> | Define a intensidade do mapa normal. |
| <b>Ângulo de Luz da Primeira Amostra</b> <i>0.0 - 360.0</i> | Define a direção do ângulo de iluminação da primeira entrada. |
| <b>Próximo Ângulo de Luz de Amostra</b> <i>Sentido anti-horário, sentido horário</i> | Define em que direção a iluminação na próxima amostra se move. |
