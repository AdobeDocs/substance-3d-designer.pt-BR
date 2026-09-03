---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/sharpen.html"
breadcrumb-title: ''
description: Use o nó Nitidez para aprimorar os detalhes e as bordas da textura e criar detalhes nítidos e definidos da superfície.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Sharpen
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nitidez
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 4%

---


# Nitidez

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone do nó de nitidez](sharpen.resources/sharpen-01.png "ícone do nó de nitidez")

<b>Entrada:</b> Nós Atômicos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O Nó de nitidez executa uma operação de nitidez em uma entrada. É um nó útil para aplicar aquele toque final de nitidez a uma imagem.

</td>
</tr>
</table>

É matematicamente muito semelhante à Máscara de nitidez da Photoshop, apesar do nome ser diferente. Funciona bem para coisas como o mapa Basecolor, mas deve ser evitado em mapas como o Normal e o Metálico.

## Entradas

<b>Entrada</b> *Cores/Tons de Cinza* (Primário)\
A imagem que deve ter a nitidez ajustada.

## Parâmetros

<b>Intensidade</b> *Flutuante*\
Define a intensidade do efeito de nitidez.

<b>Alpha de perfuração</b> *Booleano* (Disponível quando uma imagem colorida está conectada à <b>Entrada</b>)\
Determina se o canal alfa da imagem deve ter a nitidez ajustada ou permanecer intacto.

## Exemplos

![Nó de nitidez - Exemplo 1](sharpen.resources/sharpen-02.png "Nó de nitidez - Exemplo 1")
