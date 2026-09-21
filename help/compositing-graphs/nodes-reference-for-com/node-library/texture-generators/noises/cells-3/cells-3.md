---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/cells-3.html"
breadcrumb-title: ""
description: Use o nó do Células 3 para gerar padrões celulares intermediários a fim de criar efeitos de textura orgânicos e biológicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Cells 3
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: CÉLULAS 3
user-guide-description: ""
user-guide-title: ""
source-git-commit: 5c22e4674afb51c0dcb1334853e889ea0f5bc748
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%
---

# CÉLULAS 3

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Células 3 - Ícone](cells-3.resources/cells_3.png "Células 3 - Ícone"){width="200px"}

<b>Entrada:</b> geradores de Textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma variação das <b>Células</b> ruídos de paredes.

A interseção de discos produz células com paredes finas de suavidade desigual.

Veja também: [Células 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md), [Células 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-2/cells-2.md), [Células 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-4/cells-4.md)

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
| <b>Dureza</b> <i>Precisão decimal</i> | A definição das paredes celulares, onde um valor mais alto resulta em paredes mais definidas e nítidas. |
| <b>Inverter</b> <i>Booleano</i> | Inverte os valores em tons de cinza da saída da imagem. |
| <b>Desordem</b> <i>Precisão decimal</i> | Desloca os ingredientes do ruído.    Isso pode ser usado para animar o ruído. |
| <b>Velocidade do distúrbio</b> <i>Flutuante</i> | Ajusta a distância de deslocamento aplicada pelo parâmetro <b>Desordem</b>.    Isso pode ser usado para controlar a velocidade de deslocamento ao animar o ruído. |
| <b>anisotropia de distúrbio</b> <i>Flutuante</i> | Controla a extensão das direções do deslocamento aplicadas pelo parâmetro <b>Desordem</b>, em que um valor mais alto resulta em uma direção mais estreita e definida.    A direção é controlada pelo parâmetro <b>Ângulo de anisotropia de desordem</b>. |
| <b>ângulo de anisotropia de desordem</b> <i>Flutuante</i> | Controla a direção do deslocamento aplicado pelo parâmetro <b>Desordem</b> quando o parâmetro &#39;anisotropia de Desordem&#39; não é zero. |
| <b>Tamanho do padrão</b> <i>Flutuante2</i> | Um multiplicador para o tamanho de um disco disperso em sua célula., onde 1,0 é o intervalo completo da célula. |
| <b>Escala de padrão</b> <i>Flutuante</i> | Um multiplicador para o <b>Tamanho do padrão</b>, onde 1,0 é o tamanho máximo. |
| <b>Ângulo</b> <i>Flutuante</i> | Ângulo usado para definir a direção dos discos, em número de voltas e começando na horizontal direita. |
| <b>Ângulo aleatório</b> <i>Flutuante</i> | O valor máximo de variação aleatória aplicado ao valor <b>Ângulo</b>, em número de voltas. |
| <b>Deslocamento do bloco</b> <i>Flutuante2</i> | Controla a posição da parte de plano infinito usada para renderizar o ruído. |
| <b>Expansão não quadrada</b> <i>Booleano</i> | Em imagens não quadradas, mantém o ladrilho gerado quadrado e expande a geração de ruído até os limites da imagem. |

## Exemplos

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="cells-3.resources/cells_3_1.png" class="modal-image" alt="Células 3 - Exemplo 1" />
        </td>
        <td style="border: 0;">
            <img src="cells-3.resources/noise_cells_3_v2_speed0.6_aniso0.gif" class="modal-image" alt="Células 3 - Exemplo 2" />
        </td>
        <td style="border: 0;">
            <img src="cells-3.resources/noise_cells_3_v2_speed0.6_aniso1.gif" class="modal-image" alt="Células 3 - Exemplo 3" />
        </td>
    </tr>
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="cells-3.resources/noise_cells_3_v2_speed0.3_aniso0.6.gif" class="modal-image" alt="Células 3 - Exemplo 4" />
        </td>
        <td style="border: 0;"></td>
        <td style="border: 0;"></td>
    </tr>
</table>
