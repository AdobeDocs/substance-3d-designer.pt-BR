---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-gradient.html"
breadcrumb-title: ''
description: Use o nó Flood Fill para gradiente a fim de preencher regiões com valores de gradiente a fim de criar transições de cores suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill para Gradiente
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 7%

---


# Flood Fill para Gradiente

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-gradient.resources/flood-fill-to-gradient-01.png){width="128px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Transforma uma base [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md) em gradientes (orientados aleatoriamente). Muito útil para criar um Heightmap onde os ladrilhos são aleatoriamente inclinados e inclinados.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Flood Fill</b> <i>Entrada de cores</i> | Dados de Flood Fill base. |
| <b>Entrada de ângulo</b> <i>Entrada em tons de cinza</i> | Mapa opcional para determinar o ângulo por célula com um mapa externo. |
| <b>Entrada de Inclinação</b> <i>Entrada em tons de cinza</i> | Mapa opcional para determinar a intensidade de inclinação do gradiente por célula. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Ângulo</b> <i>0.0 - 1.0</i> | Define um ângulo/direção global uniforme para todos os ladrilhos. |
| <b>Variação de ângulo</b> <i>0.0 - 1.0</i> | Dispõe aleatoriamente o ângulo de cada peça individualmente. Este é o parâmetro mais útil e poderoso! |
| <b>Multiplicar pelo tamanho da caixa delimitadora</b> <i>0.0 - 1.0</i> | Dimensiona todo o efeito linear pelo tamanho da caixa delimitadora individual do ladrilho. Isso significa que os ladrilhos menores acabarão sendo mais escuros do que os maiores. |
| <b>Multiplicador de Entrada de Imagem de Ângulo</b> <i>0.0 - 1.0</i> | Definir a influência do mapa de entrada de ângulo opcional nas direções de gradiente geradas |
| <b>Multiplicador de Entrada de Imagem de Inclinação</b> <i>0.0 - 1.0</i> | Defina a influência do mapa de entrada de Inclinação opcional na intensidade de inclinação do gradiente gerado. |
| <b>Multiplicar por Intensidade de Inclinação</b> <i>0.0 - 1.0</i> |  |
| <b>Cor de Inclinação plana</b> <i>(Valor em tons de cinza)</i> | Permite a configuração de valor sólido para inclinações simples. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-gradient.resources/flood-fill-to-gradient-02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-gradient.resources/flood-fill-to-gradient-03.png" />
        </td>
    </tr>
</table>
