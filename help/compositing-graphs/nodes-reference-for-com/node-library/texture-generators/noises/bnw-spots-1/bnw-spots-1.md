---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/bnw-spots-1.html"
breadcrumb-title: ""
description: Use o nó Manchas 1 para gerar padrões de manchas pretas e brancas para criar variações de textura e máscaras de detalhes.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > BnW spots 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Manchas Pb 1
user-guide-description: ""
user-guide-title: ""
source-git-commit: 5c22e4674afb51c0dcb1334853e889ea0f5bc748
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 1%
---

# Manchas Pb 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Pontos PB 1 - Ícone](bnw-spots-1.resources/bnw_spots_1.png "Pontos PB 1 - Ícone"){width="200px"}

<b>Entrada:</b> geradores de Textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma variação dos ruídos grosseiros de <b>manchas pretas e brancas (BnW)</b>.

Veja também: [Manchas P2B](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/bnw-spots-2/bnw-spots-2.md), [Manchas P2B3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/bnw-spots-3/bnw-spots-3.md)

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
| <b>Desordem</b> <i>Precisão decimal</i> | Desloca os ingredientes do ruído.    Isso pode ser usado para animar o ruído. |
| <b>Velocidade do distúrbio</b> <i>Precisão decimal</i> | Ajusta a distância de deslocamento aplicada pelo parâmetro <b>Desordem</b>.    Isso pode ser usado para controlar a velocidade de deslocamento ao animar o ruído. |
| <b>anisotropia de distúrbio</b> <i>Precisão decimal</i> | Controla a extensão das direções do deslocamento aplicadas pelo parâmetro <b>Desordem</b>, em que um valor mais alto resulta em uma direção mais estreita e definida.    A direção é controlada pelo parâmetro <b>ângulo de anisotropia de Desordem</b>. |
| <b>ângulo de anisotropia de desordem</b> <i>Precisão decimal</i> | Controla a direção do deslocamento aplicado pelo parâmetro <b>Desordem</b> quando o parâmetro <b>anisotropia de Desordem</b> não é zero. |
| <b>Aspereza</b> <i>Precisão decimal</i> | O equilíbrio das oitavas de ruído, onde um valor mais alto tornará as oitavas de frequência mais altas mais visíveis. |
| <b>Deslocamento do bloco</b> <i>Precisão decimal 2</i> | Controla a posição da parte de plano infinito usada para renderizar o ruído. |
| <b>Expansão não quadrada</b> <i>Booleano</i> | Em imagens não quadradas, mantém o ladrilho gerado quadrado e expande a geração de ruído até os limites da imagem. |

## Exemplos

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="bnw-spots-1.resources/bnw_spots_1_1.png" class="modal-image" alt="Pontos P/B 1 - Exemplo 1" />
        </td>
        <td style="border: 0;">
            <img src="bnw-spots-1.resources/noise_bnw_spots_1_v2_speed0.6_aniso0.gif" class="modal-image" alt="Pontos P/B 1 - Exemplo 2" />
        </td>
        <td style="border: 0;">
            <img src="bnw-spots-1.resources/noise_bnw_spots_1_v2_speed0.6_aniso1.gif" class="modal-image" alt="Pontos P/B 1 - Exemplo 3" />
        </td>
    </tr>
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="bnw-spots-1.resources/noise_bnw_spots_1_v2_speed0.3_aniso0.6.gif" class="modal-image" alt="Pontos de largura de banda 1 - Exemplo 4" />
        </td>
        <td style="border: 0;"></td>
        <td style="border: 0;"></td>
    </tr>
</table>
