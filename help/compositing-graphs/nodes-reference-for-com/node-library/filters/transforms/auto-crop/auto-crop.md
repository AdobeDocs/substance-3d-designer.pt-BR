---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/auto-crop.html"
breadcrumb-title: ''
description: Use o nó Corte automático para cortar automaticamente texturas para remover bordas vazias e otimizar as dimensões da textura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Auto Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Corte automático
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---


# Corte automático

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](auto-crop.resources/autocropgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](auto-crop.resources/autocropcolor.png){width="200px"}

</td>
</tr>
</table>

<b>Entrada:</b> Filtros > Transformas

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O nó **Corte automático** ajusta a **Entrada** de modo que o conteúdo seja colocado no *centro* da imagem sem ser redimensionado ou *redimensionado para a extensão* da imagem.

O conteúdo da imagem é definido por uma caixa ajustada ao *primeiro e último pixels* em **X** e **Y**, cujos valores são *superiores a 0* (ou seja, não são pretos). A versão **Cor** permite escolher entre os canais RGB e Alfa para definir essa caixa.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Modo</b> <i>Inteiro</i> | Defina o método de corte que deve ser aplicado:<br><br>- <i>Quadrado de corte</i>: a imagem é cortada para que a forma fique no centro da menor imagem <i>quadrada</i> que pode incluí-la totalmente<br>- <i>Automático de corte</i>: a imagem é cortada para que a forma fique no centro da menor imagem <i>quadrada ou não quadrada</i> que pode incluí-la totalmente<br>- <i>Ajustar (Manter proporção)</i>: a imagem é redimensionada para a <i>cheia extensão</i> da imagem mantendo suas <i>proporções</i> (por exemplo, proporção entre largura e comprimento)<br>- <i>Preenchimento (Esticamento)</i>: a imagem é redimensionada para a <i>extensão completa</i> da imagem |
| <b>Usar alfa</b> <i>Booleano</i> | Use o canal alfa da <b>Entrada</b> para determinar os <i>limites</i> do conteúdo da imagem para corte. Quando definido como <i>Falso</i>, os pixels pretos são usados.<br><br><i>Observação:</i> esse parâmetro só está disponível na versão <b>Cor</b> do nó. |
| <b>Modo de Filtragem</b> <i>Inteiro</i> | Define como tratar os resultados de amostra ao <i>interpolar</i> entre pixels:<br><br>- <i>Mais próximo</i>: obterá uma amostra exatamente do <i>mesmo</i> valor (mais rápido)<br>- <i>Bilinear</i>: aplicará um filtro bilinear no resultado para uma aparência <i>mais suave</i><br>- <i>Automático</i>: usa o mais apropriado dos dois modos acima, dependendo do <b>Modo</b> selecionado para corte |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-demo-01-resized.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant4.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-variant3.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="auto-crop.resources/autocrop-node.png" />
        </td>
    </tr>
</table>
