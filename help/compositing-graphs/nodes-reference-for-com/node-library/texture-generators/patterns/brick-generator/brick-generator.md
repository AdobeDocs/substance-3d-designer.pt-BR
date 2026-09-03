---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/brick-generator.html"
breadcrumb-title: ''
description: Use o nó Gerador de tijolos para criar padrões processuais de tijolos com propriedades personalizáveis de tamanho, deslocamento e argamassa.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Brick Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gerador de tijolos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 8%

---


# Gerador de tijolos

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](brick-generator.resources/brick-generator-01.png){width="128px"}

<b>Em:</b> Geradores De Textura > Padrões

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gerador de padrão de tijolo avançado. Tem muitas opções para gerar especificamente padrões de tijolos feitos pelo homem

Para obter mais opções, consulte [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Tijolos</b> <i>1 - 64</i> | Define a quantidade de tijolos nos eixos X e Y. |
| <b>Chanfro</b> <i>0.0 - 1.0</i> | Altera o perfil de chanfro dos tijolos, permite alterar em duas direções, bem como definir o perfil de declínio e o arredondamento de canto. |
| <b>Manter Proporção</b> <i>Falso/Verdadeiro</i> | Torna o perfil de chanfro vinculado ao tamanho do tijolo ou não. |
| <b>Lacuna</b> <i>0.0 - 1.0</i> | Espaço para deixar entre tijolos. Lembre-se de que o chanfro também apresenta uma lacuna, portanto, definir chanfros também significa compensar com esse parâmetro. |
| <b>Tamanho Médio</b> <i>0.0 - 1.0</i> | Deslocamento de padrão de tijolo, altera o tamanho de todas as outras colunas ou linhas. |
| <b>Height</b> <i>-1.0 - 1.0</i> | Modifica perfis de height. Permite a introdução da variação de luminância e todos os tipos de aleatorização. |
| <b>Inclinação</b> <i>-1.0 - 1.0</i> | Introduz uma inclinação por tijolo, como se certos tijolos estivessem deitados em ângulo. |
| <b>Deslocamento</b> <i>0.0 - 1.0</i> | Desloca os tijolos em uma base de linha, afeta o espaçamento por linha. |
| <b>Expansão não quadrada</b> <i>Falso/Verdadeiro</i> | Permite a compensação de esmagamento e alongamento com proporções não quadradas. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="brick-generator.resources/brick-generator-02.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="brick-generator.resources/brick-generator-03.gif" />
        </td>
    </tr>
</table>
