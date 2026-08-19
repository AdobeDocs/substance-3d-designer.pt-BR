---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/selective-dirt.html"
breadcrumb-title: ''
description: Use o nó Dirt seletivo para gerar máscaras de acumulação de dirt seletivo com base na geometria de malha para tempo realista.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Selective Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dirt seletivo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 5%

---


# Dirt seletivo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/selective-dirt.png){width="128px"}

## Dirt seletivo

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Esta máscara do [Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html) representa um efeito de dirt simples em bordas convexas.

## Parâmetros

### Entradas

* **Curvatura**: *Entrada em tons de cinza*\
  Mapa baked usado para efeitos internos e mascaramento.
* **Máscara de Variação**: *Entrada em Tons de Cinza*\
  O mapa de variação opcional pode ser ativado por meio de parâmetros.
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Nível**: *0.0 - 1.0*\
  Define o nível total do efeito, revelando gradualmente.
* **Contraste**: *0.0 - 1.0*\
  Ajusta o contraste do resultado.
* **Variação**: *0.0 - 1.0* Define a quantidade de variação/desgaste a ser mesclada no efeito.
* **Substituir máscara de variação**: *Falso/Verdadeiro* Permite substituir a variação por um slot de entrada personalizado.

## Imagens de exemplo

![](../../../../../../assets/selective-dirt-ex.gif)

</td>
</tr>
</table>
