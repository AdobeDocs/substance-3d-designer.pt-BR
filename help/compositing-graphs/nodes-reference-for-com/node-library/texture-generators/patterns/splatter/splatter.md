---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter.html"
breadcrumb-title: ''
description: Use o nó respingos para dispersão formas entre texturas para criar padrões aleatórios e detalhes de textura orgânica.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Respingo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 9%

---


# Respingo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](splatter.resources/splatter-01.png)

![](splatter.resources/splatter-02.png)

<b>Em:</b> Geradores De Textura > Padrões

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Splatter é um gerador de padrões destinado ao posicionamento aleatório de uma entrada de mapa. Ele tem muitos controles para posicionamento geometricamente padronizado e é mais simples em uso do que o [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Este último pode alcançar resultados semelhantes, mas é muito mais complexo.

O Splatter funciona bem para rapidamente carimbar algumas formas, sem precisar de muitos ajustes.

Lembre-se de que os parâmetros padrão de Splatter não parecem aleatórios: você precisa ajustar alguns deles para obter aleatoriedade (principalmente parâmetros de desordem). Lembre-se também de que o Splatter requer uma entrada de mapa para funcionar.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Largura do Tamanho do Padrão</b> <i>0.0 - 1000.0</i> | Número de padrões a serem usados no eixo X. |
| <b>Height de Tamanho de Padrão</b> <i>0.0 - 1000.0</i> | Número de padrões a serem usados no eixo Y. |
| <b>Rotação</b> <i>-360.0 - 360.0</i> | Gira cada padrão por um valor definido. |
| <b>Variação de Rotação</b> <i>0.0 - 360.0</i> | Introduz rotação aleatória para cada forma separada. |
| <b>Zoom</b> <i>100.0 - 10000.0</i> | Aumenta o resultado final. Lembre-se de que isso quebra a divisão em blocos gráficos! |
| <b>Ganho</b> <i>0.0 - 10.0</i> | Ajusta o ganho de mesclagem de cada padrão. Faz com que se destaquem mais. |
| <b>Panorâmica X</b> <i>-100.0 - 100.0</i> | Desloca o resultado inteiro no eixo X. |
| <b>Panorâmica Y</b> <i>-100.0 - 100.0</i> | Desloca o resultado inteiro no eixo Y. |
| <b>Desordem</b> <i>0.0 - 100.0</i> | Desloca as formas aleatoriamente. |
| <b>Número da Grade</b> <i>0 - 8</i> | Salta por diferentes tamanhos de grade para ajustar a escala dos resultados. Mantém a divisão em blocos gráficos. |
| <b>Ângulo de Desordem</b> <i>0.0 - 360.0</i> | Controla o ângulo de deslocamento da desordem. |
| <b>Desordem Aleatória</b> <i>Falso/Verdadeiro</i> | Dispõe aleatoriamente o ângulo da desordem, adicionando muito mais caos. |
| <b>Tamanho do padrão</b> <i>5 - 12</i> |  |
| <b>Variação de Tamanho</b> <i>0.0 - 100.0</i> | Introduz escala aleatória para cada forma. |
| <b>Filtragem de Entrada de Imagem (Mecanismo > somente v4)</b> <i>Bilinear + Mipmaps, Bilinear, Mais Próximo</i> | Qual filtragem aplicar à imagem de entrada. |
| <b>Nível de Saída Mínimo</b> <i>0.0 - 1.0</i> | Ajuste de nível mínimo de saída. |
| <b>Nível Máximo de Saída</b> <i>0.0 - 1.0</i> | Ajuste de nível máximo de saída. |
| <b>Cor do plano de fundo</b> <i>(Valor em tons de cinza)</i> | Define a cor sólida do plano de fundo. |
| <b>Variação de luminância</b> <i>0.0 - 1.0 (somente versão em Tons de Cinza)</i> | Introduz a variação de luminância. |
| <b>Variação de cor</b> <i>0.0 - 1.0 (Somente Versão de Cores)</i> | Apresenta a variação de cores. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="splatter.resources/splatter-03.gif" />
        </td>
    </tr>
</table>
