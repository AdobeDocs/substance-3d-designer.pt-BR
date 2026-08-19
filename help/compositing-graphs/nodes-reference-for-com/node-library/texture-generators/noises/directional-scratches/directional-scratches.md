---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-scratches.html"
breadcrumb-title: ''
description: Use o nó Scratches direcional para criar padrões de arranhões direcionais para adicionar efeitos de desgaste e danos aos materiais.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Directional scratches
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Arranhões direcionais
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 1%

---


# Arranhões direcionais

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Rabiscos direcionais - Ícone](../../../../../../assets/directional_scratches.png "Rabiscos direcionais - Ícone"){width="200px"}

<b>Entrada:</b> geradores de textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma dispersão aleatória de padrões de rabisco com ângulo e tamanho ajustáveis.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
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

## Saídas

|  |  |
| --- | --- |
| <b>Saída</b> *Tons de cinza* | O ruído gerado como bitmap em tons de cinza. |

## Parâmetros

|  |  |
| --- | --- |
| <b>Escala</b> Inteiro | A subdivisão da grade usada para gerar os blocos de ruído.    Um valor mais alto resulta no desenho de mais ladrilhos e em um ruído mais denso. |
| <b>Desordem</b> Flutuante | Desloca os ingredientes do ruído.    Isso pode ser usado para animar o ruído. |
| <b>Velocidade do distúrbio</b> flutuante | Ajusta a distância de deslocamento aplicada pelo parâmetro <b>Desordem</b>.    Isso pode ser usado para controlar a velocidade de deslocamento ao animar o ruído. |
| <b>anisotropia de desordem</b> flutuante | Controla a extensão das direções do deslocamento aplicadas pelo parâmetro <b>Desordem</b>, em que um valor mais alto resulta em uma direção mais estreita e definida.    A direção é controlada pelo parâmetro <b>Ângulo de anisotropia de desordem</b>. |
| <b>Ângulo de anisotropia do distúrbio</b> flutuante | Controla a direção do deslocamento aplicado pelo parâmetro <b>Desordem</b> quando o parâmetro <b>anisotropia de Desordem</b> não é zero. |
| <b>Ângulo</b> Flutuante | O ângulo usado para definir a direção dos arranhões, em número de voltas e começando da direita horizontal. |
| <b>Ângulo aleatório</b> flutuante | O valor máximo de variação aleatória aplicado ao valor <b>Ângulo</b>, em número de voltas. |
| <b>Valor padrão</b> flutuante | Um multiplicador para a quantidade de padrões de rascunho que está sendo espalhada. |
| <b>Tamanho do padrão</b> Float2 | O tamanho da caixa delimitadora do padrão de rascunho.    O valor Y controla o comprimento máximo dos riscos. |
| <b>Tamanho de padrão aleatório</b> Float2 | Um multiplicador para a quantidade aleatória de downscaling aplicada aos riscos.    O valor Y aplica isso ao comprimento dos riscos. |
| <b>Deslocamento do bloco</b> flutuante2 | Controla a posição da parte de plano infinito usada para renderizar o ruído. |
| <b>Expansão não quadrada</b> Booleana | Em imagens não quadradas, mantém o ladrilho gerado quadrado e expande a geração de ruído até os limites da imagem. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Arranhões Direcionais - Exemplo 1](../../../../../../assets/directional_scratches_1.png "Arranhões Direcionais - Exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Arranhões Direcionais - Exemplo 2](../../../../../../assets/noise-directional-scratches-speed0.3-aniso0.gif "Arranhões Direcionais - Exemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Arranhões Direcionais - Exemplo 3](../../../../../../assets/noise-directional-scratches-speed0.3-aniso0.6.gif "Arranhões Direcionais - Exemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Arranhões Direcionais - Exemplo 4](../../../../../../assets/noise-directional-scrat-1.gif "Arranhões Direcionais - Exemplo 4"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Arranhões Direcionais - Exemplo 5](../../../../../../assets/noise-directional-scrat-2.gif "Arranhões Direcionais - Exemplo 5"){zoomable="yes"}

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
