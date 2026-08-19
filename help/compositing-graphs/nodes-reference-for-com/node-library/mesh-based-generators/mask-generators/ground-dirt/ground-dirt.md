---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/ground-dirt.html"
breadcrumb-title: ''
description: Use o nó Dirt terrestre para gerar máscaras de acúmulo de dirt com base na posição da malha e orientação relativas ao solo.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Ground Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dirt terrestre
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# Dirt terrestre

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/ground-dirt.png){width="128px"}

## Dirt terrestre

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara representa o dirt acumulado desde o início, o oposto de [De baixo para cima](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/bottom-to-top/bottom-to-top.md) ou [Dust](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/dust/dust.md). Não há substituição de mapa personalizada.

## Entradas

* **Posição**: *Entrada em Tons de Cinza*\
  Mapa de posição cozido no qual o efeito base será ativado. Obrigatório!
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

## Parâmetros

* **Nível**: *0.0 - 1.0*\
  Define o nível de aparência total do dirt.
* **Contraste**: *0.0 - 1.0*\
  Ajusta o contraste do resultado.
* **Height de Dirt**: *0.0 - 1.0* Define até qual height (proporcionalmente) o dirt deve aparecer.

## Imagens de exemplo

![](../../../../../../assets/ground-dirt-ex.gif)

</td>
</tr>
</table>
