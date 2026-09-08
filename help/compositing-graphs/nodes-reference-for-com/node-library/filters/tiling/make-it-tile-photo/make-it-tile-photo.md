---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-photo.html"
breadcrumb-title: ''
description: Use o nó Criar foto em bloco para converter fotografias em texturas de revestimento perfeitas para a criação de material.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Photo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tornar foto lado a lado
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 9%

---


# Tornar foto lado a lado

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/make-it-tile-photo.png)

![](../../../../../../assets/make-it-tile-photo-grayscale.png)

<b>Em:</b> Filtros > Lado a Lado

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Este nó fornece a funcionalidade de correção de borda para qualquer imagem que possa não ser ladrilhada devido a bordas não contínuas. Ela não afeta nada além das bordas da imagem de entrada. Se quiser ajustar o dimensionamento ou o ladrilho de diferentes maneiras, observe [Criar um patch de ladrilho](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-patch/make-it-tile-patch.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Distorção de máscara H</b> <i>-100.0 - 100.0</i> | Introduz a deformação no eixo horizontal para evitar transições indefinidas. |
| <b>Distorção de máscara V</b> <i>-100.0 - 100.0</i> | Introduz a deformação no eixo vertical para evitar transições indefinidas. |
| <b>Tamanho da máscara H</b> <i>0.0 - 1.0</i> | Define até onde a borda de transição alcança horizontalmente. |
| <b>Tamanho da máscara V</b> <i>0.0 - 1.0</i> | Define até onde a borda de transição alcança verticalmente. |
| <b>Precisão da Máscara H</b> <i>0.0 - 1.0</i> | Define a suavidade da transição na horizontal. |
| <b>Precisão da Máscara V</b> <i>0.0 - 1.0</i> | Define a suavidade da transição na vertical. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/mit-photo-ex.png" />
        </td>
    </tr>
</table>
