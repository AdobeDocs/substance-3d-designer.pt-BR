---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/rust-weathering.html"
breadcrumb-title: ''
description: Use o nó de intemperismo de Ferrugem para gerar padrões de ferrugem com base na geometria da malha a fim de criar efeitos realistas de corrosão metálica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Rust Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ferrugem intemperismo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 1%

---


# Ferrugem intemperismo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/rust-weathering.png){width="128px"}

## Ferrugem intemperismo

**Entrada:** *Geradores Baseados Em Malha**/Clima*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

## Parâmetros

### Entradas

* **Oclusão De Ambiente**: *Entrada Em Tons De Cinza*\
  Mapa baked usado para efeitos internos e mascaramento.
* **Curvatura**: *Entrada em tons de cinza*\
  Mapa baked usado para efeitos internos e mascaramento.
* **Posição**: *Entrada de cores*
* **Máscara** : *Entrada Em Tons De Cinza*\
  Slot de máscara usado para mascarar os efeitos do nó. Pode ser alternado com o parâmetro “Máscara”.

### Parâmetros

* **Canais**
  * Ative e desative os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza.
* **Avançado**
  * **Formato Normal**: *DirectX, OpenGL*\
    Alterna entre diferentes formatos de Mapas Normais (inverte o canal verde).
  * **Máscara**: *Falso/Verdadeiro*\
    Ativa ou desativa o uso do Mapa de máscaras.
* **Efeito**
  * **Propagação de Ferrugem**: *0.0 - 1.0*
  * **Espalhando Smoothness**: *0.0 - 1.0*
  * **Escala de danos do verniz**: *0.0 - 1.0*
  * **Intensidade de gotas**: *0.0 - 1.0*
  * **Quantidade de Amostras de Gotas**: *0 - 32*
  * **Smoothness de gotas**: *0.0 - 1.0*
* **Mesclagem**
  * **Intensidade Difusa**: *0.0 - 1.0*\
    Intensidade de mesclagem do Difusa.
  * **Intensidade de cor base**: *0.0 - 1.0*\
    Intensidade de mesclagem da Cor de base.
  * **Intensidade Normal**: *0.0 - 32.0*\
    Intensidade de mesclagem do Normal.
  * **Intensidade de Specular**: *0.0 - 1.0*\
    Intensidade de mistura do Specular.
  * **Intensidade de textura reluzente**: *0.0 - 1.0*\
    Intensidade de mistura da Textura reluzente.
  * **Intensidade de aspereza**: *0.0 - 1.0*\
    Intensidade de mistura da aspereza.
  * **Intensidade Metálica**: *0.0 - 1.0*\
    Intensidade de mistura do Metálico.
  * **Intensidade de Oclusão do ambiente**: *0.0 - 1.0*\
    Intensidade de mesclagem da Oclusão ambiente.
  * **Intensidade de Height**: *0.0 - 1.0*\
    Intensidade de mistura do Height.

## Imagens de exemplo

![](../../../../../../assets/rust-ex.gif)

</td>
</tr>
</table>
