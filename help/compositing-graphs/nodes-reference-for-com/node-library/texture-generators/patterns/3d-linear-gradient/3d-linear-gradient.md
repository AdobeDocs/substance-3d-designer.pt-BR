---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-linear-gradient.html"
breadcrumb-title: ''
description: Use o nó 3D linear gradient para criar gradientes lineares com base na posição do mundo 3D para efeitos espaciais.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Linear Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D linear gradient
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---


# 3D linear gradient

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-linear-gradient.png){width="128px"}

## 3D linear gradient

**Entrada:** *Geradores De Textura**/Padrões*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Cria um gradiente volumétrico com base no mapa de posição de entrada. Gera efetivamente uma transição de preto para branco entre 2 pontos no espaço 3D. Projetado para uso apenas com o mecanismo de GPU.

Consulte também [Máscara de volume 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) para obter um efeito semelhante.

## Parâmetros

* **Modo de Posição de Pontos**: *Posições UV, Posições Mundiais de Espaço* Escolha se os Pontos de Gradiente funcionam melhor no Espaço UV (funcionam melhor ao defini-los na exibição 2D) ou em coordenadas 3D, se desejar inserir manualmente uma posição exata.
* **Ponto 1**:\
  Ponto inicial do gradiente. Podem ser coordenadas 2D ou 3D com base no modo de posição.
* **Ponto 2**:\
  Ponto final do gradiente. Podem ser coordenadas 2D ou 3D com base no modo de posição.
* **Contraste**: *0.0 - 1.0*\
  Ajusta o contraste do resultado.

## Imagens de exemplo

![](../../../../../../assets/3d-gradient.gif)

</td>
</tr>
</table>
