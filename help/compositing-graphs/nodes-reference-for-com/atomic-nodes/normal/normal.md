---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/normal.html"
breadcrumb-title: ""
description: Use o nó Normal para processar e manipular texturas de mapa normal para controlar os detalhes da superfície e a iluminação.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Normal
user-guide-description: ""
user-guide-title: ""
source-git-commit: 961ee151245fbc3266574676bd535c374bd0e3ad
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 7%
---

# Normal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: Normal](normal.resources/comp_normal_1.png "Nó atômico: Normal"){width="100%"}

</td>
<td style="border: 0;" valign="top">

Calcula um mapa normal a partir de uma imagem em tons de cinza interpretada como um mapa de altura.

O nó converte um mapa de entrada em tons de cinza em uma saída de Mapa normal de espaço tangente. Ele tem algumas opções de usuário para definir a intensidade e a codificação.

</td>
</tr>
</table>

<div data-preserve-html="true" align="center"><img src="normal.resources/normal-tooltip.gif" alt="dica de ferramenta normal" /></div>

É um nó muito útil que é usado com frequência para converter entradas de mapa de altura em mapas normais para materiais prontos em tempo real. Existem alternativas a serem encontradas no [Normal Sobel](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-sobel/normal-sobel.md) e no Height para Unidades Mundiais Normais.



## Parâmetros

|  |  |
| --- | --- |
| <b>Intensidade</b> *Precisão decimal* | Modifica a intensidade do mapa de altura.   Define a intensidade com que o mapa de altura de entrada é interpretado para conversão em normais. Dependendo dos mapas de entrada, valores acima de 100 têm pouco mais efeito. |
| <b>Formato normal</b> *Booleano* | Inverte as coordenadas Y do mapa de altura (OpenGL).   Define como o canal Verde (Y) é codificado. Basicamente, um interruptor “Flip Green/Y”. |
| <b>Conteúdo do canal alfa</b> *Booleano* | Preencha o canal alfa da mapa normal com a textura de entrada.   Preencher Alpha com entrada/forçar Alpha para 1: permite que o canal alfa seja definido como sólido, em vez de usar a entrada como um Alpha adicional. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Tons de cinza* PRIMÁRIO | Imagem de entrada interpretada como um mapa de altura. |


## Exemplos

*Em breve.*
