---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/directional-blur.html"
breadcrumb-title: ""
description: Use o nó Desfoque direcional para aplicar efeitos de desfoque em uma direção específica para criar efeitos de desfoque de movimento e listras.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Directional blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desfoque direcional
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 8%
---

# Desfoque direcional

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![Nó atômico: desfoque direcional](directional-blur.resources/comp_dirmotionblur_1.png "Nó atômico: desfoque direcional"){width="100%"}

<b>Entrada:</b> Nós Atômicos

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

Aplica desfoque em uma direção especificada, de acordo com um mapa de intensidade.

Este nó executa uma operação semelhante a um desfoque de movimento em uma entrada. Diferentemente do nó regular de &#39;[Desfoque](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)&#39;, que desfoca igualmente em todas as direções, o &#39;Desfoque direcional&#39; funciona em um ângulo definido pelo usuário.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="directional-blur.resources/directional-blur-tooltip.gif" alt="dica de ferramenta de desfoque direcional" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>

Semelhante ao “Desfoque”, também é uma operação mais rápida e de baixa qualidade. Uma alternativa estendida e de maior qualidade é fornecida no [Desfoque Anisotrópico](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md), com uma compensação de desempenho


## Desfoque direcional e anisotrópico

As imagens abaixo mostram o desfoque direcional e o [desfoque anisotrópico](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md) em vigor na mesma forma de entrada, com parâmetros semelhantes. O Desfoque anisotrópico foi definido como anisotropia total e alta qualidade.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Desfoque direcional</b>

![Comparação de desfoque direcional](directional-blur.resources/dirblur-01.png "Comparação de desfoque direcional"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

<b>Desfoque anisotrópico</b>

![Comparação de desfoque anisotrópico](directional-blur.resources/aniso-01.png "Comparação de desfoque anisotrópico"){zoomable="yes"}

</td>
</tr>
</table>


## Parâmetros

|  |  |
| --- | --- |
| <b>Intensidade</b> *Precisão decimal* | Define o raio de desfoque em pixels. |
| <b>Ângulo</b> *Precisão decimal* | A direção do efeito de desfoque em número de voltas no sentido horário, começando na horizontal, ou seja, vetor de direção (1, 0). |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Tons de Cinza/Cor* [PRIMÁRIO](../../../../glossary/glossary.md) | A imagem a ser processada. |


## Exemplos

*Em breve.*
