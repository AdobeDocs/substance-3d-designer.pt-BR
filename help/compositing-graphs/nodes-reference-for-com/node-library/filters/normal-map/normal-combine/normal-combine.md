---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-combine.html"
breadcrumb-title: ''
description: Use o nó Combinação normal para combinar vários mapas normais para detalhes e detalhes da superfície da camada.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Combine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Combinação normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---


# Combinação normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/normal-combine.png){width="128px"}

<b>Entrada:</b> Filtros > Mapa normal

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Combinação normal combina os detalhes de dois mapas normais de uma maneira matemática correta.

É semelhante ao método conhecido de “Sobreposição” de outros softwares de edição de imagens em 2D, mas funciona de forma ligeiramente diferente internamente (três opções).

</td>
</tr>
</table>

Esta é a melhor e mais correta maneira de adicionar detalhes de mapa normal gerados em 2D a um mapa baked.

Se você quiser mesclar dois mapas normais sem combinar seus detalhes (usando uma máscara, por exemplo), use a [Mesclagem normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-blend/normal-blend.md).

## Conectores de entrada

<b>Normal 2</b> *Cor* Descrição

<b>Normal</b> *Cor* Descrição

## Parâmetros

<b>Técnica</b> *Inteiro* Define qual técnica de mesclagem interna usar, trocando em velocidade por qualidade.\
*- Whiteout (Baixa qualidade)
* Misturador de canais (alta qualidade)
* Orientado a detalhes (alta qualidade)*

## Exemplos
