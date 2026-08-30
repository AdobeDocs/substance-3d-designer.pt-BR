---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/3d-texture-offset.html"
breadcrumb-title: ''
description: Use o nó Deslocamento de textura 3D para deslocar texturas no espaço 3D a fim de criar efeitos de paralaxe e variações de superfície.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > 3D Texture Offset
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Deslocamento de textura 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# Deslocamento de textura 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](3d-texture-offset.resources/3dtextureoffsetgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](3d-texture-offset.resources/3dtextureoffsetcolor.png){width="200px"}

</td>
</tr>
</table>

<b>Em:</b> Filtro > Transformação

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O nó **Deslocamento de Textura 3D** aplica uma *transformação de deslocamento* nos eixos **X**, **Y** e **Z** em um objeto descrito pela *textura 3D* conectada à **Entrada**.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Tons de cinza/Cor</i> | A <i>textura 3D</i> que descreve um objeto 3D.<br>O objeto é normalmente descrito em um <i>cubo de unidade</i>. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Deslocamento</b> <i>Flutuante3</i> | A quantidade de deslocamento em <i>espaço global</i> aplicada ao objeto descrito pela <i>textura 3D</i> conectada à <b>Entrada</b>. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-offset.resources/3dtextureoffset-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-offset.resources/3dtextureoffset-node.png" />
        </td>
    </tr>
</table>
