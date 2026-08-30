---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-uv.html"
breadcrumb-title: ''
description: Use o nó Difusão UV para aplicar efeitos de difusão no espaço UV para criar transições e mesclagens de cores suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion UV
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Difusão UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 2%

---


# Difusão UV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](diffusion-uv.resources/diffusion-uv-icon.png){width="200px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Aplique um processo de difusão às coordenadas UV na entrada de imagem **Origem** de acordo com a entrada de imagem **Máscara** fornecida, interpolando coordenadas entre valores da **Origem**.

Apenas UVs de pixels correspondentes à máscara são difundidos; outros pixels não participam do resultado.

Observe que a divisão em blocos gráficos é tratada de uma maneira especial: quando a divisão em blocos gráficos está *habilitada* (o que é o caso por padrão), as coordenadas vizinhas podem ser calculadas em média através do limite de 0/1.

Por exemplo, se o valor da coordenada U for 0,1 em um pixel e 0,8 em outro, o valor médio será 0,95 em vez de 0,45, porque *a divisão lado a lado das coordenadas é assumida*. Isso é independente da posição real do pixel: os valores de coordenadas são tratados da mesma maneira em toda a imagem.

Isso pode levar a resultados indesejados ao usar este filtro para *deformação de textura*. Se isso acontecer, certifique-se de que sua máscara defina “controlar curvas/pontos” com não mais de *metade de um comprimento de textura de um ponto a outro*.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Origem</b> <i>Cor</i> | Os UVs se difundem. Observe que a divisão em blocos gráficos é tratada de maneira especial neste filtro (consulte <i>Descrição</i>). |
| <b>Máscara</b> <i>Tons de cinza</i> | A máscara de difusão: os pixels brancos são amostrados em <i>Origem</i> e difundidos em pixels pretos. A imagem deve ser preta e branca. Se a máscara incluir gradientes, o valor de corte será 0,5. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Iterações</b> <i>0.0 - 64.0</i> | O número de iterações de difusão a serem executadas (maior é melhor, mas mais lento). Os valores úteis estão no intervalo [8, 48].<br>Observe que, se você não estiver procurando correção matemática, os valores baixos serão ótimos ou até melhores. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-01a-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-01a-after.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-01b-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-01b-after.jpg" />
        </td>
    </tr>
</table>
