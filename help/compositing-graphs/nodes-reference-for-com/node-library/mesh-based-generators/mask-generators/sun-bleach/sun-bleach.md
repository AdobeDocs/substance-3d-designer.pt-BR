---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/sun-bleach.html"
breadcrumb-title: ''
description: Use o nó Desfoque do sol para gerar máscaras com base na exposição ao sol para criar efeitos realistas de desfoque e desbotado do sol.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Sun Bleach
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Branquear do Sol
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# Branquear do Sol

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/sun-bleach.png){width="128px"}

## Branquear do Sol

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara é semelhante a [Clara](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/light/light.md), mas também tem suporte para AO, levando a uma máscara que representa o branqueamento claro e o esmaecimento sobre um efeito.

## Entradas

* **Espaço Mundial Normal**: *Entrada De Cores*
* **Oclusão De Ambiente**: *Entrada Em Tons De Cinza*\
  Mapa baked usado para efeitos internos e mascaramento.
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

## Parâmetros

* **Nível**: *0.0 - 1.0*\
  Define a quantidade total de branqueamento, move o efeito para baixo.
* **Contraste**: *0.0 - 1.0*\
  Ajusta o contraste do resultado.
* **Oclusão**: *0.0 - 1.0* Define a influência do AO no resultado final.

## Imagens de exemplo

![](../../../../../../assets/sun-bleach-ex.gif)

</td>
</tr>
</table>
