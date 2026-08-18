---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-speckle.html"
breadcrumb-title: ''
description: Use o nó Manchas de borda para gerar padrões de desgaste manchados nas bordas da malha a fim de criar efeitos realistas de danos às bordas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Speckle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Speckle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 2%

---


# Edge Speckle

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/edge-speckle.png){width="128px"}

## Edge Speckle

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara representa as bordas com um leve respingo adicionado para quebrá-las. Consulte também [Dirt de borda](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md).

## Parâmetros

### Entradas

* **Curvatura**: *Entrada em tons de cinza*\
  Mapa baked usado para realce de Aresta. Obrigatório!
* **Máscara de Variação**: *Entrada em Tons de Cinza*\
  Slot de máscara opcional usado para mascarar os efeitos do nó. Ative com “substituir máscara de variação”.
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Nível**: *0.0 - 1.0*\
  Define a quantidade total de realce de borda.
* **Contraste**: *0.0 - 1.0*\
  Ajusta o contraste do resultado.
* **Seleção de borda**: *0.0 - 1.0* Define a influência de bordas convexas.
* **Variação**: *0.0 - 1.0* Define a extensão na qual a máscara de variação divide o efeito.
* **Substituir máscara de variação**: *Falso/Verdadeiro* Substitui a máscara interna pelo slot de entrada personalizado.

## Imagens de exemplo

![](../../../../../../assets/edge-speckle-ex.gif)

</td>
</tr>
</table>
