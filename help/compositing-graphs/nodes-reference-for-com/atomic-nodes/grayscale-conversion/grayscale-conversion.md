---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/grayscale-conversion.html"
breadcrumb-title: ''
description: Use o nó Conversão em escala cinza para converter texturas coloridas em tons de cinza usando vários métodos de conversão.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Grayscale conversion
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Conversão em tons de cinza
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8b6f65bd88f3c83bf6682c7bca91615166389a91
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 7%

---


# Conversão em tons de cinza

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: conversão em tons de cinza](grayscale-conversion.resources/comp_grayscaleconversion_1.png "Nó atômico: conversão em tons de cinza"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Converte uma imagem colorida em tons de cinza, ponderando a luminância de cada canal de cor.

Esse nó pode ser usado como um método otimizado para extrair um canal em tons de cinza de uma imagem colorida, definindo todos os valores de “Espessuras de canal” como 0, exceto o canal desejado, que deve ser definido como 1.

</td>
</tr>
</table>

A maioria dos nós pode ser definida para saída em tons de cinza ou coloridos, sendo que o primeiro é preferível por motivos de simplicidade e desempenho.

Na verdade, é recomendável trabalhar em tons de cinza desde o início e colorir as imagens mais tarde no fluxo de trabalho, usando, por exemplo, um nó [Mapa de gradiente](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md).

Isso significa que um nó de conversão de tons de cinza geralmente só é reservado para os casos em que especificamente se deseja converter uma imagem colorida em tons de cinza. Nesses casos, observe também a [Conversão de tons de cinza avançada](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/grayscale-conversion-adv/grayscale-conversion-advanced.md) e a [Cor para máscara](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-to-mask/color-to-mask.md).

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

## Parâmetros

</td>
<td style="border: 0;" valign="top">

### Conectores de entrada

</td>
<td style="border: 0;" valign="top">

### Conectores de saída

</td>
<td style="border: 0;" valign="top">

### Exemplos

</td>
</tr>
</table>

## Parâmetros

|  |  |
| --- | --- |
| <b>Espessuras de canal</b> *Precisão decimal 4* | Define o peso de cada um dos canais de RGBA na conversão de tons de cinza.   Por padrão, uma divisão uniforme é feita nos canais da RGB. |
| <b>Achatar alfa</b> *Booleano* | Define o comportamento do Alpha no resultado final da escala de cinza, pois os valores da escala de cinza não podem conter informações de Alpha.   Quando *Verdadeiro*, a conversão em tons de cinza é multiplicada no canal Alfa da imagem de entrada |
| <b>Valor do plano de fundo</b> *Precisão decimal* | Define o valor base do plano de fundo quando a entrada tem uma máscara alfa. Ou seja, determina quais pixels devem ser tratados como transparentes.   *Disponível quando &#39;Achatar alfa&#39; estiver definido como &#39;Verdadeiro&#39;.* |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Cor* PRIMÁRIA | A imagem colorida a ser processada. |

## Conectores de saída

|  |  |
| --- | --- |
| <b>Saída</b> *Tons de cinza* |  |

## Exemplos

*Em breve.*
