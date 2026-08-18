---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/light.html"
breadcrumb-title: ''
description: Use o nó Luz para gerar máscaras com base nas condições de iluminação de malha a fim de criar variações de material realistas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luz
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 3%

---


# Luz

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/light-2.png){width="128px"}

## Luz

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara é um pouco diferente de outros Geradores: ela faz puramente iluminação falsa, com base no World Space Normalmap, retornando uma máscara “lightmap” em preto e branco.

## Parâmetros

* **Ângulo horizontal**: *0.0 - 1.0* Define o ângulo horizontal da luz falsa.
* **Ângulo vertical**: *0.0 - 1.0* Define o ângulo vertical da luz falsa.
* **Brilho do realce**: *0.0 - 0.999* Define a dispersão da área realçada.
* **Nível de Realce**: *0.0 - 1.0* Define o nível de brilho da área realçada.

## Imagens de exemplo

![](../../../../../../assets/light-ex.gif)

</td>
</tr>
</table>
