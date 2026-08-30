---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-blend.html"
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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 6%

---


# Mesclagem de material

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-blend.resources/material-blend.png){width="128px"}

<b>Em:</b> Filtros Materiais > Mesclagem

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

A Mesclagem de Material é o Equivalente de Material Completo Multicanal do [nó de mesclagem atômica](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md). Ela mescla entre dois materiais completos (todos os canais possíveis) com base em uma máscara em tons de cinza ou, opcionalmente, com base em uma única cor de uma Máscara de identificação de cores.

Esse nó é útil se você deseja mesclar dois materiais e ter um mapa em tons de cinza, mas não uma ID de cor completa. Se você tiver uma torta de ID de cor e quiser mesclar mais de dois materiais, sugerimos que você use a [Mesclagem de vários materiais](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>ColorID</b> <i>Entrada de cores</i> | Mapa opcional de ID de cor cozida. |
| <b>Máscara em tons de cinza</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Canais</b> | Ative e desative os canais de material neste grupo ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza, por exemplo. |
| <b>Difusa</b> |  |
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Mesclar opacidade entre o primeiro plano e o plano de fundo |
| <b>Modo de Mesclagem</b> <i>Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar</i> |  |
| <b>Cor base</b> |  |
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Mesclar opacidade entre o primeiro plano e o plano de fundo |
| <b>Modo de Mesclagem</b> <i>Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar</i> |  |
| <b>Normal</b> |  |
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Mesclar opacidade entre o primeiro plano e o plano de fundo |
| <b>Specular</b> |  |
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Mesclar opacidade entre o primeiro plano e o plano de fundo |
| <b>Modo de Mesclagem</b> <i>Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar</i> |  |
| <b>Emissivo</b> |  |
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Mesclar opacidade entre o primeiro plano e o plano de fundo |
| <b>Modo de Mesclagem</b> <i>Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar</i> |  |
| <b>Textura reluzente</b> |  |
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Mesclar opacidade entre o primeiro plano e o plano de fundo |
| <b>Modo de Mesclagem</b> <i>Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar</i> |  |
| <b>Aspereza</b> |  |
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Mesclar opacidade entre o primeiro plano e o plano de fundo |
| <b>Modo de Mesclagem</b> <i>Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar</i> |  |
| <b>Metálico</b> |  |
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Mesclar opacidade entre o primeiro plano e o plano de fundo |
| <b>Modo de Mesclagem</b> <i>Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar</i> |  |
| <b>Specular level</b> |  |
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Mesclar opacidade entre o primeiro plano e o plano de fundo |
| <b>Modo de Mesclagem</b> <i>Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar</i> |  |
| <b>Oclusão de ambiente</b> |  |
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Mesclar opacidade entre o primeiro plano e o plano de fundo |
| <b>Modo de Mesclagem</b> <i>Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar</i> |  |
| <b>Height</b> |  |
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Mesclar opacidade entre o primeiro plano e o plano de fundo |
| <b>Modo de Mesclagem</b> <i>Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar</i> |  |
| <b>Opacidade</b> |  |
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Mesclar opacidade entre o primeiro plano e o plano de fundo |
| <b>Modo de Mesclagem</b> <i>Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar</i> |  |
| <b>Máscara de identificação de cores</b> <i>Falso/Verdadeiro</i> | Use Máscara de identificação de cores em vez de máscara em tons de cinza. Lembre-se de que isso é apenas para uma cor! |
| <b>Cor</b> <i>(Valor da cor)</i> | Qual cor escolher e converter em branco. |
| <b>Grau de seleção</b> <i>0.01 - 1.0</i> | A extensão com que a cor selecionada é misturada com seus vizinhos. |
| <b>Preenchimento</b> <i>0.0 - 1.0</i> | Contraste de transição da cor escolhida. |
