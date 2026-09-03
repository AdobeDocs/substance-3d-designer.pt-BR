---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/normal.html"
breadcrumb-title: ''
description: Use o nó Normal para processar e manipular texturas de mapa normal para controlar os detalhes da superfície e a iluminação.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 8%

---


# Normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: Normal](normal.resources/normal-01.png "Nó atômico: Normal"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Calcula um mapa normal a partir de uma imagem em tons de cinza interpretada como um mapa de altura.

O nó converte um mapa de entrada em tons de cinza em uma saída de Mapa normal de espaço tangente. Ele tem algumas opções de usuário para definir a intensidade e a codificação.

</td>
</tr>
</table>

É um nó muito útil que é usado frequentemente para converter entradas de mapas de height em mapas normais para materiais prontos em tempo real. Existem alternativas a serem encontradas no [Normal Sobel](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-sobel/normal-sobel.md) e no Height para Unidades Mundiais Normais.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Conectores de saída

</td>
<td style="border: 0;" valign="top">

### Exemplos

</td>
</tr>
</table>

## Parâmetros

|  |  |
| --- | --- |
| <b>Intensidade</b> *Precisão decimal* | Modifica a intensidade do mapa de altura.   Define a intensidade com que o mapa de height de entrada é interpretado para conversão em normais. Dependendo dos mapas de entrada, valores acima de 100 têm pouco mais efeito. |
| <b>Formato normal</b> *Booleano* | Inverte as coordenadas Y do mapa de altura (OpenGL).   Define como o canal Verde (Y) é codificado. Basicamente, um interruptor “Flip Green/Y”. |
| <b>Conteúdo do canal alfa</b> *Booleano* | Preencha o canal alfa da mapa normal com a textura de entrada.   Preencher Alpha com entrada/forçar Alpha para 1: permite que o canal alfa seja definido como sólido, em vez de usar a entrada como um Alpha adicional. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Tons de cinza* PRIMÁRIO | Imagem de entrada interpretada como um mapa de altura. |

## Conectores de saída

|  |  |
| --- | --- |
| <b>Saída</b> *Cor* |  |

## Exemplos

*Em breve.*
