---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-sdf.html"
breadcrumb-title: ''
description: Use o nó SDF de Textura 3D para gerar texturas de campo de distância assinadas a partir de dados 3D para criar formas e efeitos suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture SDF
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SDF de textura 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---


# SDF de textura 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-texture-sdf.resources/3d-texture-sdf-01.png){width="200px"}

<b>Entrada:</b> Filtro > Efeito

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O nó **SDF** de Textura 3D gera o *campo de distância assinado* de uma forma a partir da máscara *textura 3D* da **Entrada** que representa as fatias do *volume* da forma.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada de máscara</b> <i>Tons de cinza</i> | A máscara de <i>textura 3D</i> que representa as fatias do <i>volume</i> de uma forma. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Limite</b> <i>Flutuante</i> | Quando o volume da forma é descrito por um <i>gradiente de desvanecimento</i>, define o valor do gradiente no qual a <i>superfície</i> da forma é <i>detectada</i>. |
| <b>Saída</b> <i>Inteiro</i> | O tipo de campo de distância que deve ser gerado:<br>- <i>Campo de distância</i>: gera um campo de distância que descreve as distâncias <i>fora</i> da forma.<br>- <i>Campo de distância sinalizado</i>: gera um campo de distância que descreve as distâncias <i>fora</i> (positivas) e <i>dentro</i> (negativas) da forma. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3d-texture-sdf-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3d-texture-sdf-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3d-texture-sdf-04.png" />
        </td>
    </tr>
</table>
