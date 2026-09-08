---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/moisture-noise.html"
breadcrumb-title: ''
description: Use o nó Ruído de umidade para gerar padrões de umidade e condensação para criar efeitos de superfície molhados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Moisture noise 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruído de humidade 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8774511f26429071b91a2eeeb8728ac36dc31ed5
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 1%

---


# Ruído de humidade 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ruído de umidade 1 - Ícone](../../../../../../assets/moisture_noise_1.png "Ruído de umidade 1 - Ícone"){width="200px"}

<b>Entrada:</b> geradores de textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma variação dos ruídos ricos e esponjosos do <b>Umidade</b>.

Discos de dureza e tamanho variados e dispersos adicionam ou subtraem da cor abaixo, começando do cinza base.

Veja também: [Ruído de umidade 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/moisture-noise-2/moisture-noise-2.md)

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
| <b>Tamanho do padrão</b> <i>Flutuante2</i> | Um multiplicador para o tamanho de um padrão de dispersão, onde 1,0 é seu tamanho de dispersão original. |
| <b>Ângulo de padrão</b> <i>Flutuante</i> | O ângulo usado para definir a direção do padrão disperso, em número de voltas e começando da direita horizontal. |
| <b>Ângulo de padrão aleatório</b> <i>Flutuante</i> | O valor máximo de variação aleatória aplicado ao valor de <b>Ângulo de padrão</b>, em número de voltas. |
| <b>Opacidade global</b> <i>Flutuante</i> | A opacidade de todos os ingredientes do ruído, em que 0,0 resulta num fundo cinzento plano e 1,0 resulta da adição ou subtração totais aplicadas pelos ingredientes. |
| <b>Deslocamento do bloco</b> <i>Flutuante2</i> | Controla a posição da parte de plano infinito usada para renderizar o ruído. |
| <b>Expansão não quadrada</b> <i>Booleano</i> | Em imagens não quadradas, mantém o ladrilho gerado quadrado e expande a geração de ruído até os limites da imagem. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ruído de umidade 1 - Exemplo 1](../../../../../../assets/moisture_noise_1_1.png "Ruído de umidade 1 - Exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ruído de umidade 1 - Exemplo 2](../../../../../../assets/noise_moisture_noise_1_v2_speed0.6_aniso0.gif "Ruído de umidade 1 - Exemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ruído de umidade 1 - Exemplo 3](../../../../../../assets/noise_moisture_noise_1_v2_speed0.6_aniso1.gif "Ruído de umidade 1 - Exemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Ruído de umidade 1 - Exemplo 4](../../../../../../assets/noise_moisture_noise_1_v2_speed0.3_aniso0.6.gif "Ruído de umidade 1 - Exemplo 4"){zoomable="yes"}

</td>
</tr>
</table>
