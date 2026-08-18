---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-uv.html"
breadcrumb-title: ''
description: Use o nó Difusão UV para aplicar efeitos de difusão no espaço UV para criar transições e mesclagens de cores suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion UV
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Difusão UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 1%

---


# Difusão UV

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-icon.png){width="200px"}

**Entrada:** *Filtros/Efeitos*

**Intermediário**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrição

Aplique um processo de difusão às coordenadas UV na entrada de imagem **Origem** de acordo com a entrada de imagem **Máscara** fornecida, interpolando coordenadas entre valores da **Origem**.

Apenas UVs de pixels correspondentes à máscara são difundidos; outros pixels não participam do resultado.

Observe que a divisão em blocos gráficos é tratada de uma maneira especial: quando a divisão em blocos gráficos está *habilitada* (o que é o caso por padrão), as coordenadas vizinhas podem ser calculadas em média através do limite de 0/1.

Por exemplo, se o valor da coordenada U for 0,1 em um pixel e 0,8 em outro, o valor médio será 0,95 em vez de 0,45, porque *a divisão lado a lado das coordenadas é assumida*. Isso é independente da posição real do pixel: os valores de coordenadas são tratados da mesma maneira em toda a imagem.

Isso pode levar a resultados indesejados ao usar este filtro para *deformação de textura*. Se isso acontecer, certifique-se de que sua máscara defina “controlar curvas/pontos” com não mais de *metade de um comprimento de textura de um ponto a outro*.

</td>
</tr>
</table>

## Parâmetros

* **Iterações**: *0.0 - 64.0* O número de iterações de difusão a serem executadas (maior é melhor, mas mais lento). Os valores úteis estão no intervalo [8, 48].\
  Observe que, se você não estiver procurando por correção matemática, os valores baixos são ótimos ou até melhores.

## Entradas

* **Origem** *Cor*\
  Os UVs se difundem. Observe que a divisão em blocos gráficos é tratada de maneira especial neste filtro (consulte *Descrição*).
* **Máscara** *Tons de cinza* A máscara de difusão: os pixels brancos são amostrados em *Origem* e difundidos em pixels pretos. A imagem deve ser preta e branca. Se a máscara incluir gradientes, o valor de corte será 0,5.

## Imagens de exemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01a-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01a-after.jpg){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01b-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01b-after.jpg){width="256px"}

</td>
</tr>
</table>
