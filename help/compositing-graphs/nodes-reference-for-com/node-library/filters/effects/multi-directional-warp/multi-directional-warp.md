---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/multi-directional-warp.html"
breadcrumb-title: ''
description: Use o nó Distorção multidirecional para aplicar efeitos de distorção em várias direções para criar padrões de distorção complexos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Multi Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Distorção multidirecional
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 1%

---


# Distorção multidirecional

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-directional-warp-color.png)![](../../../../../../assets/multi-directional-warp-grayscalepng.png)

## Distorção multidirecional (tons de cinza)

**Entrada:** *Filtros/Efeitos*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

A Distorção Multidirecional aplica a [Distorção Direcional](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) várias vezes em direções opostas, enquanto a textura deslocada permanece no lugar. Ele difere da Distorção direcional padrão na medida em que pode empurrar em várias direções, enquanto a versão atômica só permite uma. Dessa forma, ele resolve o problema clássico em que a Distorção direcional sempre parece afastar demais a imagem em uma única direção. Em vez disso, ele funciona ao longo de várias direções ou eixos em vez de uma única direção.

Difere principalmente de [Non Uniform Directional Warp](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/non-uniform-directional/non-uniform-directional-warp.md) no sentido de que é um pouco mais limitado: a direção da distorção é controlada apenas através de parâmetros e não pode ser definida através de um mapa de entrada. A vantagem é que é um pouco mais fácil de usar e pode ser mais preciso, dependendo do seu caso de uso.

## Parâmetros

### Entradas

* **Entrada**: *Entrada em Tons de Cinza/Cor*\
  Mapa base ao qual a distorção será aplicada. Pode ser colorido ou em tons de cinza.
* **Entrada de Intensidade**: *Entrada em Tons de Cinza*\
  O mapa de máscara obrigatório que direciona a intensidade do efeito de distorção deve ser em tons de cinza.

### Parâmetros

* **Intensidade**: *0.0 - 20.0*\
  Define a intensidade do efeito de distorção, em que distância os pixels devem ser empurrados para fora.
* **Ângulo de Distorção**: *0.0 - 1.0*\
  Define o Ângulo ou a direção na qual aplicar o efeito Distorcer.
* **Modo**: *Média, Máx, Mín, Cadeia*\
  Define o modo de mesclagem para passagens consecutivas. Só tem efeito se as Direções forem 2 ou 4!
* **Direções**: *1, 2, 4* Define em quantos eixos a distorção funciona. 1 significa que se move na direção do Ângulo e, no oposto dessa direção, 2 significa o eixo do ângulo, mais o eixo perpendicular, 4 significa os eixos anteriores, mais inclinações de 45 graus.

## Imagens de exemplo

</td>
</tr>
</table>
