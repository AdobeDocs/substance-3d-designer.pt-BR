---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/messy-fibers-1.html"
breadcrumb-title: ''
description: Use o nó Messy Fibres 1 para gerar padrões básicos de fibra para criar detalhes de tecido e textura têxtil.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Messy fibers 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fibras bagunçadas 1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%

---


# Fibras bagunçadas 1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Fibras bagunçadas 1 - Ícone](messy-fibers-1.resources/messy-fibers-1-01.png "Fibras bagunçadas 1 - Ícone"){width="200px"}

<b>Entrada:</b> geradores de textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma variação dos <b>ruídos estruturados de fibras desordenadas</b>.

Veja também: [Fibras confusas 2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-2/messy-fibers-2.md), [Fibras confusas 3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/messy-fibers-3/messy-fibers-3.md)

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
| <b>ângulo de anisotropia de desordem</b> <i>Flutuante</i> | Controla a direção do deslocamento aplicado pelo parâmetro <b>Desordem</b> quando o parâmetro &#39;anisotropia de Desordem&#39; não é zero. |
| <b>Ângulo</b> <i>Precisão decimal</i> | O ângulo usado para definir a direção dos encadeamentos, em número de voltas e começando da direita horizontal. |
| <b>Ângulo aleatório</b> <i>Flutuante</i> | O valor máximo de variação aleatória aplicado ao valor <b>Ângulo</b>, em número de voltas. |
| <b>Número de linhas</b> <i>Precisão decimal</i> | A quantidade de divisão em blocos gráficos aplicada aos encadeamentos de base, em que um valor mais alto resulta em encadeamentos mais densos e mais finos. |
| <b>Deslocamento do bloco</b> <i>Precisão decimal 2</i> | Controla a posição da parte de plano infinito usada para renderizar o ruído. |
| <b>Expansão não quadrada</b> <i>Booleano</i> | Em imagens não quadradas, mantém o ladrilho gerado quadrado e expande a geração de ruído até os limites da imagem. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Fibras bagunçadas 1 - Ícone](messy-fibers-1.resources/messy-fibers-1-02.png "Fibras bagunçadas 1 - Ícone"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Fibras bagunçadas 1 - Exemplo 2](messy-fibers-1.resources/messy-fibers-1-03.gif "Fibras bagunçadas 1 - Exemplo 2"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Fibras bagunçadas 1 - Exemplo 3](messy-fibers-1.resources/messy-fibers-1-04.gif "Fibras bagunçadas 1 - Exemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Fibras bagunçadas 1 - Exemplo 4](messy-fibers-1.resources/messy-fibers-1-05.gif "Fibras bagunçadas 1 - Exemplo 4"){zoomable="yes"}

</td>
</tr>
</table>
