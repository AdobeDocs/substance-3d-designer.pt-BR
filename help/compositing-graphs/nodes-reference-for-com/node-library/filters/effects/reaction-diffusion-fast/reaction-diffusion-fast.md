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
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 3%

---


# Difusão de reação rápida

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó de Difusão de Reação](reaction-diffusion-fast.resources/reaction-diffusion.png "ícone de nó de Difusão de Reação")

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

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Tons de cinza</i> | A imagem em tons de cinza à qual o efeito de difusão-reação deve ser aplicado. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Saída</b> <i>Tons de cinza</i> | A imagem em tons de cinza que representa o efeito de difusão de reação aplicado à imagem de entrada. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Raio</b> *Flutuante* | Até onde o efeito deve se espalhar. |
| <b>Contraste</b> *Flutuante* | Ajusta o contraste da entrada, serve como um tipo de limite. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo 1](reaction-diffusion-fast.resources/reactdiff03.png "Exemplo 1")

</td>
<td style="border: 0;" valign="top">

![Exemplo 2](reaction-diffusion-fast.resources/reactdiff02.png "Exemplo 2")

</td>
<td style="border: 0;" valign="top">

![Exemplo 3](reaction-diffusion-fast.resources/reactdiff01.gif "Exemplo 3")

</td>
</tr>
</table>
