---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/cloth-wear.html"
breadcrumb-title: ''
description: Use o nó Desgaste de pano para gerar máscaras de desgaste em superfícies de pano com base na curvatura da malha e nas áreas de contato.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Cloth Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desgaste de pano
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 2%

---


# Desgaste de pano

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/cloth-wear.png){width="128px"}

## Desgaste de pano

**Entrada:** *Geradores Baseados Em Malha**/Geradores De Máscara*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

A máscara representa bordas congeladas em materiais de tecido. Ele usa um mapa de altura de detalhe de pano que determina a maior parte da aparência; sem um mapa apropriado, o efeito parece muito básico.

## Parâmetros

### Entradas

* **Height De Pano**: *Entrada Em Tons De Cinza*\
  Height somente para o padrão de tecido. Esse não é o height do objeto (assado), mas sim um padrão de detalhes de revestimento.
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.
* **Curvatura**: *Entrada em tons de cinza*\
  Curvatura assada/gerada para determinar bordas elevadas.

### Parâmetros

* **Quantidade de Bordas Rígidas**: *0.0 - 1.0*
* **Suavidade de desgaste**: *0.0 - 5.0* Determina o quão desfocadas/suaves são as bordas gastas.

## Imagens de exemplo

![](../../../../../../assets/cloth-wear-ex.gif)

</td>
</tr>
</table>
