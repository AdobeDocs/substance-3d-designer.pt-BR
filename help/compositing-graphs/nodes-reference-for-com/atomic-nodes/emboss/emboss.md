---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/emboss.html"
breadcrumb-title: ""
description: Use o nó Relevo para criar efeitos em relevo nas texturas para adicionar profundidade e relevo aos detalhes da superfície.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Entalhe
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 9%
---

# Entalhe

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![Nó atômico: Relevo](emboss.resources/comp_emboss_1.png "Nó atômico: Relevo"){width="100%"}

<b>Entrada:</b> Nós Atômicos

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

Aplica um efeito de relevo iluminando os lados das formas em uma imagem de acordo com a direção de uma fonte de luz especificada.

Ou seja, o nó executa um sombreamento 2D simples com base em 2 entradas, simulando a luz caindo em uma superfície com variação de height e profundidade.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="emboss.resources/emboss-tooltip.gif" alt="Dica de ferramenta de relevo" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>

Esse nó não é usado com frequência para projetos do tipo PBR, mas pode servir em determinados casos em que você deseja uma iluminação simples e feita bake na textura. Como alternativa, o [Relevo com Brilho](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/emboss-with-gloss/emboss-with-gloss.md) e o [Relevo Uber](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md) fornecem uma funcionalidade semelhante, mas mais ampla.



## Parâmetros

|  |  |
| --- | --- |
| <b>Intensidade</b> *Precisão decimal* | Ajusta a intensidade global do efeito de iluminação.   Define a intensidade da luz do mapa de “height” e, portanto, a intensidade do efeito de iluminação |
| <b>Ângulo claro</b> *Precisão decimal* | Define o ângulo em que a luz é simulada.   Define o ângulo de iluminação do realce da imagem em alto-relevo |
| <b>Cor de realce</b> *Precisão decimal/Precisão decimal 4* | Define a cor das áreas voltadas para o ângulo claro.   Define a cor do realce se a imagem de entrada for colorida. |
| <b>Cor da sombra</b> *Precisão decimal/Precisão decimal 4* | Define a cor das áreas opostas ao ângulo claro.   Define a cor das regiões sombreadas da imagem em alto-relevo. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Tons de Cinza/Cor* PRIMÁRIO | Fornece a base, cores não sombreadas. Veja como um tipo de textura difusa ou de basecolor. |
| <b>Entrada de intensidade</b> *Tons de cinza* | Representa o mapa de altura usado para calcular a iluminação na superfície. Preto é baixo e branco é alto. |


## Exemplos

*Em breve.*
