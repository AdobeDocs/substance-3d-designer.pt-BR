---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-grayscale.html"
breadcrumb-title: ''
description: Use o nó Tons de cinza de difusão para aplicar efeitos de difusão em tons de cinza para criar transições e mesclagens de cores suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Escala de cinza de difusão
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 1%

---


# Escala de cinza de difusão

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-icon.png){width="200px"}

**Entrada:** *Filtros/Efeitos*

**Intermediário**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrição

Aplique um processo de difusão aos valores na entrada de imagem **Origem** de acordo com a entrada de imagem **Máscara** fornecida, criando gradações suaves entre os valores.

Somente os valores de pixels correspondentes à máscara são difundidos; outros pixels não participam do resultado.

</td>
</tr>
</table>

## Parâmetros

* **Iterações**: *0.0 - 64.0* O número de iterações de difusão a serem executadas (maior é melhor, mas mais lento). Os valores úteis estão no intervalo [8, 48].\
  Observe que, se você não estiver procurando por correção matemática, os valores baixos são ótimos ou até melhores.\
  **Distância**: **0.0 - 1.0** Ajusta a distância máxima da difusão.
* **Habilitar Pontilhamento**: *Verdadeiro/Falso* Controla o método de amostragem de cada passagem. O pontilhamento permite a convergência em menos passagens, mas introduz ruído.\
  Sem ele, cada passagem é mais rápida, mas são necessárias mais passagens para obter um resultado suave sem artefatos de faixa.

## Entradas

* **Origem** *Tons de Cinza*\
  A imagem a ser difundida.
* **Máscara** *Tons de cinza*\
  Máscara de difusão: os pixels brancos são amostrados em *Origem* e difundidos em pixels pretos. A imagem deve ser preta e branca. Se a máscara incluir gradientes, o valor de corte será 0,5.
* **Intensidade** *Tons de cinza*\
  Define localmente o grau de aplicação do processo de difusão. Este mapa deve ser *contrastado* para obter um efeito perceptível.

## Imagens de exemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-01-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-01a-after.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-01b-after.jpg){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-02-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-02-after.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-grayscale-02-render.jpg){width="512px"}

</td>
</tr>
</table>
