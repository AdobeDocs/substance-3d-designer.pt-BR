---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/multi-directional-warp.html"
breadcrumb-title: ''
description: Use o nó Distorção multidirecional para aplicar efeitos de distorção em várias direções para criar padrões de distorção complexos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Multi Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Várias Deformações direcionais
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 3%

---


# Distorção multidirecional

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-directional-warp.resources/multi-directional-warp-01.png)![](multi-directional-warp.resources/multi-directional-warp-02.png)

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

A Distorção Multidirecional aplica a [Distorção Direcional](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) várias vezes em direções opostas, enquanto a textura deslocada permanece no lugar. Ele difere da Distorção direcional padrão na medida em que pode empurrar em várias direções, enquanto a versão atômica só permite uma. Dessa forma, ele resolve o problema clássico em que a Deformação direcional sempre parece afastar demais a imagem em uma única direção. Em vez disso, ela funciona ao longo de várias direções ou eixos em vez de uma única direção.

Difere principalmente de [Non Uniform Directional Warp](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/non-uniform-directional/non-uniform-directional-warp.md) no sentido de que é um pouco mais limitado: a direção da distorção é controlada apenas através de parâmetros e não pode ser definida através de um mapa de entrada. A vantagem é que é um pouco mais fácil de usar e pode ser mais preciso, dependendo do seu caso de uso.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Entrada em Tons de Cinza/Cores</i> | Mapa base ao qual a distorção será aplicada. Pode ser colorido ou em tons de cinza. |
| <b>Entrada de Intensidade</b> <i>Entrada em tons de cinza</i> | O mapa de máscara obrigatório que direciona a intensidade do efeito de distorção deve ser em tons de cinza. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Intensidade</b> <i>0.0 - 20.0</i> | Define a intensidade do efeito de distorção, em que distância os pixels devem ser empurrados para fora. |
| <b>Ângulo de distorção</b> <i>0.0 - 1.0</i> | Define o Ângulo ou a direção na qual aplicar o efeito Distorcer. |
| <b>Modo</b> <i>Média, Máx, Mín, Cadeia</i> | Define o modo de Combinar para passagens consecutivas. Só tem efeito se as Direções forem 2 ou 4! |
| <b>Direções</b> <i>1, 2, 4</i> | Define em quantos eixos a distorção funciona. 1 significa que se move na direção do Ângulo e, no oposto dessa direção, 2 significa o eixo do ângulo, mais o eixo perpendicular, 4 significa os eixos anteriores, mais inclinações de 45 graus. |
