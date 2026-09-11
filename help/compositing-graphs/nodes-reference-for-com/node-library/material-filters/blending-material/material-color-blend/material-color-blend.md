---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-color-blend.html"
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
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 2%

---


# Mistura de cores do material

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-color-blend.resources/material-color-blend.png){width="128px"}

<b>Em:</b> Filtros Materiais > Mesclagem

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Este nó permite ajustes em um material completo multicanal por meio da mistura de cores sólidas na parte superior. Essa é a principal diferença com a [Mesclagem de ajuste de material](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-adjustment-blend/material-adjustment-blend.md), que permite somente ajustes do tipo [Níveis](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) em canais, enquanto esse nó usa ajustes do tipo [Mesclar](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) com uma cor sólida.

Esse nó é mais útil quando você quer introduzir uma dica de cor simples em Cor difusa ou Cor base, ou quer “nivelar” outros canais usando um valor de cor sólido definido.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>ColorID</b> <i>Entrada de cores</i> | Slot de máscara usado para mascarar os efeitos do nó. |
| <b>Máscara em tons de cinza</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Canais</b> | Ative e desative os canais de material neste grupo ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza, por exemplo. |
| <b>Difusa</b> |  |
| <b>Cor</b> <i>(Valor da cor)</i> | Qual valor de cor deve ser mesclado sobre o canal da Difusão. |
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Mesclar opacidade entre primeiro plano e plano de fundo. |
| <b>Modo de Mesclagem</b> <i>Normal, Adicionar, Subtrair, Multiplicar, Adicionar/Sub, Máx, Mín, Alternar</i> | modo Combinar a ser usado na operação. |
| <b>Cor base</b> | Combinar uma cor sólida em cima deste canal com opções como no grupo de Difusões. |
| <b>Normal</b> |  |
| <b>Origem</b> <i>Height, Máscara</i> |  |
| <b>Modo de Mesclagem</b> <i>Combinar, Combinar</i> |  |
| <b>Intensidade de Height</b> <i>0.0 - 1.0</i> |  |
| <b>Opacidade do Height</b> <i>0.0 - 1.0</i> |  |
| <b>Formato</b> <i>DirectX, OpenGL</i> |  |
| <b>Specular</b> | Combinar uma cor sólida em cima deste canal com opções como no grupo de Difusões. |
| <b>Emissivo</b> | Combinar uma cor sólida em cima deste canal com opções como no grupo de Difusões. |
| <b>Textura reluzente</b> | Combinar uma cor sólida em cima deste canal com opções como no grupo de Difusões. |
| <b>Aspereza</b> | Combinar uma cor sólida em cima deste canal com opções como no grupo de Difusões. |
| <b>Metálico</b> | Combinar uma cor sólida em cima deste canal com opções como no grupo de Difusões. |
| <b>Specular level</b> | Combinar uma cor sólida em cima deste canal com opções como no grupo de Difusões. |
| <b>Oclusão de ambiente</b> | Combinar uma cor sólida em cima deste canal com opções como no grupo de Difusões. |
| <b>Height</b> | Mescla uma cor sólida sobre este canal com opções como no grupo Difuso. |
| <b>Opacidade</b> | Mescla uma cor sólida sobre este canal com opções como no grupo Difuso. |
| <b>Máscara de identificação de cores</b> <i>Falso/Verdadeiro</i> | Use Máscara de identificação de cores em vez de máscara em tons de cinza. Lembre-se de que isso é apenas para uma cor!<br><br>Habilita todas as opções abaixo. |
| <b>Cor</b> <i>(Valor da cor)</i> | Qual cor escolher e converter em branco. |
| <b>Grau de seleção</b> <i>0.01 - 1.0</i> | A extensão com que a cor selecionada é misturada com seus vizinhos. |
| <b>Preenchimento</b> <i>0.0 - 1.0</i> | Contraste de transição da cor escolhida. |
