---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-blend.html"
breadcrumb-title: ''
description: Use o nó Mesclagem de materiais para mesclar materiais inteiros usando máscaras para criar efeitos de materiais compostos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mesclagem de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---


# Mesclagem de material

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-blend.png){width="128px"}

## Mesclagem de material

**Entrada:** *Filtros/Mesclagem de Material*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

A Mesclagem de Material é o Equivalente de Material Completo Multicanal do [nó de mesclagem atômica](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md). Ela mescla entre dois materiais completos (todos os canais possíveis) com base em uma máscara em tons de cinza ou, opcionalmente, com base em uma única cor de uma Máscara de identificação de cores.

Esse nó é útil se você deseja mesclar dois materiais e ter um mapa em tons de cinza, mas não uma ID de cor completa. Se você tiver uma torta de ID de cor e quiser mesclar mais de dois materiais, sugerimos que você use a [Mesclagem de vários materiais](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md).

## Parâmetros

### Entradas

* **ColorID**: *Entrada de cor*\
  Mapa opcional de ID de cor cozida.
* **Máscara em tons de cinza**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Canais**
  * Ative e desative os canais de material neste grupo ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza, por exemplo.
* **Difusa**
  * **Opacidade**: *0.0 - 1.0*\
    Mesclar opacidade entre o primeiro plano e o plano de fundo
  * **Modo De Mesclagem**: *Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar*
* **Cor base**
  * **Opacidade**: *0.0 - 1.0*\
    Mesclar opacidade entre o primeiro plano e o plano de fundo
  * **Modo De Mesclagem**: *Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar*
* **Normal**
  * **Opacidade**: *0.0 - 1.0*\
    Mesclar opacidade entre o primeiro plano e o plano de fundo
* **Specular**
  * **Opacidade**: *0.0 - 1.0*\
    Mesclar opacidade entre o primeiro plano e o plano de fundo
  * **Modo De Mesclagem**: *Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar*
* **Emissivo**
  * **Opacidade**: *0.0 - 1.0*\
    Mesclar opacidade entre o primeiro plano e o plano de fundo
  * **Modo De Mesclagem**: *Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar*
* **Textura reluzente**
  * **Opacidade**: *0.0 - 1.0*\
    Mesclar opacidade entre o primeiro plano e o plano de fundo
  * **Modo De Mesclagem**: *Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar*
* **Aspereza**
  * **Opacidade**: *0.0 - 1.0*\
    Mesclar opacidade entre o primeiro plano e o plano de fundo
  * **Modo De Mesclagem**: *Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar*
* **Metálico**
  * **Opacidade**: *0.0 - 1.0*\
    Mesclar opacidade entre o primeiro plano e o plano de fundo
  * **Modo De Mesclagem**: *Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar*
* **Specular level**
  * **Opacidade**: *0.0 - 1.0*\
    Mesclar opacidade entre o primeiro plano e o plano de fundo
  * **Modo De Mesclagem**: *Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar*
* **Oclusão de ambiente**
  * **Opacidade**: *0.0 - 1.0*\
    Mesclar opacidade entre o primeiro plano e o plano de fundo
  * **Modo De Mesclagem**: *Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar*
* **Height**
  * **Opacidade**: *0.0 - 1.0*\
    Mesclar opacidade entre o primeiro plano e o plano de fundo
  * **Modo De Mesclagem**: *Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar*
* **Opacidade**
  * **Opacidade**: *0.0 - 1.0*\
    Mesclar opacidade entre o primeiro plano e o plano de fundo
  * **Modo De Mesclagem**: *Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar*
* **Máscara de identificação de cores**: *Falso/Verdadeiro* Use Máscara de identificação de cores em vez de máscara em tons de cinza. Lembre-se de que isso é apenas para uma cor!
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
