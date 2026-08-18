---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/bottom-to-top.html"
breadcrumb-title: ''
description: Use o nó De baixo para cima para gerar máscaras de gradiente de baixo para cima com base na posição do mundo da malha.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Bottom To Top
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: De baixo para cima
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 1%

---


# De baixo para cima

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/bottom-to-top.png){width="128px"}

## De baixo para cima

**Entrada:** *Geradores Baseados Em Malha/Geradores De Máscara*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/features/smart-materials-and-masks) do [Painter](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/home).

Isso gera uma transição de branco para preto da parte inferior para a parte superior de um modelo, útil para fazer falhas e seleções baseadas em geometria.

## Parâmetros

### Entradas

* **Posição**: *Entrada de cores*\
  Mapa da posição cozida. Obrigatório!
* **Aspereza:** *Entrada em tons de cinza*\
  Isso não tem nada a ver com a rugosidade do PBR, mas é um mapa de variação (opcional) para quebrar a transição. Aparece somente quando a Aspereza está definida como maior que 0.
* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Nível**: *0.0 - 1.0*\
  Desloca o nível médio do resultado entre preto ou branco, como um ajuste de brilho.
* **Contraste**: *0.0 - 1.0*\
  Ajusta o contraste da transição.
* **Variação\_de_aspereza**: *0.0 - 1.0* Determina a quantidade do mapa de aspereza a ser mesclada para a variação. Aumentar isso em 0 revela o slot do mapa.

## Imagens de exemplo

![](../../../../../../assets/bottom-to-top-ex.gif)

</td>
</tr>
</table>
