---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/distance.html"
breadcrumb-title: ''
description: Use o nó Distância para calcular mapas de distância a partir de formas para criar máscaras e efeitos de procedimento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Distance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Distância
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca8beeed4bcddc6518237761ba87c319a1624018
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 8%

---


# Distância

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: Distância](distance.resources/comp_distance_1.png "Nó atômico: Distância"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Localiza a posição do pixel branco mais próximo em uma máscara e gera um gradiente dessa posição, ou a cor nessa posição em uma imagem de origem.

Este nó cria um esmaecimento linear externo (gradiente) de quaisquer pixels no máximo de entrada acima do valor de tons de cinza de 0,5.

</td>
</tr>
</table>

O fade externo em expansão terminará assim que encontrar outra célula: eles nunca se sobreporão. Internamente, isto é realmente calcular e exibir a distância para o pixel mais próximo > 0,5, com o nó de distância definido como um grampo/máximo.

Um mapa de origem opcional permite combinar as células com a textura de um mapa de entrada secundário.

O nó de distância não é um nó fácil de dominar, mas seus principais casos de uso são expandir as máscaras existentes de forma confiável (em comparação com desfocar e ajustar o contraste), gerando células de ruído do tipo Voronoi, e chanfrando formas existentes com um perfil nítido e linear (que pode ser remapeado mais tarde.

Veja os [exemplos](#examples) abaixo para obter mais informações.

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
| <b>Modo de cores</b> *Booleano* | Alterna entre uma imagem em tons de cinza e uma imagem colorida de saída. Altera também o tipo de entrada &#39;Entrada de origem&#39;. |
| <b>Distância máxima</b> *Flutuante* | Ajusta a distância máxima para detecção da borda mais próxima na máscara, em pixels. |
| <b>Combinar origem/distância</b> *Booleano* | Determine como a “Entrada de origem” opcional é combinada com as células finais.<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Combinar:</i> combina o valor de &#39;Entrada de origem&#39; com a máscara linear de esmaecimento. Se a entrada &#39;Source input&#39; estiver conectada, seu valor será combinado com a distância calculada.</li> <li data-preserve-html="true"><i>Somente Origem:</i> resulta em cor sólida somente da &#39;Entrada de origem&#39;.</li> </ul> |
| <b>Modo de distância</b> *Inteiro* | Seleciona o método de cálculo da distância até a borda mais próxima na máscara extraída:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Euclidiano:</i> soma das diferenças X/Y quadradas.</li> <li data-preserve-html="true"><i>Manhattan:</i> Soma de valores absolutos de diferenças X/Y.</li> <li data-preserve-html="true"><i>Chebyshev:</i> O máximo de valores absolutos de diferenças X/Y.</li> </ul>  <div><img alt="Exemplos de modo de distância" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_copy_copy_copy_row-yj03rtt-column-0i13nfd_image" src="distance.resources/distance-comparison.jpg" title="Exemplos de modo de distância"/></div> |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada de máscara</b> *Tons de cinza* PRIMÁRIO | Uma máscara em tons de cinza, cujas bordas devem ter um valor de distância calculado.   Uma máscara binária é extraída da imagem, usando um valor de limite de 0,5, em que todos os valores acima desse limite são brancos e todos os valores abaixo são pretos. |
| <b>Entrada de origem</b> *Cores/Tons de Cinza* | Imagem opcional em tons de cinza da qual o valor de pixel na borda mais próxima da “Entrada da máscara” deve ser copiado. |

## Conectores de saída

|  |  |
| --- | --- |
| <b>Saída</b> *Cores/Tons de Cinza* |  |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](distance.resources/distance-ex01.gif){width="250px"}

</td>
<td style="border: 0;" valign="top">

![](distance.resources/distance-ex02.gif){width="250px"}

</td>
<td style="border: 0;" valign="top">

![](distance.resources/distance-ex03.gif){width="250px"}

</td>
</tr>
</table>
