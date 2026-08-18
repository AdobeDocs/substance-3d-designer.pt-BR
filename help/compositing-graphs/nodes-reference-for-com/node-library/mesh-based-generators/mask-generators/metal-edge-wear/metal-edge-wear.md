---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/metal-edge-wear.html"
breadcrumb-title: ''
description: Use o nó Edge Wear de metal para gerar máscaras de desgaste em bordas de metal com base na curvatura e posição da malha.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Metal Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Edge Wear de metal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---


# Edge Wear de metal

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/metal-edge-wear.png){width="128px"}

## Edge Wear de metal

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara representa o desgaste de bordas em um objeto metálico, com arranhões e lascas aparecendo em bordas convexas elevadas, potencialmente mascaradas por áreas escuras de AO assadas.

## Parâmetros

### Entradas

* **Curvatura**: *Entrada em tons de cinza*\
  Mapa baked usado para efeitos internos e mascaramento.
* **Oclusão De Ambiente**: *Entrada Em Tons De Cinza*\
  Mapa baked usado para efeitos internos e mascaramento.
* **Entrada de Desgaste**: *Entrada em Tons de Cinza*
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.
* **Espaço Mundial Normal**: *Entrada de Cores*
* **Posição**: *Entrada de cores*

### Parâmetros

* **Nível de desgaste**: *0.0 - 1.0* Define a quantidade total de desgaste, revela gradualmente.
* **Desgastar Contraste**: *0.0 - 1.0* Define o contraste do resultado final.
* **Smoothness de bordas**: *0.0 - 16.0* Define o smoothness da queda das bordas da Curvatura.
* **Quantidade de Desgaste**: *0.0 - 1.0* Define a quantidade de desgaste a ser mesclada entre as bordas.
* **Escala do Desgaste**: *1 - 16* Define a escala do Desgaste.
* **Mascaramento de Oclusão ambiente**: *0.0 - 1.0* Define a quantidade de efeito que o AO tem sobre o efeito final, e as áreas escuras são mascaradas.
* **Espessura da curvatura**: *0.0 - 1.0* Define a quantidade de efeito que as bordas convexas da curvatura têm sobre o efeito final.
* **Usar Desgaste Personalizado**: *Falso/Verdadeiro* Habilita um slot de entrada personalizado do mapa de Desgaste.
* **Usar Triplanar**: *Falso/Verdadeiro* Habilitar projeção [Triplanar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) para ocultar costuras.
* **Contraste de Mesclagem Triplanar**: *0.0 - 1.0* Define o contraste de mesclagem para a Projeção Triplanar.

## Imagens de exemplo

![](../../../../../../assets/metal-edge-wear-ex.gif)

</td>
</tr>
</table>
