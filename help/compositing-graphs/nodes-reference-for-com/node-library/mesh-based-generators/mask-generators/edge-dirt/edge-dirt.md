---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-dirt.html"
breadcrumb-title: ''
description: Use o nó Dirt de borda para gerar máscaras de acúmulo de dirt nas bordas da malha a fim de criar efeitos realistas de reticência de borda.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Dirt
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 2%

---


# Edge Dirt

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-dirt.png){width="128px"}

## Edge Dirt

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara representa um efeito de dirt que se acumula ao redor das bordas, com base apenas em um mapa de curvatura.

## Parâmetros

### Entradas

* **Curvatura**: *Entrada em tons de cinza*\
  Mapa baked usado para posicionamento do efeito. Obrigatório!
* **Máscara de Variação**: *Entrada em Tons de Cinza*\
  Slot de máscara usado para mascarar os efeitos do nó, usado somente quando o parâmetro de substituição está ativado.
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Nível**: *0.0 - 1.0*\
  Define a quantidade de dirt.
* **Contraste**: *0.0 - 1.0*\
  Ajusta o contraste do resultado.
* **Variação**: *0.0 - 1.0* Combina a quantidade de máscaras/separações em grande escala que devem ocorrer.
* **Substituir máscara de variação**: *Falso/Verdadeiro*

## Imagens de exemplo

![](../../../../../../assets/edge-dirt-ex.gif)

</td>
</tr>
</table>
