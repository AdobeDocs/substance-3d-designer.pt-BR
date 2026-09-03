---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/surface-brush.html"
breadcrumb-title: ''
description: Use o nó Pincel de superfície para gerar máscaras com base na orientação da superfície para criar efeitos de intemperismo e desgaste direcionais.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Surface Brush
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pincel de superfície
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 7%

---


# Pincel de superfície

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](surface-brush.resources/surface-brush-01.png){width="128px"}

<b>Entrada:</b> Geradores > Geradores de máscara Baseados em Malha

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma máscara em preto e branco com base em mapas baked e configurações do usuário. Semelhante às [Máscaras Inteligentes](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks) do [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter).

Essa máscara representa um efeito interessante do pincel de metal em uma superfície de objeto, ocultado pela geometria de objetos e pelo AO.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Espaço Mundial Normal</b> <i>Entrada de cores</i> |  |
| <b>Curvatura</b> <i>Entrada em tons de cinza</i> | Mapa baked usado para efeitos internos e mascaramento. |
| <b>Oclusão de ambiente</b> <i>Entrada em tons de cinza</i> | Mapa baked usado para efeitos internos e mascaramento. |
| <b>Posição</b> <i>Entrada em tons de cinza</i> |  |
| <b>Máscara (opcional)</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Nível</b> <i>0.0 - 1.0</i> | Define o nível de efeito global, revelando gradualmente. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta o contraste do resultado. |
| <b>Scratches Comprimento</b> <i>0.0 - 8.0</i> | Define o comprimento dos arranhões. Valores menores são mais como pontos, valores maiores são listras longas. |
| <b>Ocultar Eixo</b> <i>X, Y, Z, nenhum</i> | Eixo do objeto que deve receber arranhões. Não altera a direção dos arranhões. |
| <b>Ocultar Intensidade do Eixo</b> <i>0.0 - 1.0</i> | Intensidade do efeito de oclusão do eixo. |
| <b>Oclusão</b> <i>0.0 - 1.0</i> | Força do AO ao ocultar arranhões. |
| <b>Intensidade de nitidez</b> <i>0.0 - 1.0</i> | Defina a quantidade de pós-nitidez a ser aplicada aos arranhões. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="surface-brush.resources/surface-brush-02.gif" />
        </td>
    </tr>
</table>
