---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/blur-hq.html"
breadcrumb-title: ''
description: Use o nó HQ de desfoque para aplicar efeitos de desfoque de alta qualidade a texturas a fim de criar resultados suaves de desfoque de aparência profissional.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Blur HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desfoque HQ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 5%

---


# Desfoque HQ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/blur-hq-1.png){width="128px"}

![](../../../../../../assets/blur-hq-grayscale.png){width="128px"}

## Desfocar sede (tons de cinza)

**Entrada:** *Filtros/Desfoques*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Executa um desfoque gaussiano de alta qualidade no resultado. Qualidade muito melhor do que [o desfoque padrão da caixa atômica](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) [.](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)

Importante: certifique-se de usar a versão apropriada para sua entrada! Use “Desfoque HQ” para entradas de cor ou “Desfoque HQ em tons de cinza” para entradas em tons de cinza.

## Parâmetros

* **Intensidade**: *0.0 - 16.0*\
  Intensidade (Raio) do desfoque. Quanto maior for esse valor, mais o desfoque alcançará.
* **Qualidade**: *0 - 1* aumenta a quantidade de amostragem interna para obter uma qualidade ainda maior, em uma velocidade de computação reduzida.

## Imagens de exemplo

![](../../../../../../assets/hqblur-example.gif)

</td>
</tr>
</table>
