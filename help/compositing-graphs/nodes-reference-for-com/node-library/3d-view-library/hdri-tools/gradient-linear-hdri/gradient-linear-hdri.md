---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/gradient-linear-hdri.html"
breadcrumb-title: ''
description: Use o nó HDRI linear de gradiente para criar gradientes lineares em ambientes HDRI para configurações de iluminação personalizadas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Gradient Linear (HDRI)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gradiente linear (HDRI)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 43dd5433948c89f68426040a2a2d76282072c75d
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---


# Gradiente linear (HDRI)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/gradient-linear.png){width="200px"}

<b>Entrada:</b> Visualização 3D > Ferramenta HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Cria um gradiente linear ao longo do centro e com um ponto inserido pelo usuário. O resultado final é ajustado de acordo com a projeção esférica, diferentemente do [Gradiente linear 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-linear-1/gradient-linear-1.md) normal.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Posição do Ponto</b> | Posição do ponto usada para determinar a direção do gradiente. |
| <b>Cor Superior</b> <i>(Valor da cor)</i> | Cor da parte superior do gradiente (no ponto) |
| <b>Cor Inferior</b> <i>(Valor da cor)</i> | Cor da parte inferior do gradiente (longe do ponto). |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta o contraste do resultado. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/gradient-ex1.gif" />
        </td>
    </tr>
</table>
