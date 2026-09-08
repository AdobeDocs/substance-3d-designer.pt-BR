---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-simplex-noise.html"
breadcrumb-title: ''
description: Use o nó Ruído simples 3D para gerar padrões de ruído simples 3D para criar texturas volumétricas suaves e de aparência natural.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Simplex Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruído simples 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---


# Ruído simples 3D

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-simplex-noise.png){width="128px"}

## Ruído simples 3D

**Entrada:** *Geradores De Textura**/Ruídos*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera um ruído processual quando um Mapa de posições feito bake é conectado ao slot de entrada. Ele deve ser usado somente com o mecanismo de GPU.\
Semelhante ao [Ruído de Perlin 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md), mas mais rápido e simples, para casos em que o desempenho e a velocidade são importantes.

Esse ruído pode ser testado com [GBuffers 3D de cubo](https://support.allegorithmic.com/documentation/display/SDDOC/Cube+3D+GBuffers) como entrada em vez de um mapa baked real (conforme mostrado na imagem de exemplo abaixo).

## Parâmetros

* **Escala**: *0.0 - 64.0*\
  Defina a escala global para o efeito.
* **Tamanho**: *0.0 - 2.0* Execute um dimensionamento não uniforme nos eixos X, Y e Z separadamente.

## Imagens de exemplo

![](../../../../../../assets/3d-simplex.gif)

</td>
</tr>
</table>
