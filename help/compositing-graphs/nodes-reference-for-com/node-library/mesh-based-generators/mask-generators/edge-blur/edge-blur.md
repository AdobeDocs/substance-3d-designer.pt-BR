---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-blur.html"
breadcrumb-title: ''
description: Use o nó Desfoque de borda para desfocar máscaras de aresta para criar transições suaves e efeitos de intemperismo baseados em borda suave.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desfoque de borda
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# Desfoque de borda

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-blur.png){width="128px"}

## Desfoque de borda

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara realça as bordas com base em um mapa de curvatura assado. É um dos geradores de máscaras mais simples.

## Parâmetros

### Entradas

* **Curvatura**: *Entrada em tons de cinza*\
  Mapa baked usado para basear o efeito.
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Nível**: *0.0 - 1.0*\
  Define a intensidade de realce de borda.
* **Contraste**: *0.0 - 1.0*\
  Ajusta o contraste do resultado.
* **Raio de desfoque**: *0.0 - 8.0* Define a quantidade de desfoque nas bordas destacadas.

## Imagens de exemplo

![](../../../../../../assets/edge-blur-ex.gif)

</td>
</tr>
</table>
