---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/dirt-gradient.html"
breadcrumb-title: ""
description: Use o nó Gradiente de Dirt para gerar padrões de dirt baseados em gradiente para criar efeitos de intemperismo direcional e acúmulo.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Dirt gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Degradê de dirt
user-guide-description: ""
user-guide-title: ""
source-git-commit: 5c22e4674afb51c0dcb1334853e889ea0f5bc748
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 1%
---

# Degradê de dirt

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Degradê de Dirt - Ícone](dirt-gradient.resources/dirt_gradient.png "Degradê de Dirt - Ícone"){width="200px"}

<b>Entrada:</b> geradores de Textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma variação dos ruídos granulados de <b>Dirt</b>, com um gradiente de queda direcional.

Veja também: [Dirt 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-1/dirt-1.md), [Dirt 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-2/dirt-2.md), [Dirt 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-3/dirt-3.md), [Dirt 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-4/dirt-4.md), [Dirt 5](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/dirt-5/dirt-5.md)

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
| <b>Desordem</b> <i>Precisão decimal</i> | Desloca os ingredientes do ruído.    Isso pode ser usado para animar o ruído. |
| <b>Velocidade do distúrbio</b> <i>Precisão decimal</i> | Ajusta a distância de deslocamento aplicada pelo parâmetro <b>Desordem</b>.    Isso pode ser usado para controlar a velocidade de deslocamento ao animar o ruído. |
| <b>anisotropia de distúrbio</b> <i>Precisão decimal</i> | Controla a extensão das direções do deslocamento aplicadas pelo parâmetro <b>Desordem</b>, em que um valor mais alto resulta em uma direção mais estreita e definida.    A direção é controlada pelo parâmetro <b>ângulo de anisotropia de Desordem</b>. |
| <b>ângulo de anisotropia de desordem</b> <i>Precisão decimal</i> | Controla a direção do deslocamento aplicado pelo parâmetro <b>Desordem</b> quando o parâmetro <b>anisotropia de Desordem</b> não é zero. |
| <b>Expansão não quadrada</b> <i>Booleano</i> | Em imagens não quadradas, mantém o ladrilho gerado quadrado e expande a geração de ruído até os limites da imagem. |

## Exemplos

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="dirt-gradient.resources/dirt_gradient_1.png" class="modal-image" alt="Degradê de dirt - Exemplo 1" />
        </td>
        <td style="border: 0;">
            <img src="dirt-gradient.resources/noise_dirt_gradient_v2_speed0.6_aniso0.gif" class="modal-image" alt="Degradê de dirt — exemplo 2" />
        </td>
        <td style="border: 0;">
            <img src="dirt-gradient.resources/noise_dirt_gradient_v2_speed0.6_aniso1.gif" class="modal-image" alt="Degradê de dirt - Exemplo 3" />
        </td>
    </tr>
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="dirt-gradient.resources/noise_dirt_gradient_v2_speed0.3_aniso0.6.gif" class="modal-image" alt="Degradê de dirt - Exemplo 4" />
        </td>
        <td style="border: 0;"></td>
        <td style="border: 0;"></td>
    </tr>
</table>
