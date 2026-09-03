---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/fractal-sum-base.html"
breadcrumb-title: ''
description: Use o nó Base de Soma fractal para gerar padrões de ruído fractal de base para criar texturas orgânicas complexas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Fractal sum base
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Soma fractal base
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---


# Soma fractal base

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Base de Soma fractal - Ícone](fractal-sum-base.resources/fractal-sum-base-01.png "Base de Soma fractal - Ícone"){width="200px"}

<b>Entrada:</b> geradores de textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Um ruído fractal personalizável com um intervalo ajustável e equilíbrio de oitavas.

A família de ruídos <b>Soma fractal</b> é baseada neste nó.

Veja também: [Soma fractal 1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-1/fractal-sum-1.md), [Soma fractal 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-2/fractal-sum-2.md), [Soma fractal 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-3/fractal-sum-3.md), [Soma fractal 4](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-4/fractal-sum-4.md)

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
| <b>Aspereza</b> <i>Flutuante</i> | O equilíbrio das oitavas de ruído.    Um valor mais alto tornará as oitavas de frequência mais visíveis. |
| <b>Mín. nível</b> <i>Inteiro</i> | A oitava mínima usada no ruído.    Um valor mais alto resulta em uma frequência de ruído mais alta. |
| <b>Máx. nível</b> <i>Inteiro</i> | A oitava máxima usada no ruído.    Um valor mais alto resulta em uma frequência de ruído mais alta. |
| <b>Desordem</b> <i>Flutuante</i> | Desloca os ingredientes do ruído.    Isso pode ser usado para animar o ruído. |
| <b>Velocidade do distúrbio</b> <i>Flutuante</i> | Ajusta a distância de deslocamento aplicada pelo parâmetro <b>Desordem</b>.    Isso pode ser usado para controlar a velocidade de deslocamento ao animar o ruído. |
| <b>Contraste</b> <i>Flutuante</i> | O contraste do resultado final. |
| <b>Opacidade global</b> <i>Flutuante</i> | A opacidade das oitavas de ruído adicionadas no resultado final.    Um valor alto pode resultar na gravação de áreas em branco. |
| <b>Expansão não quadrada</b> <i>Booleano</i> | Em imagens não quadradas, mantém o ladrilho gerado quadrado e expande a geração de ruído até os limites da imagem. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Base de Soma fractal - Exemplo 1](fractal-sum-base.resources/fractal-sum-base-02.png "Base de Soma fractal - Exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Base de Soma fractal - Exemplo 2](fractal-sum-base.resources/fractal-sum-base-03.gif "Base de Soma fractal - Exemplo 2"){zoomable="yes"}

</td>
</tr>
</table>
