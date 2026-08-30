---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-mapper.html"
breadcrumb-title: ''
description: Use o nó Mapeador de Flood Fill para mapear valores em regiões conectadas usando algoritmos de preenchimento por inundação para processamento de textura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mapeador de Flood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 6%

---


# Mapeador de Flood Fill

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-mapper.resources/floodfill-mapper-gray.png)![](flood-fill-mapper.resources/floodfill-mapper-color.png)

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O Mapeador de Flood Fill permite o remapeamento de um Padrão ou Textura existente em cada célula de um [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md). É diferente de outras conversões de Flood Fill, como [Escala de cinza aleatória](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md) ou [Gradiente](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md), pois não gera cores ou valores sólidos, mas permite que você use seus próprios mapas de entrada. Ele pode ser visto como uma espécie de combinação de [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) e [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) ou [Mapeador de formas](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-mapper/shape-mapper.md), pois fornece alguns controles e interfaces semelhantes.

A versão Cor tem controles adicionais para trabalhar com Mapas Normais, onde pode [compensar rotações de Mapa de Normap do espaço tangente](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-vector-rotation/normal-vector-rotation.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Flood Fill Bbox</b> <i>Entrada de cores</i> | Entrada de Flood Fill padrão, necessária. |
| <b>Entrada de padrão 1-8</b> <i>Entrada em Tons de Cinza/Cores</i> | Entrada de imagem de padrão personalizado. |
| <b>Mapa de Distribuição de Padrões</b> <i>Entrada em tons de cinza</i> | Mapa de ID para determinar qual padrão vai para qual célula. Pode vir de outro Mapa de Flood Fill, como Flood Fill para Índice. |
| <b>Mapa de Escala</b> <i>Entrada em tons de cinza</i> | Mapa para determinar a Escala por célula. |
| <b>Mapa de rotação</b> <i>Entrada em tons de cinza</i> | Mapa para determinar a Rotação por Célula. |
| <b>Mapa de deslocamento de luminância</b> <i>Entrada em tons de cinza</i> | Mapa para definir a Luminância por Célula |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Modo Revestimento</b> <i>Sem divisão em blocos gráficos, H+V</i> | Define se deseja usar a divisão em blocos gráficos ou não. Visível apenas se Tamanho ou Escala estiverem definidos abaixo de 1. |
| <b>Padrão</b> |  |
| <b>Número de Entrada de Padrão</b> <i>1 - 8</i> | Defina a quantidade de Entradas de Padrão Personalizado a ser usada. |
| <b>Modo de Distribuição de Padrão</b> <i>Aleatório, Tamanho Da Forma, Entrada Do Mapa De Distribuição</i> | Defina o método para determinar qual Padrão é mostrado em uma Célula. |
| <b>Tremulação de Distribuição de Padrão</b> <i>0.0 - 1.0</i> | Permite uma pequena variação ou Deslocamento na distribuição do padrão sem alterar tudo pela Distribuição aleatória. |
| <b>Tamanho</b> |  |
| <b>Modo de Tamanho</b> <i>Em relação à Textura, em relação à forma BSphere, em relação à forma maior, em relação à forma menor, ajustar caixa de forma</i> | Define como o tamanho do padrão em cada célula é determinado. |
| <b>Tamanho</b> <i>0.0 - 1.0</i> | Permite um dimensionamento não uniforme do padrão. |
| <b>Escala</b> <i>0.0 - 1.0</i> | Defina a escala global (uniforme) do efeito. |
| <b>Multiplicador de Mapa de Escala</b> <i>0.0 - 1.0</i> | Defina a influência do Mapa de escala opcional. |
| <b>Escala aleatória</b> <i>-1.0 - 1.0</i> | Define a quantidade de variação aleatória na escala de padrão. |
| <b>Rotação</b> |  |
| <b>Rotação</b> <i>0.0 - 1.0</i> | Define a rotação global e uniforme para cada célula. |
| <b>Multiplicador de Mapas de rotação</b> <i>0.0 - 1.0</i> | Definir influência do Mapa de rotação opcional. |
| <b>Rotação aleatória</b> <i>0.0 - 1.0</i> | Define o valor de rotação aleatória para cada célula. |
| <b>Escala Automática de Rotação</b> <i>Falso/Verdadeiro</i> | Defina se um padrão deve ajustar sua escala para caber dentro de uma célula quando girado. |
| <b>Posição</b> |  |
| <b>Deslocamento de Posição</b> <i>0.0 - 1.0</i> | Defina o deslocamento global da posição para cada célula. |
| <b>Alinhamento de Deslocamento de Posição</b> <i>Textura, Padrão</i> | Defina para alinhar o deslocamento de 0 ponto à célula Padrão ou à textura. |
| <b>Deslocamento de Posição Aleatório</b> <i>0.0 - 1.0</i> | Defina a quantidade de deslocamento aleatório de Posição por célula. |
| <b>Cor (Somente para a versão em tons de cinza)</b> |  |
| <b>Intervalo de luminância</b> <i>0.0 - 1.0</i> | Define o contraste global na textura, onde 0 se torna cinza médio. |
| <b>Intervalo de luminância aleatório</b> <i>0.0 - 1.0</i> | Define a quantidade de aleatorização para o Intervalo de luminância. |
| <b>Deslocamento de luminância</b> <i>-1.0 - 1.0</i> | Define o deslocamento para a Luminância, trabalhando como um controle de brilho. |
| <b>Deslocamento de luminância aleatório</b> <i>0.0 - 1.0</i> | Define a quantidade de aleatorização para o Deslocamento de luminância. |
| <b>Multiplicador de Mapa de Deslocamento de Luminância</b> <i>0.0 - 1.0</i> | Define a influência do mapa opcional de Deslocamento de luminância. |
| <b>Cor do plano de fundo</b> <i>(Valor em tons de cinza)</i> | Define a cor do plano de fundo na qual as texturas são mescladas. |
| <b>Cor (Somente para a versão Colorida)</b> |  |
| <b>É Mapa normal</b> <i>Falso/Verdadeiro</i> | Defina para interpretar a Entrada de padrão como uma Mapa normal. Compensará e corrigirá a rotação de espaço Tangente Normal. |
| <b>Formato Normal</b> <i>DirectX, OpenGL</i> | Alternar entre Formatos de mapa normais diferentes (inverte o canal verde). Somente ativo quando Is Mapa normal é verdadeiro. |
| <b>Ajuste de HSL</b> <i>-1.0 - 1.0</i> | Ajustar o HSL globalmente. |
| <b>HSL Aleatório</b> <i>-1.0 - 1.0</i> | Definir aleatorização por HSL por célula. |
| <b>Ajuste de Alpha</b> <i>-1.0 - 1.0</i> | Definir ajuste de Alpha global, reduz o contraste de Alpha. |
| <b>Alpha aleatório</b> <i>-1.0 - 1.0</i> | Definir aleatoriedade de ajuste de Alpha por célula. |
| <b>Cor do plano de fundo</b> <i>(Valor da cor)</i> | Define a cor do plano de fundo na qual as texturas são mescladas. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-mapper.resources/floodfill-mapper-ex01.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="flood-fill-mapper.resources/floodfill-mapper-ex02.jpg" />
        </td>
    </tr>
</table>
