---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/preview-paths.html"
breadcrumb-title: ''
description: Use o nó Visualizar caminhos para visualizar dados de caminho na visualização 2D para depuração e verificação.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Preview Paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Visualizar demarcadores
user-guide-description: ''
user-guide-title: ''
source-git-commit: f9ae596767e754b5c0f62ed6bdb6f16dd33bb799
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---


# Visualizar demarcadores

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](preview-paths.resources/preview-paths-icon.png "Ícone de nó")

<b>Ferramentas de Spline e Caminho </b> > Ferramentas de Caminho

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Traça segmentos e vértices do caminho em cima do plano de fundo fornecido. Uma cor aleatória por caminho.

Você obterá um resultado semelhante à saída <b>Visualizar</b> de [Mascarar para Caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md), mas com mais opções.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Fundo</b> <i>Cor</i> | Uma imagem de fundo na parte superior exibe o caminho. Isso também controla o tamanho da renderização. |
| <b>Caminhos</b> <i>Cor</i> | Uma lista de caminhos de segmentos codificados. Conecte esta entrada ao resultado de uma [Máscara para Caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) ou a outro nó de processamento de Caminho. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Mostrar Cantos</b> <i>Booleano</i> | Exibe um quadrado em cada vértice marcado como canto (mesclagem aditiva). |
| <b>Mostrar vértices</b> <i>Booleano</i> | Exibe uma forma circular em cada vértice (mistura aditiva). Os cantos ainda são exibidos como quadrados. |
| <b>Thickness de segmentos (px)</b> <i>Flutuante</i> | Ajusta o thickness de segmentos renderizados em pixels. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 1](preview-paths.resources/PathsToSpline-Variant2-Before_1.jpg "Exemplo de nó 1")

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](preview-paths.resources/PathsToSpline-Variant1-Before_1.jpg "Exemplo de nó 2")

</td>
</tr>
</table>
