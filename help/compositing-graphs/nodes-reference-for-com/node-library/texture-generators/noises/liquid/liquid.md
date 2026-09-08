---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/liquid.html"
breadcrumb-title: ''
description: Use o nó Líquido para gerar padrões líquidos e fluidos para criar água, óleo e outros efeitos de superfície do fluido.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Liquid
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Líquido
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8774511f26429071b91a2eeeb8728ac36dc31ed5
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 9%

---


# Líquido

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/liquid.png){width="128px"}

<b>Entrada:</b> Geradores de Textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Esta é uma variante simples do [Ruído Gaussiano](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md), que [deforma](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) consigo mesmo para criar um efeito líquido.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Escala</b> <i>1 - 128</i> | Define a escala global do efeito. |
| <b>Desordem</b> <i>0.0 - 1.0</i> | Muda a fase do ruído para introduzir uma pequena variação |
| <b>Intensidade de distorção</b> <i>0.0 - 1.0</i> | Define a intensidade do efeito de distorção. |
| <b>Expansão não quadrada</b> <i>Falso/Verdadeiro</i> | Permite a compensação de esmagamento e alongamento com proporções não quadradas. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/liquid-ex.gif" />
        </td>
    </tr>
</table>
