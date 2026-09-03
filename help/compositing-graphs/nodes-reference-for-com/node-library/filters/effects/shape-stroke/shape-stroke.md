---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-stroke.html"
breadcrumb-title: ''
description: Use o nó Traçado de forma para adicionar contornos de traçado a formas para criar bordas e efeitos de borda.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Stroke
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Traçado da forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 4%

---


# Traçado da forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-stroke.resources/shape-stroke-01.png){width="128px"}

![](shape-stroke.resources/shape-stroke-02.png){width="128px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Adiciona um traçado ou contorno em torno de uma máscara em preto e branco (para a versão em tons de cinza) ou de uma forma com um canal alfa (para a versão colorida), como você já deve estar familiarizado com outros aplicativos de edição de imagens 2D. Pode ser visto como uma versão mais completa da [Detecção de borda](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md).

Muito útil para diversos efeitos de edição de imagens.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Largura</b> <i>-1.0 - 1.0</i> | Largura do efeito de traçado. |
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Opacidade global do efeito. |
| <b>(Contorno) Cor</b> <i>(Valor da cor)</i> | Cor usada para o efeito de contorno. |
| <b>Cor da máscara</b> <i>(Valor da cor) (Somente Versão em Tons de Cinza)</i> | Cor sólida a ser usada para a saída mapeada de transparência. |
| <b>A Entrada É Pré-Multiplicada</b> <i>Falso/Verdadeiro (Somente Versão Colorida)</i> | Se a entrada deve ser assumida como pré-multiplicada. |
| <b>Saída Pré-Multiplicada</b> <i>Falso/Verdadeiro</i> | Se a saída deve ser pré-multiplicada. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-stroke.resources/shape-stroke-03.png" />
        </td>
    </tr>
</table>
