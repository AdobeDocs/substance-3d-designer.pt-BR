---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/non-uniform-directional-warp.html"
breadcrumb-title: ''
description: Use o nó Non Uniform Directional Warp para aplicar deformação direcional não uniforme para criar efeitos de distorção variados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Non Uniform Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Non Uniform Directional Warp
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 1%

---


# Non Uniform Directional Warp

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-directional-warp-color.png)![](../../../../../../assets/non-uniform-directional-warp-grayscale.png)

## Diretório Não Uniforme Distorcer (tons de cinza)

**Entrada:** *Filtros/Efeitos*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

A Distorção de Direção Não Uniforme é uma versão avançada da [Distorção Direcional](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md) que permite que a intensidade e a direção da distorção sejam determinadas por uma entrada de imagem. Permite muito mais controle e pode criar uma distorção de imagem muito útil e interessante, em vão igual ao [Desfoque de Inclinação](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md).

É diferente de [Distorção Multidirecional](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/multi-directional-warp/multi-directional-warp.md), pois permite o controle sobre o Ângulo por meio de uma entrada de Mapa personalizada, enquanto a Distorção Multidirecional só permite o controle da Direção por meio de parâmetros. Isso significa que você pode criar efeitos avançados de curva e de direita que, de outra forma, não seriam possíveis.

## Parâmetros

### Entradas

* **Entrada**: *Entrada em Tons de Cinza*\
  Mapa base ao qual a distorção será aplicada.
* **Entrada de Intensidade**: *Entrada em Tons de Cinza*\
  O mapa de máscara obrigatório que direciona a intensidade do efeito de distorção deve ser em tons de cinza.
* **Entrada de Ângulo de Distorção**: *Entrada em Tons de Cinza*\
  O mapa de máscara obrigatório que orienta o Ângulo do efeito de distorção deve ser em tons de cinza.

### Parâmetros

* **Intensidade**: *0.0 - 20.0*\
  Define a intensidade do efeito de distorção, em que distância os pixels devem ser empurrados para fora.
* **Ângulo de Distorção**: *0.0 - 1.0*\
  Define o Ângulo ou a direção na qual aplicar o efeito Distorcer.
* **Multiplicador de Entrada de Ângulo de Distorção**: *0.0 - 1.0*\
  Define o efeito do Mapa de entrada do Ângulo de distorção. O mapa de entrada Ângulo de distorção será usado para interpolar de 0 ao valor desse parâmetro.
* **Modo De Rastreamento**: *Mín, Máx, Média*\
  Define como as Trilhas são mescladas.
* **Comprimento da Trilha**: *0.0 - 1.0*\
  Define o comprimento das trilhas.
* **Desvanecimento da Trilha**: *0.0 - 1.0*\
  Define o quanto cada Trilha deve desvanecer-se
* **Curva de trilha**: *-1.0 - 1.0* Só tem efeito se o Desvanecimento da trilha não for 0. Define o comportamento do efeito de esmaecimento.

## Imagens de exemplo

</td>
</tr>
</table>
