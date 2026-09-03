---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-3.html"
breadcrumb-title: ''
description: Use o nó Noise Upscale 3 para aumentar texturas usando algoritmos avançados baseados em ruído para preservar detalhes em resoluções mais altas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Aumento de ruído 3
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 2%

---


# Aumento de ruído 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](noise-upscale-3.resources/noise-upscale-3-01.png){width="128px"}

<b>Entrada:</b> Filtros > Transformas

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Utiliza um procedimento de ruído de entrada e o dimensiona para resolução dupla, mantendo os detalhes, mas sem introduzir muitos ladrilhos. Usa uma máscara definida pelo usuário para mesclar ruídos sobre sua escala original.

Este nó é destinado principalmente para otimizar gráficos lentos que usam ruídos pesados e grandes. Ele permite que você use resoluções mais altas sem introduzir muito tempo extra de computação.

Veja também [Aumento de Ruído 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-1/noise-upscale-1.md) e [Aumento de Ruído 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md), que na maioria dos casos tendem a ser um pouco melhores para ocultar ladrilhos.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Tons de cinza</b> <i>Entrada em tons de cinza</i> | Imagem de ruído de destino. |
| <b>Máscara</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="noise-upscale-3.resources/noise-upscale-3-02.png" />
        </td>
    </tr>
</table>
