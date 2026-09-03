---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/uber-emboss.html"
breadcrumb-title: ''
description: Use o nó Entalhe Uber para criar efeitos avançados de entalhe com controles personalizáveis de profundidade, ângulo e iluminação.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Uber Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Entalhe Uber
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 9%

---


# Entalhe Uber

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](uber-emboss.resources/uber-emboss-01.png){width="128px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Versão avançada, repleta de recursos do [Entalhe](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md). Executa um elaborado efeito de iluminação falso em 2D com base em um mapa de altura.

Útil ao criar iluminação preparada para determinados estilos de texturização quando muito controle é necessário.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Cor</b> <i>Entrada de cores</i> | Imagem base para modificar. |
| <b>Height</b> <i>Entrada em tons de cinza</i> | Mapa de altura usado como driver para o efeito. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Cor do ambiente</b> <i>(Valor da cor)</i> | Cor usada em áreas sombreadas. |
| <b>Cor da Difusão</b> <i>(Valor da cor)</i> | Cor usada em áreas iluminadas. |
| <b>Cor do Specular</b> <i>(Valor da cor)</i> | Cor usada para reflexões de specular |
| <b>Intensidade da luz</b> <i>0.0 - 1.0</i> | Intensidade da luz (simulada). |
| <b>Ângulo de luz</b> <i>0.0 - 1.0</i> | Ângulo de incidência da luz (falsa) |
| <b>Intensidade de Specular</b> <i>0.0 - 1.0</i> | Intensidade dos reflexos do specular. |
| <b>Brilho do Specular</b> <i>0.0 - 1.0</i> | Tamanho do destaque do specular. |
| <b>Aspereza de Difusão</b> <i>0.0 - 1.0</i> | Aspereza usada no cálculo da iluminação difusa. |
| <b>Opacidade das sombras</b> <i>0.0 - 1.0</i> | Mesclar opacidade das áreas sombreadas. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="uber-emboss.resources/uber-emboss-02.png" />
        </td>
    </tr>
</table>
