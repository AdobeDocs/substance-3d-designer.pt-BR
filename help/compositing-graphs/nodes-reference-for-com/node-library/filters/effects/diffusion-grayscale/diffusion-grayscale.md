---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-grayscale.html"
breadcrumb-title: ''
description: Use o nó Tons de cinza de difusão para aplicar efeitos de difusão em tons de cinza para criar transições e mesclagens de cores suaves.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Escala de cinza de difusão
user-guide-description: ''
user-guide-title: ''
source-git-commit: 07f136ebd89fbe737b6c042f1275bd348b2be514
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 3%

---


# Escala de cinza de difusão

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](diffusion-grayscale.resources/diffusion-grayscale-icon.png){width="200px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Aplique um processo de difusão aos valores na entrada de imagem **Origem** de acordo com a entrada de imagem **Máscara** fornecida, criando gradações suaves entre os valores.

Somente os valores de pixels correspondentes à máscara são difundidos; outros pixels não participam do resultado.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Origem</b> <i>Tons de cinza</i> | A imagem a ser difundida. |
| <b>Máscara</b> <i>Tons de cinza</i> | Máscara de difusão: os pixels brancos são amostrados em <i>Origem</i> e difundidos em pixels pretos. A imagem deve ser preta e branca. Se a máscara incluir gradientes, o valor de corte será 0,5. |
| <b>Intensidade</b> <i>Tons de cinza</i> | Define localmente o grau de aplicação do processo de difusão. Este mapa deve ser <i>contrastado</i> para obter um efeito perceptível. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Iterações</b> <i>0.0 - 64.0</i> | O número de iterações de difusão a serem executadas (maior é melhor, mas mais lento). Os valores úteis estão no intervalo [8, 48].<br>Observe que, se você não estiver procurando correção matemática, os valores baixos serão ótimos ou até melhores. |
| <b>Distância</b> <i>0.0 - 1.0</i> | Ajusta a distância máxima da difusão. |
| <b>Habilitar Pontilhamento</b> <i>Verdadeiro/Falso</i> | Controla o método de amostragem de cada passagem. O pontilhamento permite a convergência em menos passagens, mas introduz ruído.<br>Sem ela, cada passagem é mais rápida, mas são necessárias mais passagens para obter um resultado suave sem artefatos de faixa. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-01-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-01a-after.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-01b-after.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-02-before.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-02-after.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-grayscale.resources/diffusion-grayscale-02-render.jpg" />
        </td>
    </tr>
</table>
