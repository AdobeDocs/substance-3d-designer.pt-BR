---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/anisotropic-noise.html"
breadcrumb-title: ''
description: Use o nó Ruído anisotrópico para gerar padrões de ruído direcional para criar efeitos de textura anisotrópica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Anisotropic noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruído anisotrópico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 3c2ada78db14be2b9c3380eff9b307aec11d40dc
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 1%

---


# Ruído anisotrópico

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ruído anisotrópico - Ícone](../../../../../../assets/anisotropic_noise_v2.png "Ruído anisotrópico - Ícone"){width="200px"}

<b>Entrada:</b> geradores de textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma pilha horizontal ou vertical de tiras coloridas aleatoriamente desvanecendo-se uma na outra.

A quantidade de faixas é ajustável, assim como o smoothness de suas transições.

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
| <b>Valor X</b> Inteiro | A quantidade de faixas no eixo X. |
| <b>Valor Y</b> Inteiro | A quantidade de faixas no eixo Y. |
| Valor de <b>Y por resolução</b> booleano | Se verdadeiro, o número de faixas no eixo Y será igual ao tamanho da imagem nesse eixo. |
| <b>Girar</b> Booleano | Gira o ruído 90 graus. |
| <b>Smoothness</b> flutuante | A intensidade de desvanecimento entre as faixas, em que 0 é o mesmo que não e 1 o último em todo o seu comprimento. |
| <b>Interpolação de Smoothness</b> flutuante | A ponderação dos dois métodos de interpolação aplicados para atenuar as faixas, onde 0 é linear e 1 é gaussiano. |
| <b>Desordem</b> Flutuante | Desloca os ingredientes do ruído.   Isso pode ser usado para animar o ruído. |
| <b>Velocidade do distúrbio</b> flutuante | Ajusta a distância de deslocamento aplicada pelo parâmetro <b>Desordem</b>.   Isso pode ser usado para controlar a velocidade de deslocamento ao animar o ruído. |
| <b>Expansão não quadrada</b> Booleana | Em imagens não quadradas, mantém o ladrilho gerado quadrado e expande a geração de ruído até os limites da imagem. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ruído anisotrópico - Exemplo 1](../../../../../../assets/anisotropic_noise_v2_1.png "Ruído anisotrópico - Exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ruído anisotrópico - Exemplo 2](../../../../../../assets/noise_anisotropic_noise_v2_speed0.3_aniso0.6.gif "Ruído anisotrópico - Exemplo 2"){zoomable="yes"}

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
