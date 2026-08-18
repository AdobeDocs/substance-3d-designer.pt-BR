---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/cracks-weathering.html"
breadcrumb-title: ''
description: Use o nó de intemperismo do Rachadura para adicionar padrões de fissura a materiais baseados em curvatura de malha e pontos de tensão.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Cracks Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rachadura Weathering
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 1%

---


# Rachadura Weathering

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/cracks-weathering.png){width="128px"}

## Rachadura Weathering

**Entrada:** *Geradores Baseados Em Malha**/Clima*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Esse é um efeito de material completo que funciona em vários canais de uma só vez. Ele adiciona um padrão de rachadura aleatório, com controle sobre a propagação e a profundidade.

Certifique-se de entender corretamente os [Modos de Criação de Link](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) ao trabalhar com materiais completos.

## Parâmetros

### Entradas

* **Curvatura**: *Entrada em tons de cinza*\
  Mapa cozido ou gerado usado para efeitos internos e mascaramento.
* **Height** : *Entrada em Tons de Cinza*\
  Mapa cozido ou gerado usado para efeitos internos e mascaramento.
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
  * **Propagação do Rachadura**: *0.0 - 1.0* Até onde o rachadura deve se espalhar. Esse é o principal controle desse efeito.
  * **Profundidade do Rachadura**: *0.0 - 1.0* Profundidade do efeito de rachadura. Isso afeta principalmente o height e afeta ligeiramente o thickness visual.
* **Mesclagem**
  * Controla a intensidade de mesclagem do efeito em cada canal resultante.

## Imagens de exemplo

![](../../../../../../assets/cracks-ex.gif)

</td>
</tr>
</table>
