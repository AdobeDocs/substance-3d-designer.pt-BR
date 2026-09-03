---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-color.html"
breadcrumb-title: ''
description: Use o nó Cor de difusão para aplicar efeitos de difusão de cores para criar transições e misturas de cores suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cor de difusão
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 4%

---


# Cor de difusão

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](diffusion-color.resources/diffusion-color-01.png){width="200px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Aplique um processo de difusão às cores na entrada de imagem de **Origem** de acordo com a entrada de imagem da **Máscara** fornecida, criando gradações suaves entre as cores ao usar o [Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html).

Somente as cores de pixels correspondentes à máscara são difusas; outros pixels não participam do resultado.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Origem</b> <i>Cor</i> | A imagem a ser difundida. |
| <b>Máscara</b> <i>Tons de cinza</i> | Máscara de difusão: os pixels brancos são amostrados em <i>Origem</i> e difundidos em pixels pretos. A imagem deve ser preta e branca. Se a máscara incluir gradientes, o valor de corte será 0,5. |
| <b>Intensidade</b> <i>Tons de cinza</i> | Define localmente o grau de aplicação do processo de difusão. Este mapa deve ser <i>contrastado</i> para obter um efeito perceptível. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Iterações</b> <i>0.0 - 64.0</i> | O número de iterações de difusão a serem executadas (maior é melhor, mas mais lento). Os valores úteis estão no intervalo [8, 48].<br>Observe que, se você não estiver procurando correção matemática, os valores baixos serão ótimos ou até melhores. |
| <b>Distância</b> <i>0.0 - 1.0</i> | Ajusta a distância máxima da difusão. |
| <b>Habilitar Pontilhamento</b> <i>Verdadeiro/Falso</i> | Controla o método de amostragem de cada passagem. O pontilhamento permite a convergência em menos passagens, mas introduz ruído.<br>Sem ela, cada passagem é mais rápida, mas são necessárias mais passagens para obter um resultado suave sem artefatos de faixa. |
| <b>É Mapa normal</b> <i>Verdadeiro/Falso</i> | Adiciona uma normalização em valores em cada etapa. |
| <b>Usar Alpha como Máscara</b> <i>Verdadeiro/Falso</i> | Use o canal alfa da entrada <i>Origem</i> como máscara de difusão, em vez da entrada <i>Máscara</i>. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-04.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-05.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-06.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-07.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-08.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-color.resources/diffusion-color-09.jpg" />
        </td>
    </tr>
</table>
