---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/reaction-diffusion-fast.html"
breadcrumb-title: ''
description: Use o nó Difusão de reação rápida para gerar padrões orgânicos usando algoritmos de difusão de reação rápida para texturas de procedimento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Reaction Diffusion Fast
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Difusão de reação rápida
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 1%

---


# Difusão de reação rápida

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó de Difusão de Reação](../../../../../../assets/reaction-diffusion.png "ícone de nó de Difusão de Reação")

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Este nó executa um efeito de difusão de reação em uma imagem de entrada em tons de cinza.

Reação-difusão é um processo no qual a matéria se espalha (difunde) e interage (reage) com outra matéria. É um modelo matemático que simula o que acontece na natureza quando certos padrões se formam na pele de animais, por exemplo.

Esse nó é otimizado para desempenho e faz algumas compensações de precisão por velocidade.

</td>
</tr>
</table>

## Conectores de entrada

<b>Entrada</b> *Tons de cinza* A imagem em tons de cinza à qual o efeito de difusão de reação deve ser aplicado.

## Conectores de saída

<b>Saída </b>*Tons de cinza* A imagem em tons de cinza que representa o efeito de difusão de reação aplicado à imagem de entrada.

## Parâmetros

<b>Raio</b> *Flutuante* Até onde o efeito deve se espalhar.

<b>Contraste</b> *Flutuante*\
Ajusta o contraste da entrada, serve como um tipo de limite.

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo 1](../../../../../../assets/reactdiff03.png "Exemplo 1")

</td>
<td style="border: 0;" valign="top">

![Exemplo 2](../../../../../../assets/reactdiff02.png "Exemplo 2")

</td>
<td style="border: 0;" valign="top">

![Exemplo 3](../../../../../../assets/reactdiff01.gif "Exemplo 3")

</td>
</tr>
</table>
