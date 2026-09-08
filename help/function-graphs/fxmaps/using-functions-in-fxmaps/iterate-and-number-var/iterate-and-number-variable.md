---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-variable.html"
breadcrumb-title: ''
description: Saiba como usar variáveis iterate e number em FXMaps para criar padrões de loop e variações de procedimento.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Iterate and number variable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Iterar e variável de número
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# Iterar e variável $number

![](../../../../assets/iterate-1.jpg)

O nó Iterar renderizará os nós conectados à saída direita durante o tempo especificado pelo valor de Iterações.

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../assets/1-iteration.png"/></div> | 1 iteração: o padrão gaussiano é renderizado uma vez |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="../../../../assets/10-iterations.png"/></div> | 10 iterações: o padrão gaussiano é renderizado 10 vezes no mesmo local |

Ao usar um nó Iterar, você pode usar a variável $number para obter o valor de iteração atual. $number é um valor float e começa em 0.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../assets/position-function.jpg){width="300px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../assets/10-iterations-position-function.png){width="300px"}

</td>
</tr>
</table>

Esta função, definida no parâmetro Deslocamento de padrão, será executada 10 vezes, uma para cada padrão.

O primeiro padrão tem um valor $number igual a 0 e é então renderizado na coordenada (0, 0). O segundo padrão tem um valor $number igual a 1 e é então renderizado na coordenada (0.1, 0) (1 x 0.1 = 0.1) e assim por diante para os próximos padrões.

Baixar exemplo: [iterate\_node.sbs](https://helpx.adobe.com/content/dam/help/en/substance-3d/documentation/sddoc/files/102400023/102367299/1/1423458106000/iterate-node.sbs)
