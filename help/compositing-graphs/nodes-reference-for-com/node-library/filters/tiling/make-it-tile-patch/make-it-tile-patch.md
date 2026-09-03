---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-patch.html"
breadcrumb-title: ''
description: Use o nó Fazer patch de bloco para aplicar patch e criar texturas de revestimento perfeitas a partir de imagens de entrada.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tornar um patch de bloco
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 8%

---


# Tornar um patch de bloco

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](make-it-tile-patch.resources/make-it-tile-patch-01.png)

![](make-it-tile-patch.resources/make-it-tile-patch-02.png)

<b>Em:</b> Filtros > Lado a Lado

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Este nó é um ladrilho semialeatório baseado em grade. Ele usa um patch de entrada e o carimba, tentando transformá-lo em uma imagem lado a lado sem muitas repetições, com base nas suas configurações.

Útil para quando você tem um pequeno pedaço de textura e deseja criar uma escala maior, textura de divisão em blocos gráficos a partir dele.

Lembre-se de que isso é diferente de [Make-It-Tile Photo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md), que corrige principalmente as bordas.

Para fazer isso com um material inteiro, consulte [Bloco Automático Inteligente](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/smart-auto-tile/smart-auto-tile.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Tamanho da máscara</b> <i>0.0 - 1.0</i> | Tamanho da máscara redonda usada ao carimbar o patch. |
| <b>Precisão da Máscara</b> <i>0.0 - 1.0</i> | Precisão de queda/smoothness da máscara. |
| <b>Distorção de máscara</b> <i>-100.0 - 100.0</i> | Introduz a deformação nas bordas da máscara. Bom para evitar transições suaves e indefinidas entre patches. |
| <b>Largura do tamanho do padrão</b> <i>0.0 - 1000.0</i> | Altera a largura da correção de maneira não uniforme. |
| <b>height de tamanho de padrão</b> <i>0.0 - 1000.0</i> | Altera o height do patch de maneira não uniforme. |
| <b>Desordem</b> <i>0.0 - 1.0</i> | Apresenta a aleatoriedade translacional, alternando ligeiramente as manchas ao redor. |
| <b>Variação de Tamanho</b> <i>0.0 - 100.0</i> | Introduz a variação de tamanho para a máscara. |
| <b>Oitava</b> <i>0 - 6</i> | Esse é o controle principal que determina o tamanho geral. |
| <b>Rotação</b> <i>-360.0 - 360.0</i> | Gira previamente o patch. |
| <b>Variação de Rotação</b> <i>0.0 - 360.0</i> | Introduz uma rotação aleatória para cada carimbo de correção. |
| <b>Cor do plano de fundo</b> <i>(Valor da cor)</i> | Define a cor do plano de fundo para áreas em que nenhuma correção é exibida. |
| <b>Variação de cor</b> <i>0.0 - 1.0 (Somente Versão de Cores)</i> | Introduz a variação de cor por correção. |
| <b>Variação de luminosidade</b> <i>(somente versão em tons de cinza)</i> | Introduz a variação de luminosidade por correção. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="make-it-tile-patch.resources/make-it-tile-patch-03.gif" />
        </td>
    </tr>
</table>
