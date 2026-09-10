---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/water-level.html"
breadcrumb-title: ''
description: Use o nó Nível da água para misturar materiais com base no height do nível da água para criar efeitos realistas da água.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Water Level
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nível da água
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 8%

---


# Nível da água

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](water-level.resources/water-level.png){width="128px"}

<b>Em:</b> Filtros Materiais > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Efeito multifuncional que adiciona um nível de água a uma entrada de material completa. O material de entrada deve ter um Heightmap de boa qualidade para que o efeito funcione. O resultado está correto para PBR.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Máscara</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Canais</b> | Ative e desative os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza. |
| <b>Nível de água</b> <i>0.0 - 1.0</i> | Controlo principal para elevar ou baixar o nível da água. |
| <b>Escuridão Hídrica</b> <i>0.0 - 1.0</i> | Define a “transparência” geral da água. |
| <b>Umidade das Bordas</b> <i>0.0 - 1.0</i> | Determina quanto de uma aparência molhada as bordas da água devem ter. |
| <b>Distância de Umidade das Bordas</b> <i>0.0 - 1.0</i> | Define o quanto as bordas molhadas atingem. |
| <b>Quantidade de Desfoque de Profundidade</b> <i>0.0 - 1.0</i> | Define a quantidade de desfoque com base na profundidade abaixo da água. Modifica o raio do desfoque. |
| <b>Opacidade do Desfoque de Profundidade</b> <i>0.0 - 1.0</i> | Determina quanto desfoque de profundidade é mesclado; pode ser usado para diminuir o efeito do desfoque. |
| <b>Cor de lodo</b> <i>(Valor da cor)</i> | Define a cor do efeito de lodo. |
| <b>Profundidade de lamas</b> <i>0.0 - 1.0</i> | Define a profundidade em que o lodo começa a aparecer, em relação ao nível da água. |
| <b>Opacidade do Lodo</b> <i>0.0 - 1.0</i> | Define a opacidade global do efeito de lodo. |
| <b>Geada</b> <i>0.0 - 1.0</i> | Define a quantidade de geada. Começa a aparecer a partir das bordas externas e se move para dentro. |
| <b>Intensidade de geada</b> <i>0.0 - 1.0</i> | Define a intensidade da geada, controla a “opacidade” do efeito. |
| <b>Rachaduras de geada</b> <i>0.0 - 1.0</i> | Define a quantidade de rachaduras nas transições de congelado para líquido. |
| <b>Formato Normal De Geada</b> <i>DirectX/OpenGL</i> | Alterna o canal verde do efeito Frost Normalmap. |
