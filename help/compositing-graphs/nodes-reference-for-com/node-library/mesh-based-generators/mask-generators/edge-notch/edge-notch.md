---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-notch.html"
breadcrumb-title: ''
description: Use o nó Entalhe de borda para gerar padrões de entalhe nas bordas da malha a fim de criar efeitos realistas de danos e recuo de borda.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Notch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Entalhe de borda
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Entalhe de borda

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-notch.png){width="128px"}

## Entalhe de borda

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara representa uma máscara simples para bordas elevadas, divididas por um ruído de alta frequência. Consulte [Dirt de borda](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md) ou [Danos de borda](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-damages/edge-damages.md) para obter mais opções.

## Entradas

* **Curvatura**: *Entrada em tons de cinza*\
  Mapa baked usado para realçar bordas. Obrigatório!
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

## Parâmetros

* **Nível**: *0.0 - 1.0*\
  Define o nível do efeito Entalhe de borda.
* **Contraste**: *0.0 - 1.0*\
  Ajusta o contraste do resultado.

## Imagens de exemplo

![](../../../../../../assets/edge-notch-ex.gif)

</td>
</tr>
</table>
