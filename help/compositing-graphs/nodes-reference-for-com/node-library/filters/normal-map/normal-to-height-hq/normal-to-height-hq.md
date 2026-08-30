---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height-hq.html"
breadcrumb-title: ''
description: Use o nó QG Normal para Height para converter mapas normais em mapas de altura de alta qualidade para a extração de detalhes da superfície.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal To Height HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal para Height HQ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 3%

---


# Normal para Height HQ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-to-height-hq.resources/normal-to-height-hq.png){width="128px"}

<b>Entrada:</b> Filtros > Mapa normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Nó de conversão reversa que tenta converter um Normalmap de espaço tangente em um Heightmap. Este é o nó mais avançado; [Normal a Height](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height/normal-to-height.md) tem menos opções e usa cálculos diferentes.

Útil quando você tem apenas uma origem Normalmap, mas ainda deseja executar operações que a combinam com um Heightmap. Lembre-se de que isso nunca poderá fornecer um resultado 100% correto, pois as informações são perdidas por natureza do processo quando o Height é convertido para Normal. Ele nunca pode substituir um Heightmap gerado corretamente!

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Formato Normal</b> <i>DirectX, OpenGL</i> | Alterna entre diferentes formatos de Mapas Normais (inverte o canal verde). |
| <b>Saldo do Relevo</b> <i>0.0 - 1.0</i> | Combinar entre polarização de baixa e alta frequência. |
| <b>Intensidade de Height</b> <i>0.0 - 1.0</i> | A Intensidade ou o multiplicador de Heightmap funciona um pouco como a opacidade global. |
| <b>Normalizar Height</b> <i>Falso/Verdadeiro</i> | Dimensiona automaticamente o intervalo do mapa de altura para usar contraste total, como [níveis automáticos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md). |
| Qualidade <b>1</b> <i>Normal, Alto</i> | Alterna entre velocidade ou qualidade. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-to-height-hq.resources/normal2height-hq-ex.png" />
        </td>
    </tr>
</table>
