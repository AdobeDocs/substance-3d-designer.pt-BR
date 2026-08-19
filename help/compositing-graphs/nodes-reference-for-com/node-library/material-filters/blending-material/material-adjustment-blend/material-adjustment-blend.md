---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-adjustment-blend.html"
breadcrumb-title: ''
description: Use o nó Mesclagem de ajuste de material para mesclar ajustes de material entre materiais a fim de ajustar os efeitos compostos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Adjustment Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mesclagem de ajuste de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

---


# Mesclagem de ajuste de material

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-adjustment-blend.png){width="128px"}

## Mesclagem de ajuste de material

**Entrada:** *Filtros/Mesclagem de Material*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Este nó permite o ajuste de todos e quaisquer canais de um material completo, com base em uma máscara. Destina-se a tornar um fluxo de trabalho de material completo mais fácil e rápido.

É útil quando você deseja ajustar alguns canais de um material (como tornar difuso mais claro e aspereza mais escuro) com base na mesma máscara.

## Parâmetros

### Entradas

* **Máscara de identificação de cores**: *Entrada de cores*\
  Slot de máscara usado para mascarar os efeitos do nó.
* **Máscara em tons de cinza**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Canais**\
  Ativa e desativa os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza.\
  Isso também ativa e desativa a aparência dos grupos relevantes do canal.
* **Difusa**\
  Executa operações de ajuste no canal Difuso, em áreas definidas pela máscara.
* **Cor base**\
  Executa operações de ajuste no canal Cor base, em áreas definidas pela máscara.
* **Normal**
  * **Intensidade**: *0.0 - 1,0* Reduz a Intensidade Normal
* **Specular**\
  Executa operações de ajuste no canal de Specular, em áreas definidas pela máscara.
* **Emissivo**\
  Executa operações de ajuste no canal Emissivo, em áreas definidas pela máscara.
* **Textura reluzente**\
  Executa operações de ajuste no canal de Textura reluzente, em áreas definidas pela máscara.
* **Aspereza**\
  Executa operações de ajuste no canal de Aspereza, em áreas definidas pela máscara.
* **Metálico**\
  Executa operações de ajuste no canal Metálico, em áreas definidas pela máscara.
* **Specular level**\
  Executa operações de ajuste no canal do Specular level, em áreas definidas pela máscara.
* **Oclusão de ambiente**\
  Executa operações de ajuste no canal Oclusão ambiente, em áreas definidas pela máscara.
* **Height**\
  Executa operações de ajuste no canal do Height, em áreas definidas pela máscara.
* **Opacidade**\
  Executa operações de ajuste no canal Opacidade, em áreas definidas pela máscara.
* **Máscara de identificação de cores**: *Falso/Verdadeiro* Defina para usar Máscara de identificação de cores em vez de máscara em tons de cinza.
* **Grau de seleção**: *0.01 - 1.0* Se a Máscara de identificação de cores estiver habilitada, ela determinará a propagação da cor de seleção da ID de Cor.
* **Cor**: *(valor da cor)*Define a cor a ser escolhida no mapa de ID de cor e na máscara.
* **Preenchimento**: *0.0 - 1.0* Determina o contraste/transições de mesclagem do mascaramento de ID de cor.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
