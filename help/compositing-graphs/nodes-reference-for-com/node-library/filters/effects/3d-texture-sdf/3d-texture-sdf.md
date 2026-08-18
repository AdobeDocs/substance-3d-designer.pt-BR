---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-sdf.html"
breadcrumb-title: ''
description: Use o nó SDF de textura 3D para gerar texturas de campo de distância assinadas a partir de dados 3D para criar formas e efeitos suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture SDF
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SDF de textura 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# SDF de textura 3D

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf.png){width="200px"}

**Entrada:** *Filtro/Efeito*

**Simples**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrição

O nó **SDF** de Textura 3D gera o *campo de distância assinado* de uma forma a partir da máscara de textura *3D* da **Entrada** que representa as fatias do *volume* da forma.

</td>
</tr>
</table>

## Parâmetros

### Entradas

* **Entrada de máscara** *Tons de cinza*\
  A máscara de *textura 3D* que representa as fatias do *volume* de uma forma.

### Parâmetros

* **Limite** *Flutuante*\
  Quando o volume da forma é descrito por um *gradiente de desvanecimento*, define o valor do gradiente no qual a *superfície* da forma é *detectada*.
* **Saída** *Inteiro*\
  O tipo de campo de distância que deve ser gerado:
  * *Campo de distância*: gera um campo de distância que descreve as distâncias *fora* da forma.
  * *Campo de distância sinalizado*: gera um campo de distância que descreve as distâncias *fora* (positivas) e *dentro* (negativas) da forma.

## Imagens de exemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-node.png){width="256px"}

</td>
</tr>
</table>
