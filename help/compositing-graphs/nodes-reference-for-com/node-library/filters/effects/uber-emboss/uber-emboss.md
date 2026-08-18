---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/uber-emboss.html"
breadcrumb-title: ''
description: Use o nó Entalhe Uber para criar efeitos avançados de entalhe com controles personalizáveis de profundidade, ângulo e iluminação.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Uber Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Entalhe Uber
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 2%

---


# Entalhe Uber

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/uber-emboss.png){width="128px"}

## Entalhe Uber

**Entrada:** *Filtros/Efeitos*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Versão avançada, repleta de recursos do [Entalhe](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md). Executa um elaborado efeito de iluminação falso em 2D com base em um mapa de altura.

Útil ao criar iluminação preparada para determinados estilos de texturização quando muito controle é necessário.

## Parâmetros

### Entradas

* **Cor**: *Entrada de cores*\
  Imagem base para modificar.
* **Height**: *Entrada em Tons de Cinza*\
  Mapa de altura usado como driver para o efeito.

### Parâmetros

* **Cor do ambiente**: *(valor da cor)*Cor usada em áreas sombreadas.
* **Cor difusa**: *(valor da cor)*Cor usada em áreas iluminadas.
* **Cor do Specular**: *(valor da cor)*Cor usada para reflexões de specular
* **Intensidade da luz**: *0.0 - 1.0*\
  Intensidade da luz (simulada).
* **Ângulo de Luz**: *0.0 - 1.0*\
  Ângulo de incidência da luz (falsa)
* **Intensidade de Specular**: *0.0 - 1.0* Intensidade de reflexos de specular.
* **Textura reluzente do Specular**: *0.0 - 1.0* Tamanho de destaque do specular.
* **Aspereza difusa**: *0.0 - 1.0* Aspereza usada no cálculo da iluminação difusa.
* **Opacidade das sombras**: *0.0 - 1.0* Opacidade de mistura das áreas sombreadas.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/uberemboss-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
