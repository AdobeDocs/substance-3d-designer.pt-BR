---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/exposure-preview.html"
breadcrumb-title: ''
description: Use o nó Visualização da exposição para visualizar ajustes de exposição em ambientes HDRI antes da renderização final.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Exposure Preview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Visualização da exposição
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 7%

---


# Visualização da exposição

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](exposure-preview.resources/hdr-exposure-preview.png){width="200px"}

<b>Entrada:</b> Visualização 3D > Ferramenta HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Nó auxiliar para visualizar etapas de exposição. Usuários definem um valor mínimo e máximo, o nó gera uma imagem muito maior com um número de diferentes versões expostas da entrada original. As diferentes versões são sempre empilhadas horizontalmente, a intensidade depende da resolução do nó ou gráfico.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Exposição Máxima (EV)</b> <i>-8.0 - 8.0</i> | Exposição máxima da imagem superior mais clara. |
| <b>Exposição Mínima (VE)</b> <i>-8.0 - 8.0</i> | Exposição mínima da imagem inferior mais escura. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="exposure-preview.resources/exp-preview-ex.png" />
        </td>
    </tr>
</table>
