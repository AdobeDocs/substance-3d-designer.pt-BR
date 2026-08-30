---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/arc-pavement.html"
breadcrumb-title: ''
description: Use o nó Pavimento de arco para gerar padrões de pavimento em forma de arco para criar texturas curvas de estrada e caminho.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Arc Pavement
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Calçada Arc
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 11%

---


# Calçada Arc

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](arc-pavement.resources/arcpavement-ex.png)

<b>Em:</b> Geradores De Textura > Padrões

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera um padrão de pavimento de arco parisiense. Este efeito não pode ser obtido com o [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)ou o [Bloco Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) padrão, portanto, este nó dedicado.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Escala</b> <i>1 - 8</i> | Define a escala/divisão em blocos gráficos globais. |
| <b>Valor do Padrão</b> <i>1 - 32</i> | Define a quantidade de tijolos usada em cada arco. |
| <b>Valor Aleatório do Padrão</b> <i>0.0 - 1.0</i> | Dispõe aleatoriamente a quantidade de tijolos em cada arco. Tem o efeito adicional de dar aos tijolos escalas diferentes. |
| <b>Valor Mínimo de Padrão</b> <i>1 - 10</i> | Controla a quantidade mínima de bricks ao randomizar arcos. |
| <b>Valor dos arcos</b> <i>0 - 20</i> | Define a quantidade de arcos empilhados verticalmente. Altera o height de tijolos. |
| <b>Padrão</b> <i>Imagem De Entrada, Quadrado, Disco, Parabolóide, Sino, Gaussiano, Espinho, Pirâmide, Tijolo, Gradações, Ondas, Meio sino, Sino Ondulado, Crescente, Cápsula, Cone</i> | Seleciona a forma de padrão a ser usada. |
| <b>Filtragem de Imagem de Entrada</b> <i>Bilinear + Mipmaps, Bilinear, Mais Próximo</i> |  |
| <b>Escala de padrão</b> <i>0.0 - 1.0</i> | Define a escala de cada ladrilho. |
| <b>Largura do Padrão</b> <i>0.0 - 1.0</i> | Define a largura de cada ladrilho. |
| <b>Height de padrões</b> <i>0.0 - 1.0</i> | Define o height para cada ladrilho. |
| <b>Largura de padrão aleatória</b> <i>0.0 - 1.0</i> | Dispõe aleatoriamente a largura do ladrilho. |
| <b>Height de padrão aleatório</b> <i>0.0 - 1.0</i> | Height de ladrilho aleatório. |
| <b>Aleatório de Largura de Padrão Global</b> <i>0.0 - 1.0</i> | Dispõe aleatoriamente a largura do ladrilho, sem criar espaços maiores entre eles. |
| <b>Diminuição do Height de padrões</b> <i>0.0 - 1.0</i> | Controla o esmagamento do height lado a lado nas extremidades de cada arco. |
| <b>Cores aleatórias</b> <i>0.0 - 1.0</i> | Dispõe aleatoriamente as cores dos ladrilhos. |
| <b>Expansão não quadrada</b> <i>Falso/Verdadeiro</i> | Permite a compensação de esmagamento e alongamento com proporções não quadradas. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="arc-pavement.resources/arcpavement-ex.png" />
        </td>
    </tr>
</table>
