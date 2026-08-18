---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/channel-shuffle.html"
breadcrumb-title: ''
description: Use o nó Embaralhamento de canais para reorganizar os canais de cores em texturas para criar efeitos de cores e troca de canal.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Channels shuffle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Embaralhamento de canais
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 7%

---


# Embaralhamento de canais

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: embaralhamento de canais](../../../../assets/comp_shuffle.png "Nó atômico: embaralhamento de canais"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Reorganiza os canais de cor de uma ou duas imagens de entrada na imagem de saída.

Por exemplo, o recebe duas entradas e permite retornar uma saída na qual qualquer um dos canais vermelho, verde, azul e Alpha são trocados ou definidos para qualquer um dos canais de entrada.

Essencialmente, ele permite empacotar e trocar canais de RGB de qualquer maneira possível. As entradas em tons de cinza são tratadas como se fossem Cores: Vermelho, Verde, Azul e Alpha retornam todos os mesmos valores.

</td>
</tr>
</table>

O Embaralhamento de canal tem opções básicas, mas na maioria dos casos de embalagem de canal ou Retirada e configuração de canais de Alpha é mais rápido usar a [Mesclagem de RGBA](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md), a [Divisão de RGBA](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-split/rgba-split.md), a [Mesclagem de Alpha](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-merge/alpha-merge.md) e a [Divisão de Alpha](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-split/alpha-split.md). Eles são configurados para executar ações padrão que não exigem a alteração de vários parâmetros e a conversão para tons de cinza posteriormente. Se você está procurando uma versão mais avançada com mais opções de mesclagem, confira o [Misturador de Canais](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/channel-mixer/channel-mixer.md).

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
| <b>Canal vermelho</b> *Inteiro* | Escolha o canal de origem a ser inserido no canal Vermelho da imagem de saída. |
| <b>Canal verde</b> *Inteiro* | Escolha o canal de origem a ser inserido no canal Verde da imagem de saída. |
| <b>Canal azul</b> *Inteiro* | Escolha o canal de origem a ser inserido no canal Azul da imagem de saída. |
| <b>canal de Alpha</b> *Inteiro* | Escolha o canal de origem a ser inserido no canal de Alpha da imagem de saída. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada 1</b> *Cores/Tons de Cinza* PRIMÁRIO | Imagem de entrada primária. |
| <b>Entrada 2</b> *Cores/Tons de Cinza* | Imagem de entrada secundária. |

## Conectores de saída

|  |  |
| --- | --- |
| <b>Saída</b> *Tons de cinza/Cor* |  |

## Exemplos

*Em breve.*
