---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/normal.html"
breadcrumb-title: ''
description: Use o nó Normal para processar e manipular texturas normais do mapa para controlar detalhes da superfície e iluminação.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8b6f65bd88f3c83bf6682c7bca91615166389a91
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 8%

---


# Normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: Normal](normal.resources/comp_normal_1.png "Nó atômico: Normal"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Calcula um mapa normal a partir de uma imagem em tons de cinza interpretada como um mapa de altura.

O nó converte um mapa de entrada em tons de cinza em uma saída de mapa normal de espaço tangente. Ele tem algumas opções de usuário para definir a intensidade e a codificação.

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
| <b>Intensidade</b> *Flutuante* | Modifica a intensidade do mapa de height.   Define a intensidade com que o mapa de height de entrada é interpretado para conversão em normais. Dependendo dos mapas de entrada, valores acima de 100 têm pouco mais efeito. |
| <b>Formato normal</b> *Booleano* | Inverte as coordenadas Y do mapa de height (OpenGL).   Define como o canal Verde (Y) é codificado. Basicamente, um interruptor “Flip Green/Y”. |
| <b>conteúdo do canal de Alpha</b> *Booleano* | Preencha o canal alfa do mapa normal com a textura de entrada.   Preencher Alpha com entrada/forçar Alpha para 1: Isso permite que o canal de Alpha seja definido como sólido, em vez de usar a entrada como um Alpha adicional. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Tons de cinza* PRIMÁRIO | Imagem de entrada interpretada como um mapa de height. |

## Conectores de saída

|  |  |
| --- | --- |
| <b>Saída</b> *Cor* |  |

## Exemplos

*Em breve.*
