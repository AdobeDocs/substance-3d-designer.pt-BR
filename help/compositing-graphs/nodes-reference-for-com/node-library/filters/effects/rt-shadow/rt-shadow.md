---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-shadow.html"
breadcrumb-title: ''
description: Use o nó Sombras RT para calcular informações de sombra em tempo real a partir da geometria para criar efeitos de iluminação dinâmicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Shadows
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sombras RT
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# Sombras RT

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone do nó Sombras RT](rt-shadow.resources/rt-shadow-01.png "Ícone do nó Sombras RT")

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera sombras traçadas de raio a partir de uma entrada de mapa de height.

Este nó não deve ser usado em combinação com o mecanismo da CPU (SSE) devido ao tempo de computação.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Amostras</b> <i>Inteiro</i> | O número de raios usados para calcular as sombras.<br>Um valor mais alto fornece um resultado mais suave e preciso, em detrimento do desempenho. |
| <b>Modo</b> <i>Inteiro</i> | O método de desenhar as sombras na superfície. |
| <b>Escala de Height</b> <i>Flutuante</i> | Um multiplicador para a intensidade do mapa de height de entrada. |
| <b>Posição da luz</b> <i>Flutuante2</i> | A posição da fonte de luz em uma esfera que envolve a superfície:<br><br>- <b>X</b>: posição horizontal, em número de voltas;<br>- <b>Y</b>: posição vertical, onde 0,5 é o zênite e 0/1 é o horizonte. |
| <b>Intensidade da luz</b> <i>Flutuante</i> | A intensidade da fonte de luz. |
| <b>Tamanho Claro</b> <i>Flutuante2</i> | (Disponível quando o <b>Modo</b> está definido como <i>Sombreado</i>) O tamanho da fonte de luz como um retângulo. |
| <b>Escala Clara (Sombras Suaves)</b> <i>Flutuante</i> | Um multiplicador da contribuição do <b>Tamanho da Luz</b> para a direção dos raios.<br>Um valor mais alto resulta em sombras mais suaves. |
| <b>Manter a luz acima do horizonte</b> <i>Booleano</i> | Se a <b>Posição da Luz</b> estiver definida de forma a colocar a luz abaixo do horizonte, este parâmetro impedirá que a luz ultrapasse esse limite, o que significa que os valores de Y estão fixados no intervalo [0;1]. |
| <b>Opacidade da sombra</b> <i>Flutuante</i> | Um multiplicador da opacidade de sombras desenhadas na superfície. |
| <b>Atenuação de Sombra</b> <i>Flutuante</i> | Um multiplicador para a atenuação das sombras quanto mais distantes elas estiverem de seu movimento de caster.<br>Um valor de 0 resulta em sombras uniformes (as sombras suaves ainda são aplicadas). |
| <b>Comprimento Máximo de Sombras</b> <i>Flutuante</i> | A distância máxima que uma sombra pode ser desenhada de seu estrato.<br>Um valor de 0 resulta em sombras não visíveis. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/rt-shadow-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/rt-shadow-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/rt-shadow-04.jpg" />
        </td>
    </tr>
</table>
