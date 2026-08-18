---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/season-filter.html"
breadcrumb-title: ''
description: Use o nó Filtro de estação para aplicar efeitos sazonais aos materiais para criar variações de primavera, verão, outono e inverno.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Season Filter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Filtro de Temporada
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---


# Filtro de Temporada

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/default-icon.png){width="128px"}

## Filtro de Temporada

**Entrada:** *Filtros/Efeitos de Material*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Este nó adiciona efeitos como um nível de água animado, neve, gelo e/ou musgo.

Lembre-se de que este é um filtro mais antigo que não deve ser totalmente correto para PBR. Ele é mantido principalmente por razões de legado/compatibilidade, embora ainda possa ser útil em alguns casos. Versões mais recentes corretas para PBR podem ser encontradas na [Snow Cover](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) e no [Water Level](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md).

O nó requer um conjunto adequado de entradas de material, principalmente com um Heightmap ou Normalmap detalhadamente.

## Parâmetros

### Entradas

* **Máscara** : *Entrada Em Tons De Cinza*\
  Slot de máscara usado para mascarar os efeitos do nó. Pode ser alternado com o parâmetro “Máscara”.

### Parâmetros

* **Canais**
  * Ative e desative os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza.
* **Avançado**
  * **Formato Normal**: *DirectX, OpenGL*\
    Alterna entre diferentes formatos de Mapas Normais (inverte o canal verde).
  * **Máscara**: *Falso/Verdadeiro*\
    Ativa ou desativa o uso do Mapa de máscaras.
  * **Intensidade da luz**: *0.0 - 1.0*\
    Intensidade da luz (simulada).
  * **Ângulo de Luz**: *0.0 - 1.0*\
    Ângulo de incidência da luz (falsa)
* **Efeito**
  * **Efeito do Height ou Normal**: *Height, Normal* Escolhe qual mapa de entrada orienta os efeitos.
  * **Nível da água**: *0.0 - 1.0* Aumenta ou diminui o nível da água com base nas informações de Height/Normal.
  * **Detalhes da Água**: *0.0 - 1.0* Define a quantidade de detalhes na água.
  * **Refração**: *0.0 - 1.0* Define a quantidade de refração falsa no efeito.
  * **Reflexo**: *0.0 - 1.0* Define a quantidade de reflexo falso no efeito.
  * **Distância de Reflexo**: *0.0 - 1.0* Controla os visuais de reflexo.
  * **Ângulo de Reflexo**: *0.0 - 1.0* Controla os visuais de reflexo.
  * **Direção do fluxo**: *0.0 - 1.0* Controla o fluxo de animação (use Substance Player para visualizar).
  * **Gelo**: *0.0 - 1.0* Define o quanto a água está congelada.
  * **Detalhes do Gelo**: *0.0 - 1.0* Define a quantidade de detalhes no gelo.
  * **Snow**: *0.0 - 1.0* Define a quantidade de cobertura de neve.
  * **Moss**: *0.0 - 1.0* Define a quantidade de cobertura de musgo.
  * **Escala do musgo**: *1 - 4* Define a escala da textura do musgo gerada.
  * **Cor do musgo**: *(valor da cor)*Define a cor do musgo.
  * **Cor da água**: *(valor da cor)*Define a cor da água, incluindo alfa/opacidade.
* **Mesclagem**
  * **Intensidade Difusa**: *0.0 - 1.0*\
    Intensidade de mesclagem do Difusa.
  * **Intensidade de cor base**: *0.0 - 1.0*\
    Intensidade de mesclagem da Cor de base.
  * **Intensidade Normal**: *0.0 - 1.0*\
    Intensidade de mesclagem do Normal.
  * **Intensidade de Specular**: *0.0 - 1.0*\
    Intensidade de mistura do Specular.
  * **Intensidade de textura reluzente**: *0.0 - 1.0*\
    Intensidade de mistura da Textura reluzente.
  * **Intensidade de aspereza**: *0.0 - 1.0*\
    Intensidade de mistura da aspereza.
  * **Intensidade de Oclusão do ambiente**: *0.0 - 1.0*\
    Intensidade de mesclagem da Oclusão ambiente.
  * **Intensidade de Height**: *0.0 - 1.0*\
    Intensidade de mistura do Height.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
