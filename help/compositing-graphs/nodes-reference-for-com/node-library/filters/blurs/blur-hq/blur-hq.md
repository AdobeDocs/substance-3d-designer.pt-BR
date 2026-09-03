---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/blur-hq.html"
breadcrumb-title: ''
description: Use o nó HQ de desfoque para aplicar efeitos de desfoque de alta qualidade às texturas a fim de criar resultados suaves de desfoque de aparência profissional.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Blur HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desfoque HQ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 10%

---


# Desfoque HQ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](blur-hq.resources/blur-hq-01.png){width="128px"}

![](blur-hq.resources/blur-hq-02.png){width="128px"}

<b>Entrada:</b> Filtros > Desfoques

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Executa um desfoque gaussiano de alta qualidade no resultado. Qualidade muito melhor do que [o desfoque padrão da caixa atômica](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md) [.](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)

Importante: certifique-se de usar a versão apropriada para sua entrada! Use “Desfoque HQ” para entradas de cor ou “Desfoque HQ em tons de cinza” para entradas em tons de cinza.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Intensidade</b> <i>0.0 - 16.0</i> | Intensidade (Raio) do desfoque. Quanto maior for esse valor, mais o desfoque alcançará. |
| Qualidade <b>1</b> <i>0 - 1</i> | Aumenta a quantidade de amostragem interna para obter uma qualidade ainda maior, com velocidade de computação reduzida. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="blur-hq.resources/blur-hq-03.gif" />
        </td>
    </tr>
</table>
