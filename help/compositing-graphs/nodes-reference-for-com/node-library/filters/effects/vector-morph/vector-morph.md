---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-morph.html"
breadcrumb-title: ''
description: Use o nó Morph do vetor para fazer texturas entre duas entradas usando campos de vetor para transições suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Morph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Morph de vetor
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 2%

---


# Morph de vetor

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/vector-morph-grayscale.png)![](../../../../../../assets/vector-morph.png)

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Distorce uma imagem de entrada por um Mapa vetorial. O efeito é semelhante à distorção UV com um mapa normal ou usando um “mapa de fluxo” em sombreadores de jogos de vídeo. Os pixels de entrada são movidos pelos vetores definidos nos valores Vermelho e Verde do mapa de vetor.

Esse nó em si não é o mais difícil de usar, mas criar um mapa vetorial apropriado é um cuidado. Recomendamos que você trabalhe com as profundidades de bits mais altas para garantir precisão ao fazer a morfagem.

A Morph do vetor é muito semelhante à [Distorção de vetor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md): a principal diferença é que esse nó de Morph não faz “loop” ou “ladrilha” o resultado quando ele é empurrado para fora dos limites da tela. Em vez disso, ela aperta e repete as bordas.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Entrada de Cores/Tons de Cinza</i> | A entrada de origem que deve ser o destino da distorção. |
| <b>Campo de vetor</b> <i>Entrada de cores</i> | O Mapa de vetor usado para direcionar a distorção. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Valor</b> <i>0.0 - 1.0</i> | Define a intensidade do efeito de distorção, que funciona como um multiplicador para o Mapa de vetor. |
