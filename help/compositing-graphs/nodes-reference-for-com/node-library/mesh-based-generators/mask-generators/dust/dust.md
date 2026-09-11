---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dust.html"
breadcrumb-title: ''
description: Use o nó Dust para gerar máscaras de acumulação de dust com base na geometria da malha para criar efeitos realistas de dust e sujeira.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dust
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 5%

---


# Dust

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dust.resources/dust.png){width="128px"}

<b>Entrada:</b> Geradores > Geradores de máscara Baseados em Malha

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara representa o dust acumulado em áreas ocultas, rebaixadas, bem como apenas em áreas voltadas para cima. Requer AO cozido e World Space Normals adequados para funcionar.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Oclusão de ambiente</b> <i>Entrada em tons de cinza</i> | Mapa baked usado para o posicionamento do dust. Obrigatório! |
| <b>Espaço Mundial Normal</b> <i>Entrada de cores</i> | Mapa baked usado para o posicionamento do dust. Obrigatório! |
| <b>Ruído</b> <i>Entrada em tons de cinza</i> | O mapa de dusts personalizado (opcional) só aparece quando Substituir ruído está definido como Verdadeiro. |
| <b>Máscara (opcional)</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Nível</b> <i>0.0 - 1.0</i> | Define a quantidade total de dust. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta o contraste da dust. |
| <b>Valor da Oclusão</b> <i>0.0 - 1.0</i> | Define a influência do AO; mais dust aparecerá em áreas ocultadas. |
| <b>Opacidade do ruído</b> <i>0.0 - 1.0</i> | Define a quantidade de ruído visível nas áreas empoeiradas. |
| <b>Substituir Ruído</b> <i>Falso/Verdadeiro</i> | Defina para usar a entrada personalizada do mapa de dusts. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dust.resources/dust-ex.gif" />
        </td>
    </tr>
</table>
