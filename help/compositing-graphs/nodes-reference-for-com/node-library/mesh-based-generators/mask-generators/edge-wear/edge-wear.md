---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-wear.html"
breadcrumb-title: ''
description: Use o nó Edge Wear para gerar máscaras de desgaste nas bordas da malha a fim de criar efeitos realistas de danos nas bordas e de intemperismo.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---


# Edge Wear

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-wear.png){width="128px"}

## Edge Wear

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Este nó representa desgaste nas bordas do objeto. Tem alguns parâmetros, mas não é o mais fácil de usar: recomendamos que você brinque e tenha uma ideia das coisas. O nó é bastante poderoso, embora nenhuma máscara de substituição personalizada possa ser feita.

## Parâmetros

### Entradas

* **Curvatura**: *Entrada em tons de cinza*\
  Mapa baked usado para efeitos internos e mascaramento
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Nível**: *0.0 - 1.0*\
  Define a propagação total do efeito.
* **Contraste**: *0.0 - 1.0*\
  Ajusta o contraste do resultado.
* **Limite**: *0.0 - 1.0* Semelhante ao Nível, define a propagação total do efeito.
* **Largura das bordas**: *0.0 - 1.0* Define a plenitude do efeito de realce. Reduza para torná-los mais dispersos.
* **Desordem**: *0.0 - 1.0*\
  Define a quantidade de ruído a ser mesclada para quebrar o smoothness.

## Imagens de exemplo

![](../../../../../../assets/edge-wear-ex.gif)

</td>
</tr>
</table>
