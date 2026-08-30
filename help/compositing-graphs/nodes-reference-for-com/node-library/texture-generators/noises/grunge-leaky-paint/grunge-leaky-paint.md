---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/grunge-leaky-paint.html"
breadcrumb-title: ''
description: Use o nó Pintura de Desgaste vazada para gerar padrões de vazamento de tinta para criar efeitos de superfície envelhecidos e envelhecidos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Grunge Leaky Paint
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desgaste Leaky Paint
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Desgaste Leaky Paint

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](grunge-leaky-paint.resources/grungeleakypaint.jpg){width="200px"}

<b>Entrada:</b> geradores de textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O nó **Pintura de Desgaste Vazado** gera um mapa de desgaste semelhante ao gotejamento de tinta através de vazamentos.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Saldo</b> <i>Flutuante</i> | Ajusta o equilíbrio entre valores escuros e brilhantes. |
| <b>Contraste</b> <i>Flutuante</i> | Ajusta o contraste da imagem. |
| <b>Inverter</b> <i>Booleano</i> | Inverte a saída da imagem, usando uma operação `1-x`. |
| <b>Expansão não quadrada</b> <i>Booleano</i> | Permite a compensação de esmagamento e alongamento com proporções não quadradas. |
| <b>Avançado</b> |  |
| <b>Intensidade de Vazamento</b> <i>Flutuante</i> | Ajusta a densidade e a intensidade dos pingos. |
| <b>Escala de vazamento</b> <i>Inteiro</i> | Ajusta a escala da separação de gotas. |
| <b>Ângulo de Vazamento Aleatório</b> <i>Flutuante</i> | Ajusta o *ângulo máximo* de gotas que podem ser girados aleatoriamente, em *número de voltas*. |
| <b>Vazamento de crocância</b> <i>Flutuante</i> | Ajusta a nitidez e a nitidez dos pingos. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="grunge-leaky-paint.resources/grungeleakypaint-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="grunge-leaky-paint.resources/grungeleakypaint-variant2.jpg" />
        </td>
    </tr>
</table>
