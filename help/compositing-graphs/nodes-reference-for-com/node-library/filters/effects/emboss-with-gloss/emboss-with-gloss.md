---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/emboss-with-gloss.html"
breadcrumb-title: ''
description: Use o nó Relevo com brilho para criar efeitos em alto-relevo com mapas de brilho para adicionar profundidade e brilho às texturas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Emboss With Gloss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Entalhe Com Brilho
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 6%

---


# Entalhe Com Brilho

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](emboss-with-gloss.resources/emboss-with-gloss.png){width="128px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Executa um efeito de entalhe com brilho (reflexo de specular) adicionado em uma entrada de cor e height. Essencialmente, adiciona iluminação feita bake e falsa a uma imagem com base em informações do height. Útil para alguns estilos de texturização que exigem iluminação feita bake nas texturas.

Para uma versão com mais opções, consulte [Uber Relevo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md). Há também a versão atômica mais simples do [Relevo](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Cor</b> <i>Entrada de cores</i> |  |
| <b>Height</b> <i>Entrada em tons de cinza</i> |  |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Cor de realce</b> <i>(Valor da cor)</i> | Cor do destaque do specular. |
| <b>Cor da sombra</b> <i>(Valor da cor)</i> | Cor usada em áreas sombreadas/não iluminadas. |
| <b>Brilho</b> <i>0.0 - 0.5</i> | Tamanho de realce reluzente. |
| <b>Intensidade</b> <i>0.0 - 10.0</i> | Intensidade do realce. |
| <b>Ângulo de luz</b> <i>0.0 - 1.0</i> | Ângulo de incidência da luz (simulada). |
