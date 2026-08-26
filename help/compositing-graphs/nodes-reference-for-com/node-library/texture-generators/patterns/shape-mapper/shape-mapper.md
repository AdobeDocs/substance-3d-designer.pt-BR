---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-mapper.html"
breadcrumb-title: ''
description: Use o nó Mapeador de formas para mapear formas em texturas com transformações e posicionamento personalizáveis.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mapeador de formas
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 3%

---


# Mapeador de formas

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Mapeador de formas - Ícone](../../../../../../assets/shape_mapper.png "Mapeador de formas - Ícone"){width="200px"}

<b>Entrada:</b> geradores de textura > Padrões

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Projeta uma imagem de entrada em um círculo ou polígono.

A projeção deforma a imagem para seguir o contorno da forma e faz com que ela se ajuste exatamente a uma quantidade especificada de vezes sem intervalos.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Entradas

</td>
<td style="border: 0;" valign="top">

### Saídas

</td>
<td style="border: 0;" valign="top">

### Parâmetros

</td>
<td style="border: 0;" valign="top">

### Exemplos

</td>
</tr>
</table>

## Entradas

|  |  |
| --- | --- |
| <b>Entrada</b> *Tons de cinza* | O padrão que deve ser colocado ao longo da forma. |

## Saídas

|  |  |
| --- | --- |
| <b>Saída</b> *Tons de cinza* | O resultado da projeção do padrão ao longo da forma, como um bitmap em tons de cinza. |

## Parâmetros

|  |  |
| --- | --- |
| <b>Forma</b> Inteiro | Define o tipo de forma ao longo do qual os padrões devem ser colocados:<ul data-preserve-html="true"> <li data-preserve-html="true">Círculo</li> <li data-preserve-html="true">Polígono</li> </ul> |
| <b>Valor padrão</b> Inteiro | A quantidade de padrões colocados ao longo da forma selecionada. |
| <b>Vincular segmentos com valor de padrão</b> Booleano *Disponível quando &#39;Forma&#39; estiver definido como &#39;Polígono&#39;* | Use o <b>Valor do padrão</b> como o número de <b>Segmentos</b>.   Isso evita que os padrões envolvam cantos, garantindo um aspecto reto e consistente. |
| <b>Segmentos</b> Inteiro *Disponível quando &#39;Forma&#39; está definido como &#39;Polígono&#39; e &#39;Vincular segmentos com valor de padrão&#39; está definido como &#39;Falso&#39;* | A quantidade de segmentos para o polígono ao longo do qual os padrões são colocados.   Os segmentos são *dimensionados uniformemente*, e todos os vértices estão *equidistantes do centro*, de modo que o aumento da quantidade de segmentos faz com que o polígono convirja em direção a um círculo. |
| <b>Raio</b> flutuante | Um multiplicador para o raio da forma, onde 1,0 é metade do comprimento do lado mais curto da imagem. |
| Flutuação de <b>Largura</b> | Um multiplicador para a largura dos padrões ao longo da forma, onde 1,0 é metade do comprimento do lado mais curto da imagem. |
| <b>Rotação</b> Flutuante | O valor de rotação aplicado à forma, em número de voltas no sentido horário a partir da direita horizontal. |
| <b>Virar um em dois</b> booleano | Virar uma forma a cada outra verticalmente. |
| <b>Modo de filtragem</b> Inteiro | O método de filtragem aplicado aos padrões colocados ao longo da forma:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Mais próximo:</i> aplica o valor do pixel projetado mais próximo como ele está, resultando em uma aparência mais nítida, mas com alias.</li> <li data-preserve-html="true"><i>Bilinear:</i> aplica um filtro bilinear para interpolar o pixel projetado com seus vizinhos, para obter uma aparência mais suave e desfocada.</li> </ul> |
| <b>Expansão não quadrada</b> Booleana | Em imagens não quadradas, mantém o quadrado da forma gerada e expande a geração da imagem até os limites da imagem. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
