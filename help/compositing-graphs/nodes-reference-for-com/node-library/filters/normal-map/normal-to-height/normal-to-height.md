---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height.html"
breadcrumb-title: ''
description: Use o nó Normal para Height para converter mapas normais em mapas de height para extrair informações de profundidade de superfície.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal to Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal para Height
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 3%

---


# Normal para Height

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-to-height.resources/normal-to-height-01.png){width="128px"}

<b>Entrada:</b> Filtros > Mapa normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Nó de conversão reversa que tenta converter um Normalmap de espaço tangente em um Heightmap. Esta é a versão ligeiramente mais simples; o [Normal para o Height HQ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height-hq/normal-to-height-hq.md) tem mais opções.

Útil quando você tem apenas uma origem Normalmap, mas ainda deseja executar operações que a combinam com um Heightmap. Lembre-se de que isso nunca poderá fornecer um resultado 100% correto, pois as informações são perdidas por natureza do processo quando o Height é convertido para Normal. Se você ajustar as configurações de acordo, esta versão não-HQ faz um trabalho decente de converter detalhes simples.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Saldo do Relevo</b> <i>0.0 - 1.0</i> | Ajuste a extensão em que as diferentes frequências influenciam o resultado final. Isso é amplamente dependente do mapa de entrada e requer um pouco de ajustes. |
| <b>Formato Normal</b> <i>DirectX, OpenGL</i> | Alterna entre diferentes formatos de Mapas Normais (inverte o canal verde). |
| <b>Opacidade Global</b> <i>0.0 - 1.0</i> | Ajusta a opacidade global do efeito. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-to-height.resources/normal-to-height-02.png" />
        </td>
    </tr>
</table>
