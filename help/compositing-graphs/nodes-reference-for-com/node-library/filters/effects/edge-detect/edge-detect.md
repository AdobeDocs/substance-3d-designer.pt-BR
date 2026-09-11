---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/edge-detect.html"
breadcrumb-title: ''
description: Use o nó Detecção de borda para detectar bordas no textura para criar contornos e efeitos de máscara baseados em bordas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Edge Detect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Detecção de borda
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5c9ae53c1de18b1c09789a480cba6b1d70bd350d
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 7%

---


# Detecção de borda

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-detect.resources/edge-detect.png){width="128px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Detecta o contraste em imagens em preto e branco e, em seguida, cria uma máscara em preto e branco destacando o contraste.

Útil em muitos casos em que algum tipo de máscara para bordas é necessário. Lembre-se de que ele funciona melhor com entradas de alto contraste; se necessário, ajuste o contraste antes de passar algo para esse nó.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Largura da borda</b> <i>1.0 - 16.0</i> | Largura das áreas detectadas ao redor das bordas. |
| <b>Arredondamento de arestas</b> <i>0.0 - 16.0</i> | Arredonda, desfoca e suaviza a máscara gerada. |
| <b>Inverter</b> <i>Falso/Verdadeiro</i> | Inverte o resultado. |
| <b>Tolerância</b> <i>0.0 - 1.0</i> | Fator de limite de tolerância para onde as bordas devem aparecer. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-detect.resources/edge-detect-ex.png" />
        </td>
    </tr>
</table>
