---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-adjustment-blend.html"
breadcrumb-title: ''
description: Use o nó Combinar de ajuste de material para mesclar ajustes de material entre materiais para ajustar os efeitos compostos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Adjustment Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Combinar de ajuste de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 2%

---


# Combinar de ajuste de material

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-adjustment-blend.resources/material-adjustment-blend.png){width="128px"}

<b>Em:</b> Filtros Materiais > Mesclagem

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Este nó permite o ajuste de todos e quaisquer canais de um material completo, com base em uma máscara. Destina-se a tornar um fluxo de trabalho de material completo mais fácil e rápido.

É útil quando você deseja ajustar alguns canais de um material (como tornar difuso mais claro e aspereza mais escuro) com base na mesma máscara.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Máscara de identificação de cores</b> <i>Entrada de cores</i> | Slot de máscara usado para mascarar os efeitos do nó. |
| <b>Máscara em tons de cinza</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Canais</b> | Ativa e desativa os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza.<br><br>Isso também ativa e desativa a aparência dos grupos relevantes do canal. |
| <b>Difusões</b> | Executa operações de ajuste no canal da Difusão, em áreas definidas pela máscara. |
| <b>Cor de base</b> | Executa operações de ajuste no canal de Cor de base, em áreas definidas pela máscara. |
| <b>Normal</b> |  |
| <b>Intensidade</b> <i>0.0 - 1.0</i> | Reduz a intensidade normal |
| <b>Specular</b> | Executa operações de ajuste no canal de Specular, em áreas definidas pela máscara. |
| <b>Emissivo</b> | Executa operações de ajuste no canal Emissivo, em áreas definidas pela máscara. |
| <b>Textura reluzente</b> | Executa operações de ajuste no canal de Textura reluzente, em áreas definidas pela máscara. |
| <b>Aspereza</b> | Executa operações de ajuste no canal de Aspereza, em áreas definidas pela máscara. |
| <b>Metálico</b> | Executa operações de ajuste no canal Metálico, em áreas definidas pela máscara. |
| <b>Specular level</b> | Executa operações de ajuste no canal do Specular level, em áreas definidas pela máscara. |
| <b>Oclusão de ambiente</b> | Executa operações de ajuste no canal de Oclusão de ambiente, em áreas definidas pela máscara. |
| <b>Height</b> | Executa operações de ajuste no canal do Height, em áreas definidas pela máscara. |
| <b>Opacidade</b> | Executa operações de ajuste no canal Opacidade, em áreas definidas pela máscara. |
| <b>Máscara de identificação de cores</b> <i>Falso/Verdadeiro</i> | Defina para usar Máscara de identificação de cores em vez de máscara em tons de cinza. |
| <b>Grau de seleção</b> <i>0.01 - 1.0</i> | Se a Máscara de identificação de cores estiver ativada, isso determina a propagação da cor de seleção da ID de cor. |
| <b>Cor</b> <i>(Valor da cor)</i> | Define a cor a ser escolhida no mapa de ID de cor e na máscara. |
| <b>Preenchimento</b> <i>0.0 - 1.0</i> | Determina o contraste/transições de mesclagem do mascaramento de ID de cor. |
