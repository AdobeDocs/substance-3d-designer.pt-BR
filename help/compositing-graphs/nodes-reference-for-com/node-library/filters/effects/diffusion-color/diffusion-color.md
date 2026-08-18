---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-color.html"
breadcrumb-title: ''
description: Use o nó Cor de difusão para aplicar efeitos de difusão de cores para criar transições e misturas de cores suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cor de difusão
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 3%

---


# Cor de difusão

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-color-icon.png){width="200px"}

**Entrada:** *Filtros/Efeitos*

**Intermediário**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrição

Aplique um processo de difusão às cores na entrada de imagem de **Origem** de acordo com a entrada de imagem da **Máscara** fornecida, criando gradações suaves entre as cores ao usar o [Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html).

Somente as cores de pixels correspondentes à máscara são difusas; outros pixels não participam do resultado.

</td>
</tr>
</table>

## Parâmetros

* **Iterações**: *0.0 - 64.0* O número de iterações de difusão a serem executadas (maior é melhor, mas mais lento). Os valores úteis estão no intervalo [8, 48].\
  Observe que, se você não estiver procurando por correção matemática, os valores baixos são ótimos ou até melhores.\
  **Distância**: **0.0 - 1.0** Ajusta a distância máxima da difusão.
* **Habilitar Pontilhamento**: *Verdadeiro/Falso* Controla o método de amostragem de cada passagem. O pontilhamento permite a convergência em menos passagens, mas introduz ruído.\
  Sem ele, cada passagem é mais rápida, mas são necessárias mais passagens para obter um resultado suave sem artefatos de faixa.
* **É Mapa Normal**: *Verdadeiro/Falso* Adiciona uma normalização em valores em cada etapa.
* **Usar Alpha como Máscara**: *Verdadeiro/Falso* Usar o canal alfa da entrada *Origem* como a máscara de difusão, em vez da entrada *Máscara*.

## Entradas

* **Origem** *Cor*\
  A imagem a ser difundida.
* **Máscara** *Tons de cinza*\
  Máscara de difusão: os pixels brancos são amostrados em *Origem* e difundidos em pixels pretos. A imagem deve ser preta e branca. Se a máscara incluir gradientes, o valor de corte será 0,5.
* **Intensidade** *Tons de cinza*\
  Define localmente o grau de aplicação do processo de difusão. Este mapa deve ser *contrastado* para obter um efeito perceptível.

## Imagens de exemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-color-02-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-color-02a-after.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-color-02b-after.jpg){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-color-01-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01b-after-1.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01a-after-1.jpg){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-color-normal.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-color-normal-render.jpg){width="512px"}

</td>
</tr>
</table>
