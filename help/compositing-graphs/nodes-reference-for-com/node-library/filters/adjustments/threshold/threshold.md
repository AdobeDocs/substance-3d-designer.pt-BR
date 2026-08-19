---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/threshold.html"
breadcrumb-title: ''
description: Use o nó Limite para converter texturas em tons de cinza em preto e branco com base em um valor de limite para criar máscaras.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Threshold
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Limiar
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---


# Limiar

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/threshold-2.png){width="200px"}

## Limiar

**Entrada:** *Filtros/Ajustes*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Retorna branco se os *critérios de comparação* definidos no parâmetro **Modo** forem atendidos para o valor de pixel de entrada relativamente ao valor **Limite**.\
Semelhante à [Verificação do histograma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), mas com contraste sempre no nível máximo. Funciona como uma maneira mais precisa e rápida de obter resultados semelhantes à Varredura de histograma.

### Parâmetros

* **Limite**: *0.0 - 1.0*\
  Valor de luminância com o qual o valor de pixel de entrada é comparado.
* **Modo**:\
  O critério pelo qual o valor de pixel de entrada deve ser comparado com o valor de **Limite**:
  * *Superior*
  * *Maior ou igual*
  * *Inferior*
  * *Inferior ou igual*

## Imagens de exemplo

</td>
</tr>
</table>
