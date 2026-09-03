---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/creased.html"
breadcrumb-title: ''
description: Use o nó vincado para gerar padrões de vinco para criar efeitos de tecido dobrado e textura de superfície enrugada.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Creased
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Suavizado
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 8%

---


# Suavizado

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](creased.resources/creased-01.png){width="128px"}

<b>Entrada:</b> Geradores de Textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Esse nó gera um ruído semelhante ao de um pano. Pode ser interpretado como Heightmap

Creased é útil quando você precisa de um ruído semidirecional com grande variação de escala.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Escala</b> <i>1 - 8</i> | Define a escala global do efeito. |
| <b>Intensidade de distorção</b> <i>0.0 - 128.0</i> | Define a intensidade do efeito de curvatura/distorção. |
| <b>Desordem</b> <i>0.0 - 100.0</i> | Desloca levemente as camadas usadas para gerar o ruído, introduzindo variação. |
| <b>Expansão não quadrada</b> <i>Falso/Verdadeiro</i> | Permite a compensação de esmagamento e alongamento com proporções não quadradas. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="creased.resources/creased-02.gif" />
        </td>
    </tr>
</table>
