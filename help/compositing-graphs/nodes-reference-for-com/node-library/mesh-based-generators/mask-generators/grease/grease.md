---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/grease.html"
breadcrumb-title: ''
description: Use o nó Graxa para gerar máscaras de acumulação de graxa com base na geometria da malha e nas áreas de contato.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Grease
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Graxa
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%

---


# Graxa

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/grease.png){width="128px"}

## Graxa

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara destina-se especificamente a faces de caracteres e outras áreas específicas. Gera um tipo de máscara de graxa de pele em áreas de baixo thickness.

## Parâmetros

### Entradas

* **Thickness**: *Entrada em Tons de Cinza*\
  Mapa de Thicknesss cozidos no qual todo o efeito é baseado. Obrigatório!
* **Ruído**: *Entrada em Tons de Cinza*\
  Mapa de ruído opcional para substituir o desgaste de graxa.
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Nível**: *0.0 - 1.0*\
  Define a quantidade total de efeito a ser exibida.
* **Contraste**: *0.0 - 1.0*\
  Ajusta o contraste do resultado.
* **Limite de Thickness**: *0.0 - 1.0* Define um thickness mínimo no qual o efeito deve aparecer. Igualmente importante como o Level; ajuste-o para se ajustar ao seu mapa de Thickness.
* **Substituir ruído**: *falso/verdadeiro* Defina para substituir o mapa de desgaste de graxa interno pelo slot de entrada personalizado.

## Imagens de exemplo

![](../../../../../../assets/grease-ex.gif)

</td>
</tr>
</table>
