---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/clone-filter-node.html"
breadcrumb-title: ''
description: Use o nó do filtro Clonar para duplicar e deslocar regiões de textura para criar padrões perfeitos e efeitos de divisão em blocos gráficos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Clone (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Clonar (Nó de Filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 4%

---


# Clonar (Nó de Filtro)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](clone-filter-node.resources/clone-4.png)

<b>Entrada:</b> Filtros > Transformas

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Clonar uma vez na imagem de entrada para um local especificado. Pode funcionar como uma ferramenta bruta de “carimbo”.

Requer um pouco de cuidado para obter os resultados desejados:

* O ideal é que a imagem de entrada tenha um canal alfa (como um decalque), uma vez que a mesclagem é apenas uma cópia reta.
* O padrão da máscara é preto. Portanto, para ver os resultados, um valor uniforme de tons de cinza branco precisa ser conectado, pelo menos.
* O Deslocamento recortará fora da imagem facilmente, portanto, use valores pequenos.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Origem</b> <i>Entrada de cores</i> | Imagem para clonar. Importante: o ideal é que a imagem tenha um canal alfa! |
| <b>Máscara</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. O padrão é preto! |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Deslocamento</b> <i>-</i> | Move ou traduz o resultado. Positivo é para a esquerda e para cima, Negativo é para a direita e para baixo. Use valores pequenos. A versão 1.0 ou posterior move o texto para fora da imagem. |
| <b>Máscara de desfoque</b> <i>0.0 - 10.0</i> | Aplique um filtro de desfoque à máscara para suavizar as arestas. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="clone-filter-node.resources/clone-example.png" />
        </td>
    </tr>
</table>
