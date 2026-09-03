---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/directional-scratches.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---


# Arranhões direcionais

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Rabiscos direcionais - Ícone](directional-scratches.resources/directional-scratches-01.png "Rabiscos direcionais - Ícone"){width="200px"}

<b>Entrada:</b> geradores de textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma dispersão aleatória de padrões de rabisco com ângulo e tamanho ajustáveis.

</td>
</tr>
</table>

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Saída</b> <i>Tons de cinza</i> | O ruído gerado como bitmap em tons de cinza. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Escala</b> <i>Inteiro</i> | A subdivisão da grade usada para gerar os blocos de ruído.    Um valor mais alto resulta no desenho de mais ladrilhos e em um ruído mais denso. |
| <b>Desordem</b> <i>Flutuante</i> | Desloca os ingredientes do ruído.    Isso pode ser usado para animar o ruído. |
| <b>Velocidade do distúrbio</b> <i>Flutuante</i> | Ajusta a distância de deslocamento aplicada pelo parâmetro <b>Desordem</b>.    Isso pode ser usado para controlar a velocidade de deslocamento ao animar o ruído. |
| <b>anisotropia de distúrbio</b> <i>Flutuante</i> | Controla a extensão das direções do deslocamento aplicadas pelo parâmetro <b>Desordem</b>, em que um valor mais alto resulta em uma direção mais estreita e definida.    A direção é controlada pelo parâmetro <b>Ângulo de anisotropia de desordem</b>. |
| <b>ângulo de anisotropia de desordem</b> <i>Flutuante</i> | Controla a direção do deslocamento aplicado pelo parâmetro <b>Desordem</b> quando o parâmetro <b>anisotropia de Desordem</b> não é zero. |
| <b>Ângulo</b> <i>Flutuante</i> | O ângulo usado para definir a direção dos arranhões, em número de voltas e começando da direita horizontal. |
| <b>Ângulo aleatório</b> <i>Flutuante</i> | O valor máximo de variação aleatória aplicado ao valor <b>Ângulo</b>, em número de voltas. |
| <b>Valor padrão</b> <i>Flutuante</i> | Um multiplicador para a quantidade de padrões de rascunho que está sendo espalhada. |
| <b>Tamanho do padrão</b> <i>Flutuante2</i> | O tamanho da caixa delimitadora do padrão de rascunho.    O valor Y controla o comprimento máximo dos riscos. |
| <b>Tamanho de padrão aleatório</b> <i>Flutuante2</i> | Um multiplicador para a quantidade aleatória de downscaling aplicada aos riscos.    O valor Y aplica isso ao comprimento dos riscos. |
| <b>Deslocamento do bloco</b> <i>Flutuante2</i> | Controla a posição da parte de plano infinito usada para renderizar o ruído. |
| <b>Expansão não quadrada</b> <i>Booleano</i> | Em imagens não quadradas, mantém o ladrilho gerado quadrado e expande a geração de ruído até os limites da imagem. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Arranhões Direcionais - Exemplo 1](directional-scratches.resources/directional-scratches-02.png "Arranhões Direcionais - Exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Arranhões Direcionais - Exemplo 2](directional-scratches.resources/directional-scratches-03.gif "Arranhões Direcionais - Exemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Arranhões Direcionais - Exemplo 3](directional-scratches.resources/directional-scratches-04.gif "Arranhões Direcionais - Exemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Arranhões Direcionais - Exemplo 4](directional-scratches.resources/directional-scratches-05.gif "Arranhões Direcionais - Exemplo 4"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Arranhões Direcionais - Exemplo 5](directional-scratches.resources/directional-scratches-06.gif "Arranhões Direcionais - Exemplo 5"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
