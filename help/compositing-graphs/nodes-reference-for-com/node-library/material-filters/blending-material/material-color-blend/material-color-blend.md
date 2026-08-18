---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-color-blend.html"
breadcrumb-title: ''
description: Use o nó Mesclagem de cores de material para mesclar canais de cores entre materiais para criar efeitos de material composto.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Color Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mistura de cores do material
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---


# Mistura de cores do material

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-color-blend.png){width="128px"}

## Mistura de cores do material

**Entrada:** *Filtros/Mesclagem de Material*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Este nó permite ajustes em um material completo multicanal por meio da mistura de cores sólidas na parte superior. Essa é a principal diferença com a [Mesclagem de ajuste de material](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-adjustment-blend/material-adjustment-blend.md), que permite somente ajustes do tipo [Níveis](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) em canais, enquanto esse nó usa ajustes do tipo [Mesclar](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) com uma cor sólida.

Esse nó é mais útil quando você quer introduzir uma dica de cor simples em Cor difusa ou Cor base, ou quer “nivelar” outros canais usando um valor de cor sólido definido.

## Parâmetros

### Entradas

* **ColorID**: *Entrada de cor*\
  Slot de máscara usado para mascarar os efeitos do nó.
* **Máscara em tons de cinza**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Canais**
  * Ative e desative os canais de material neste grupo ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza, por exemplo.
* **Difusa**
  * **Cor**: *(valor da cor)*Qual valor de cor mesclar sobre o Canal Difuso.
  * **Opacidade**: *0.0 - 1.0*\
    Mesclar opacidade entre primeiro plano e plano de fundo.
  * **Modo de Mesclagem**: *Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar* Modo de mesclagem a ser usado na operação.
* **Cor base**
  * Mescla uma cor sólida sobre este canal com opções como no grupo Difuso.
* **Normal**
  * **Origem**: *Height, Máscara*
  * **Modo de Mesclagem**: *Combinar, Mesclar*
  * **Intensidade de Height**: *0.0 - 1.0*
  * **Opacidade Do Height**: *0.0 - 1.0*
  * **Formato**: *DirectX, OpenGL*
* **Specular**
  * Mescla uma cor sólida sobre este canal com opções como no grupo Difuso.
* **Emissivo**
  * Mescla uma cor sólida sobre este canal com opções como no grupo Difuso.
* **Textura reluzente**
  * Mescla uma cor sólida sobre este canal com opções como no grupo Difuso.
* **Aspereza**
  * Mescla uma cor sólida sobre este canal com opções como no grupo Difuso.
* **Metálico**
  * Mescla uma cor sólida sobre este canal com opções como no grupo Difuso.
* **Specular level**
  * Mescla uma cor sólida sobre este canal com opções como no grupo Difuso.
* **Oclusão de ambiente**
  * Mescla uma cor sólida sobre este canal com opções como no grupo Difuso.
* **Height**
  * Mescla uma cor sólida sobre este canal com opções como no grupo Difuso.
* **Opacidade**
  * Mescla uma cor sólida sobre este canal com opções como no grupo Difuso.
* **Máscara de identificação de cores**: *Falso/Verdadeiro* Use Máscara de identificação de cores em vez de máscara em tons de cinza. Lembre-se de que isso é apenas para uma cor!\
  Ativa todas as opções abaixo.
* **Cor**: *(valor da cor)*Qual cor escolher e converter em branco.
* **Grau de seleção**: *0.01 - 1.0* A extensão com que a cor escolhida é mesclada em seus vizinhos.
* **Preenchimento**: *0.0 - 1.0* Contraste de transição da cor escolhida.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
