---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape.html"
breadcrumb-title: ''
description: Use o nó Forma para gerar formas geométricas básicas para criar padrões e texturas no Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 6%

---


# Forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/shape-2.png){width="128px"}

<b>Em:</b> Geradores De Textura > Padrões

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma variedade de formas processuais, com opções para modificar as formas básicas. As formas são sempre perfeitamente interpoladas e de alta precisão.

Apesar de sua simplicidade, este é um nó muito útil: é o bloco de construção da mais processual geração Heightmap! Combinando formas básicas com nós de transformo, é possível criar uma forma de Heightmap totalmente processual que seja muito mais precisa do que qualquer bitmap.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Divisão em blocos gráficos</b> <i>1 - 16</i> | Define a quantidade de vezes que o resultado deve ser colocado lado a lado. |
| <b>Padrão</b> <i>Quadrado, Disco, Parabolóide, Sino, Gaussiano, Espinho, Pirâmide, Tijolo, Gradação, Ondas, Meio sino, Sino Ondulado, Crescente, Cápsula, Cone, Hemisfério</i> | Seleciona a forma de padrão a ser usada. |
| <b>Específico de Padrão</b> <i>0.0 - 1.0</i> | Permite que você altere a forma do padrão selecionado. O efeito depende do padrão selecionado. |
| <b>Escala</b> <i>0.0 - 1.0</i> | Dimensiona toda a forma. |
| <b>Tamanho</b> <i>0.0 - 1.0</i> | Permite um dimensionamento não uniforme nos eixos X ou Y. |
| <b>Ângulo</b> <i>0.0 - 1.0</i> | Gira toda a forma. |
| <b>Rotação 45°</b> <i>Falso/Verdadeiro</i> | Gira em 45 graus predefinidos. |
| <b>Expansão não quadrada</b> <i>Falso/Verdadeiro</i> | Permite a compensação de esmagamento e alongamento com proporções não quadradas. |
| <b>Divisão em blocos gráficos não quadrados</b> <i>Falso/Verdadeiro</i> | Quando o Expansão não quadrada estiver ativado, ele irá cobrir a forma sem esmagar. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/shape-ex.gif" />
        </td>
    </tr>
</table>
