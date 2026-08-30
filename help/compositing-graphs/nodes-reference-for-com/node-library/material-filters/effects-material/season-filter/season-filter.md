---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/season-filter.html"
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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 11%

---


# Filtro de Temporada

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](season-filter.resources/default-icon.png){width="128px"}

<b>Em:</b> Filtros Materiais > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Este nó adiciona efeitos como um nível de água animado, neve, gelo e/ou musgo.

Lembre-se de que este é um filtro mais antigo que não deve ser totalmente correto para PBR. Ele é mantido principalmente por razões de legado/compatibilidade, embora ainda possa ser útil em alguns casos. Versões mais recentes corretas para PBR podem ser encontradas na [Snow Cover](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) e no [Water Level](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md).

O nó requer um conjunto adequado de entradas de material, principalmente com um Heightmap ou Normalmap detalhadamente.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Máscara</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. Pode ser alternado com o parâmetro “Máscara”. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Canais</b> | Ative e desative os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza. |
| <b>Avançado</b> |  |
| <b>Formato Normal</b> <i>DirectX, OpenGL</i> | Alterna entre diferentes formatos de Mapas Normais (inverte o canal verde). |
| <b>Máscara</b> <i>Falso/Verdadeiro</i> | Ativa ou desativa o uso do Mapa de máscaras. |
| <b>Intensidade da luz</b> <i>0.0 - 1.0</i> | Intensidade da luz (simulada). |
| <b>Ângulo de luz</b> <i>0.0 - 1.0</i> | Ângulo de incidência da luz (falsa) |
| <b>Efeito</b> |  |
| <b>Efeito do Height ou Normal</b> <i>Height, Normal</i> | Escolhe qual mapa de entrada direciona os efeitos. |
| <b>Nível de água</b> <i>0.0 - 1.0</i> | Aumenta ou diminui o nível da água com base em informações de Height/Normal. |
| <b>Detalhes da Água</b> <i>0.0 - 1.0</i> | Define a quantidade de detalhes na água. |
| <b>Refração</b> <i>0.0 - 1.0</i> | Define a quantidade de refração falsa no efeito. |
| <b>Reflexo</b> <i>0.0 - 1.0</i> | Define a quantidade de reflexão falsa no efeito. |
| <b>Distância de Reflexo</b> <i>0.0 - 1.0</i> | Controla os visuais de reflexo. |
| <b>Ângulo de Reflexo</b> <i>0.0 - 1.0</i> | Controla os visuais de reflexo. |
| <b>Direção do Fluxo</b> <i>0.0 - 1.0</i> | Controla o fluxo de animação (use Substance Player para visualizar). |
| <b>Gelo</b> <i>0.0 - 1.0</i> | Define o quão congelada a água está. |
| <b>Detalhes do gelo</b> <i>0.0 - 1.0</i> | Define a quantidade de detalhes no gelo. |
| <b>Snow</b> <i>0.0 - 1.0</i> | Define a quantidade de cobertura de neve. |
| <b>Moss</b> <i>0.0 - 1.0</i> | Define a quantidade de cobertura de musgo. |
| <b>Escala do Moss</b> <i>1 - 4</i> | Define a escala da textura de musgo gerada. |
| <b>Cor do musgo</b> <i>(Valor da cor)</i> | Define a cor do musgo. |
| <b>Cor da água</b> <i>(Valor da cor)</i> | Define a cor da água, incluindo alfa/opacidade. |
| <b>Mesclagem</b> |  |
| <b>Intensidade de Difusão</b> <i>0.0 - 1.0</i> | Intensidade de mesclagem do Difusa. |
| <b>Intensidade de Cor de base</b> <i>0.0 - 1.0</i> | Intensidade de mesclagem da Cor de base. |
| <b>Intensidade normal</b> <i>0.0 - 1.0</i> | Intensidade de mesclagem do Normal. |
| <b>Intensidade de Specular</b> <i>0.0 - 1.0</i> | Intensidade de mistura do Specular. |
| <b>Intensidade de brilho</b> <i>0.0 - 1.0</i> | Intensidade de mistura da Textura reluzente. |
| <b>Intensidade de aspereza</b> <i>0.0 - 1.0</i> | Intensidade de mistura da aspereza. |
| <b>Intensidade de Oclusão de ambiente</b> <i>0.0 - 1.0</i> | Intensidade de mesclagem da Oclusão ambiente. |
| <b>Intensidade de Height</b> <i>0.0 - 1.0</i> | Intensidade de mistura do Height. |
