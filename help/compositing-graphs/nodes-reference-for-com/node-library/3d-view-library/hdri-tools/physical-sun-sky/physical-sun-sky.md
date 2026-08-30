---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/physical-sun-sky.html"
breadcrumb-title: ''
description: Use o nó Físico do SunSky para gerar ambientes de iluminação física precisos do sol e do céu para visualização de material realista.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Physical SunSky
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SunSky físico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 9%

---


# Sol/céu físico

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](physical-sun-sky.resources/panorama-physical-sun-sky.png){width="200px"}

<b>Entrada:</b> Visualização 3D > Ferramenta HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Implementação física de Sun e Sky baseada no modelo de claraboia Hosek-Wikie. Fornece uma base excelente para um HDRI artificial.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Posição do Sol</b> | gama = [0,1]x[0,1] (ângulos de longitude e latitude) |
| <b>Turvação</b> <i>1.0 - 10.0</i> | A turbidez varia de 1 a 10 |
| <b>Albedo</b> <i>0.0 - 1.0</i> | O albedo varia de 0 a 1. |
| <b>Cor do solo</b> <i>(Valor da cor)</i> | Cor do plano do solo. |
| <b>Exposição (EV)</b> <i>-1.0 - 4.0</i> | Valor da exposição da saída resultante. |
| <b>Tamanho do Sol</b> <i>0.0 - 4.0</i> | Escala do Sol, qualquer valor diferente de 1 é fisicamente incorreto. O valor tem efeitos sutis! |
| <b>Intensidade do Sol</b> <i>0.0 - 1.0</i> | Intensidade do disco solar. O disco solar é relativamente pequeno, por isso o efeito não é imediatamente visível. |
| <b>Intensidade do céu</b> <i>0.0 - 1.0</i> | Intensidade do céu. Também afeta a queima do sol no céu, não no disco em si. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="physical-sun-sky.resources/sky-ex.gif" />
        </td>
    </tr>
</table>
