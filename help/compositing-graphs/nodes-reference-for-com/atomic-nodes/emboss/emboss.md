---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/emboss.html"
breadcrumb-title: ""
description: Use o nó Entalhe para criar efeitos em alto-relevo nas texturas para adicionar profundidade e relevo aos detalhes da superfície.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Entalhe
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 9%
---

# Entalhe

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![Nó atômico: Entalhe](emboss.resources/comp_emboss_1.png "Nó atômico: Entalhe"){width="100%"}

<b>Entrada:</b> Nós Atômicos

</td>
<td style="border: 0;" valign="top">

Aplica um efeito de relevo iluminando os lados das formas em uma imagem de acordo com a direção de uma fonte de luz especificada.

Ou seja, o nó executa um sombreamento 2D simples com base em 2 entradas, simulando a luz caindo em uma superfície com variação de height e profundidade.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="emboss.resources/emboss-tooltip.gif" alt="Dica de ferramenta de relevo" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

Esse nó não é usado com frequência para projetos do tipo PBR, mas pode servir em determinados casos em que você deseja uma iluminação assada simples na textura. Como alternativa, o [Entalhe com Brilho](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/emboss-with-gloss/emboss-with-gloss.md) e o [Entalhe Uber](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md) oferecem uma funcionalidade semelhante, porém mais ampla.



## Parâmetros

|  |  |
| --- | --- |
| <b>Intensidade</b> *Flutuante* | Ajusta a intensidade global do efeito de iluminação.   Define a intensidade da luz do mapa de “height” e, portanto, a intensidade do efeito de iluminação |
| <b>Ângulo claro</b> *Flutuante* | Define o ângulo em que a luz é simulada.   Define o ângulo de iluminação do realce da imagem em alto-relevo |
| <b>Cor de realce</b> *Flutuante/Flutuante4* | Define a cor das áreas voltadas para o ângulo claro.   Define a cor do realce se a imagem de entrada for colorida. |
| <b>Cor da sombra</b> *Flutuante/Flutuante4* | Define a cor das áreas opostas ao ângulo claro.   Define a cor das regiões sombreadas da imagem em alto-relevo. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Tons de Cinza/Cor* PRIMÁRIO | Fornece a base, cores não sombreadas. Vê-lo como um tipo de textura difusa ou de cor base. |
| <b>Entrada de intensidade</b> *Tons de cinza* | Representa o mapa de altura usado para calcular a iluminação na superfície. Preto é baixo e branco é alto. |


## Exemplos

*Em breve.*
