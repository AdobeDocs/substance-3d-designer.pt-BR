---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/sharpen.html"
breadcrumb-title: ''
description: Use o nó Nitidez para aprimorar os detalhes e as bordas da textura para criar detalhes nítidos e definidos da superfície.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Sharpen
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nitidez
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 4%

---


# Nitidez

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone do nó de nitidez](../../../../assets/sharpen-4.png "ícone do nó de nitidez")

<b>Entrada:</b> Nós Atômicos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O Nó de nitidez executa uma operação de nitidez em uma entrada. É um nó útil para aplicar aquele toque final de nitidez a uma imagem.

</td>
</tr>
</table>

É matematicamente muito semelhante à Máscara de nitidez da Photoshop, apesar do nome ser diferente. Funciona bem para coisas como um mapa de Basecolor, mas deve ser evitado em mapas como Mapas normais e mapas metálicos.

## Entradas

<b>Entrada</b> *Cores/Tons de Cinza* (Primário)\
A imagem que deve ter a nitidez ajustada.

## Parâmetros

<b>Intensidade</b> *Precisão decimal*\
Define a intensidade do efeito de nitidez.

<b>Alpha de perfuração</b> *Booleano* (Disponível quando uma imagem colorida está conectada à <b>Entrada</b>)\
Determina se o canal alfa da imagem deve ter a nitidez ajustada ou permanecer intacto.

## Exemplos

![Nó de nitidez - Exemplo 1](../../../../assets/sharpen-ex.png "Nó de nitidez - Exemplo 1")
