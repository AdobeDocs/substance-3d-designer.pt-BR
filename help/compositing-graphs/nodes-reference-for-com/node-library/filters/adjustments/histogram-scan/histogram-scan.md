---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan.html"
breadcrumb-title: ''
description: Use o nó Varredura de histograma para digitalizar e analisar histogramas de textura para correção e ajustes de cores.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Varredura de histograma
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 5%

---


# Varredura de histograma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/histogram-scan-1.png){width="128px"}

## Varredura de histograma

**Entrada:** *Filtros/Ajustes*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Nó muito simples, mas útil, que fornece uma maneira intuitiva de remapear o contraste e o brilho das imagens em tons de cinza de entrada. Pode ser usado para “aumentar” e “encolher” máscaras de maneiras dinâmicas.

[Clique aqui para assistir a um vídeo do Substance Academy sobre operações do histograma.](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=427s)

## Parâmetros

* **Posição**: *0.0 - 1.0* Semelhante a um controle de brilho, desloca o ponto médio do resultado. Quando usado em uma entrada de gradiente, expande e encolhe o ponto de transição.\
  Importante: um valor padrão de 0 significa que o resultado final está sempre preto. Portanto, tente começar com 0,5!
* **Contraste**: *0.0 - 1.0*\
  Ajusta o contraste do resultado. Pode ser usado para definir a rigidez da transição.
* **Inverter Posição**: *Falso/Verdadeiro* Inverte o resultado final.

## Imagens de exemplo

![](../../../../../../assets/histogram-scan.gif)

![](../../../../../../assets/histogram-scan2.gif)

![](../../../../../../assets/histogram-scan3.gif)

</td>
</tr>
</table>
