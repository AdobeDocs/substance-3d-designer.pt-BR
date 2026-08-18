---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-morph.html"
breadcrumb-title: ''
description: Use o nó Morph do vetor para combinar texturas entre duas entradas usando campos de vetor para transições suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Morph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Morph de vetor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---


# Morph de vetor

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/vector-morph-grayscale.png)![](../../../../../../assets/vector-morph.png)

## Morph vetorial (tons de cinza)

**Entrada:** *Filtros/Efeitos*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Distorce uma imagem de entrada por um Mapa vetorial. O efeito é semelhante à distorção UV com um mapa normal ou usando um “mapa de fluxo” em sombreadores de jogos de vídeo. Os pixels de entrada são movidos pelos vetores definidos nos valores Vermelho e Verde do mapa de vetor.

Esse nó em si não é o mais difícil de usar, mas criar um mapa vetorial apropriado é um cuidado. Recomendamos que você trabalhe com as profundidades de bits mais altas para garantir precisão ao fazer a morfagem.

A Morph do vetor é muito semelhante à [Distorção de vetor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md): a principal diferença é que esse nó de Morph não faz “loop” ou “ladrilha” o resultado quando ele é empurrado para fora dos limites da tela. Em vez disso, ela aperta e repete as bordas.

## Parâmetros

### Entradas

* **Entrada**: *Entrada de cor/tons de cinza* A entrada de origem que deve ser o destino da distorção.
* **Campo Vetorial**: *Entrada de Cores* O Mapa Vetorial usado para orientar a distorção.

### Parâmetros

* **Valor**: *0.0 - 1.0* Define a intensidade do efeito de distorção e funciona como um multiplicador para o Mapa de Vetor.

## Imagens de exemplo

</td>
</tr>
</table>
