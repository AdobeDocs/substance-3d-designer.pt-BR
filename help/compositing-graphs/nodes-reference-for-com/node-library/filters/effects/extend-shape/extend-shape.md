---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/extend-shape.html"
breadcrumb-title: ''
description: Use o nó Extend Shape para estender as formas além dos limites para criar efeitos expandidos de máscara e padrão.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Extend Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extend Shape
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---


# Extend Shape

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](extend-shape.resources/extend-shape-01.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](extend-shape.resources/extend-shape-02.png){width="200px"}

</td>
</tr>
</table>

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O nó <b>Extend Shape</b> estende uma <i>seção</i> da <b>entrada</b> sobre uma direção e distância definidas.

O parâmetro <b>Mostrar auxiliar</b> permite visualizar a direção da seção estendida e da extensão.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Modo</b> <i>Inteiro</i> | Define os <i>parâmetros</i> usados para aplicar a extensão:<br><br>- <i>Bidirecional</i>: a seção da <b>Entrada</b> especificada pela <b>Posição de Extensão</b> e pelo <b>Ângulo de Extensão</b> é estendida sobre a <b>Distância de Extensão</b> em <i>direções opostas</i><br>- <i>Unidirecional</i>: a seção da <b>Entrada</b> especificada pela <b>Posição de Extensão</b> e O <b>Ângulo de extensão</b> é estendido ao longo da <b>Distância de extensão</b> em uma <i>única direção</i><br>- <i>Posições de início/fim</i>: um <i>vetor</i> de extensão é definido pela <b>Posição de início</b> e pela <b>Posição de fim</b>. A seção <i>perpendicular</i> da <b>Entrada</b> na <b>Posição inicial</b> é estendida <i>sobre este vetor</i> até a <b>Posição final</b> |
| <b>Distância de Extensão</b> <i>Flutuante</i> | A distância na qual a seção especificada pela <b>Posição da Extensão</b> e pelo <b>Ângulo de Extensão</b> deve ser estendida. A distância é expressa como uma <i>proporção</i> da extensão da imagem. |
| <b>Posição da Extensão</b> <i>Flutuante</i> | A posição na imagem da seção que deve ser estendida. O valor é expresso como um <i>deslocamento do centro</i>. |
| <b>Ângulo de Extensão</b> <i>Flutuante</i> | O ângulo da seção que deve ser estendida, considerando o ponto inicial, é uma <i>seção vertical</i>. |
| <b>Posição Inicial</b> <i>Flutuante2</i> | A posição inicial do <i>vetor de extensão</i>. |
| <b>Posição Final</b> <i>Flutuante2</i> | A posição final do <i>vetor de extensão</i>. |
| <b>Deslocamento da luminância de início</b> <i>Flutuante</i> | Aplica um deslocamento de luminância à área da imagem <i>anterior</i> à seção estendida. Este deslocamento de luminância é <i>interpolado ao longo da seção</i> para a luminância da área da imagem após a seção.<br><br><i>Observação</i>: este parâmetro está disponível somente na versão <b>Tons de Cinza</b> do nó. |
| <b>Deslocamento da luminância final</b> <i>Flutuante</i> | Aplica um deslocamento de luminância à área da imagem <i>após</i> a seção estendida. Este deslocamento de luminância é <i>interpolado ao longo da seção</i> para a luminância da área da imagem anterior à seção.<br><br><i>Observação</i>: este parâmetro está disponível somente na versão <b>Tons de Cinza</b> do nó. |
| <b>Ameixa. O Deslocamento Ignora Pixels Pretos</b> <i>Booleano</i> | Quando definido como <i>Verdadeiro</i>, os deslocamentos de luminância especificados em <i>ambos</i> O <b>Deslocamento da luminância de início</b> e o <b>Deslocamento da luminância de fim</b> são aplicados apenas a pixels <i>não pretos</i>, ou seja, pixels com valor superior a 0.<br><br><i>Observação</i>: este parâmetro só está disponível na versão <b>Tons de Cinza</b> do nó. |
| <b>Modo de Filtragem</b> <i>Inteiro</i> | Define como tratar os resultados de amostra ao <i>interpolar</i> entre pixels:<br><br>- <i>Mais próximo</i>: obterá uma amostra exatamente do <i>mesmo</i> valor (mais rápido)<br>- <i>Bilinear</i>: aplicará um filtro bilinear no resultado para uma aparência <i>mais suave</i> |
| <b>Mostrar auxiliar</b> <i>Booleano</i> | Visualize a <i>seção estendida</i> como uma sobreposição com setas que mostram a <i>direção</i> da extensão. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extend-shape-03.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extend-shape-04.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extend-shape-05.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extend-shape-06.png" />
        </td>
    </tr>
</table>
