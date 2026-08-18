---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-patch.html"
breadcrumb-title: ''
description: Use o nó Fazer patch de bloco para aplicar patch e criar texturas de revestimento perfeitas a partir de imagens de entrada.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tornar um patch de bloco
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# Tornar um patch de bloco

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/make-it-tile-patch.png)

![](../../../../../../assets/make-it-tile-patch-grayscale.png)

## Torná-lo um patch de bloco (tons de cinza)

**Entrada:** *Filtros/Divisão em blocos*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Este nó é um ladrilho semialeatório baseado em grade. Ele usa um patch de entrada e o carimba, tentando transformá-lo em uma imagem lado a lado sem muitas repetições, com base nas suas configurações.

Útil para quando você tem um pequeno pedaço de textura e deseja criar uma escala maior, textura de divisão em blocos gráficos a partir dele.

Lembre-se de que isso é diferente de [Make-It-Tile Photo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md), que corrige principalmente as bordas.

Para fazer isso com um material inteiro, consulte [Bloco Automático Inteligente](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/smart-auto-tile/smart-auto-tile.md).

## Parâmetros

* **Tamanho da máscara**: *0.0 - 1.0* Tamanho da máscara redonda usada ao carimbar a correção.
* **Precisão da Máscara**: *0.0 - 1.0* Precisão de queda/smoothness da máscara.
* **Distorção de máscara**: *-100.0 - 100.0* Introduz a distorção nas bordas da máscara. Bom para evitar transições suaves e indefinidas entre patches.
* **Largura do tamanho do padrão**: *0.0 - 1000.0* Altera a largura do patch de maneira não uniforme.
* **height de tamanho de padrão**: *0.0 - 1000.0* Altera o height do patch de maneira não uniforme.
* **Desordem**: *0.0 - 1.0*\
  Apresenta a aleatoriedade translacional, alternando ligeiramente as manchas ao redor.
* **Variação de Tamanho**: *0.0 - 100.0* Introduz a variação de tamanho para a máscara.
* **Oitava**: *0 - 6* Este é o controle principal que determina o tamanho geral.
* **Rotação**: *-360.0 - 360.0* Pré-gira o patch.
* **Variação de Rotação**: *0.0 - 360.0* Introduz a rotação aleatória para cada carimbo de correção.
* **Cor do plano de fundo**: *(valor da cor)*Define a cor do plano de fundo para áreas em que nenhuma correção aparece.
* **Variação de cor**: *0.0 - 1.0 (somente versão de cor)*Introduz a variação de cor por correção.
* **Variação de luminosidade** *(somente versão em tons de cinza)*Introduz a variação de luminosidade por correção.

## Imagens de exemplo

![](../../../../../../assets/patch-ex.gif)

</td>
</tr>
</table>
