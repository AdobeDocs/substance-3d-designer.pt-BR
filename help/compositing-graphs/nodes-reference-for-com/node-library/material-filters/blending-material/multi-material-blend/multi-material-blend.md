---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/multi-material-blend.html"
breadcrumb-title: ''
description: Use o nó Mesclagem de vários materiais para mesclar vários materiais para criar combinações de materiais complexas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Multi-Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mesclagem de vários materiais
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 7%

---


# Mesclagem de vários materiais

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-material-blend.resources/multi-material-blend.png){width="128px"}

<b>Em:</b> Filtros Materiais > Mesclagem

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Este nó combina vários materiais com base em um mapa de ID de material/ID de cor, que pode ser cozido de uma malha. São necessários até 16 materiais completos diferentes, com qualquer tipo de canais que você ative no grupo Canais.

O nó é muito útil ao texturizar adereços completos, pois permite a parametrização completa de materiais enquanto ainda combina dinamicamente todos eles. Perfeito para texturizar adereços simples a complexos que têm bolos de ID adequados, ou até mesmo para criar Substance de “Modelo” totalmente pipeline que totalmente cohere aos padrões de equipe.

Lembre-se de que, ao usar isso, o Material 1, Slot 1 é sempre o material padrão e aparecerá em qualquer lugar em que nenhum outro material apareça. É por isso que não é possível configurar uma cor para ele. Se quiser jogar este cofre, você pode, por exemplo, conectar um [Material de base](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md) definido como preto áspero.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>1-16 slots de material completo</b> | A quantidade de slots é determinada pelo menu suspenso <b>Materiais</b>. |
| <b>ID de cor</b> <i>Entrada de cores</i> | Mapa de ID de cor assada. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Materiais</b> <i>2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16</i> | Define a quantidade máxima de diferentes materiais para mesclagem. |
| <b>Canais</b> | Ative e desative os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza. |
| <b>Material 2-16</b> | Um grupo é exibido para cada material ativado. |
| <b>Cor</b> <i>(Valor da cor)</i> | Cor para selecionar no mapa de ID que corresponde a este slot de material. |
| <b>Grau de seleção</b> <i>0.01 - 1.0</i> | Sangria para as cores vizinhas. |
| <b>Preenchimento</b> <i>0.0 - 1.0</i> | Dureza das transições: contraste da máscara. |
