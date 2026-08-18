---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/waveform-1.html"
breadcrumb-title: ''
description: Use o nó Forma de onda 1 para gerar padrões de forma de onda para criar texturas orgânicas e variações de procedimentos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Waveform 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Forma de onda 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 2%

---


# Forma de onda 1

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Forma de onda 1 - Ícone](../../../../../../assets/waveform_01_v2.png "Forma de onda 1 - Ícone"){width="200px"}

<b>Entrada:</b> geradores de textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma organização horizontal de padrões selecionados pelo usuário empilhados em uma forma semelhante a uma forma de onda.

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
| <b>Amostras</b> Inteiro | A quantidade de padrões colocados ao longo do eixo X para desenhar a forma de onda, onde um valor mais baixo resulta em uma aparência mais passo a passo. |
| <b>Função</b> Inteiro | A função usada para desenhar a forma de onda.   Controla o tamanho vertical do padrão colocado em cada amostra:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Ruído de valor:</i> uma distribuição aleatória de valores</li> <li data-preserve-html="true"><i>Cosseno:</i> os valores seguem a progressão de uma função de cosseno</li> <li data-preserve-html="true"><i>Função personalizada:</i> use uma função de autoria do usuário para direcionar os valores</li> </ul> |
| <b>Função personalizada</b> Flutuante *Disponível quando &#39;Função&#39; está definido como &#39;Função personalizada&#39;* | Calcula o tamanho vertical do padrão colocado em cada amostra.   Variáveis disponíveis:<ul data-preserve-html="true"> <li data-preserve-html="true"><b>pos</b> (<i>float</i>) A posição do padrão no eixo X. Isso pode ser usado para selecionar padrões.</li> </ul> |
| <b>Aspereza</b> flutuante | Interpola entre uma forma de onda limpa e suave com uma mais áspera e distribuída uniformemente.    Isso pode ser considerado um sinal limpo vs. ruído branco. |
| <b>Escala</b> Inteiro | A extensão horizontal da forma de onda visível na imagem. |
| <b>Amplitude mínima</b>  Float | O valor mínimo (ou thickness) da forma de onda. |
| <b>Amplitude máxima</b>  Float | O valor máximo (ou thickness) da forma de onda. |
| <b>Ruído</b> flutuante | Aplica ruído à forma de onda que subtrai aleatoriamente de sua extensão vertical. |
| <b>Posição</b> Inteiro | A posição da forma de onda na imagem:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Centralizado:</i> a origem está no centro vertical da imagem</li> <li data-preserve-html="true"><i>Parte inferior:</i> a origem é a parte inferior da imagem</li> </ul> |
| <b>Padrão</b> Inteiro | O padrão colocado em cada amostra da forma de onda. |
| <b>Variação de padrão</b> Flutuante | Um ajuste adicional disponível para alguns padrões. |
| <b>Desordem</b> Flutuante | Desloca os valores da forma de onda.    Isso pode ser usado para animá-lo. |
| <b>Velocidade do distúrbio</b> flutuante | Ajusta a distância de deslocamento aplicada pelo parâmetro <b>Desordem</b>.    Isso pode ser usado para controlar a velocidade de deslocamento ao animar a forma de onda. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Forma de onda 1 - Exemplo 1](../../../../../../assets/waveform_01_v2_speed0.1_aniso0.gif "Forma de onda 1 - Exemplo 1"){zoomable="yes"}

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
