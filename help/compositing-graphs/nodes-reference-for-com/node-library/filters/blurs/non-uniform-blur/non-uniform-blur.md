---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/non-uniform-blur.html"
breadcrumb-title: ''
description: Use o nó Desfoque não uniforme para aplicar desfoque com intensidades diferentes nas direções X e Y para efeitos anisotrópicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Non Uniform Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desfoque não uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 9%

---


# Desfoque não uniforme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-blur-grayscale.png){width="128px"}

![](../../../../../../assets/non-uniform-blur.png){width="128px"}

<b>Entrada:</b> Filtros > Desfoques

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Executa um Desfoque de alta qualidade, onde a intensidade é orientada por uma máscara de entrada. As opções permitem adicionar Anisotropia e assimetria.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Mapa de desfoque</b> <i>Entrada em tons de cinza</i> | Mapa de máscaras para determinar a intensidade do efeito. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Intensidade</b> <i>0.0 - 50.0</i> | Intensidade máxima para aplicar o desfoque. Mascarada pelo Mapa de desfoque, portanto, essa configuração não terá efeito sobre as áreas pretas desse mapa. |
| <b>Anisotropia</b> <i>0.0 - 1.0</i> | Opcionalmente, adiciona direcionalidade ao efeito de desfoque. Direcionado pelo parâmetro Ângulo. |
| <b>Assimetria</b> <i>0.0 - 1.0</i> | Opcionalmente, adiciona um viés à amostragem. Direcionado pelo parâmetro Ângulo. |
| <b>Ângulo</b> <i>0.0 - 1.0</i> | Ângulo para definir a direcionalidade e o viés de amostragem. |
| <b>Amostras</b> <i>1 - 16</i> | Quantidade de amostras, determina a qualidade. Multiplicado pela quantidade de lâminas. |
| <b>Pás</b> <i>1 - 9</i> | Quantidade de setores de amostragem, determina a qualidade. Multiplicado pela quantidade de amostras. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/nonuniform-example.gif" /><br><i>O exemplo abaixo é orientado por uma rampa de gradiente (a 90 graus) no slot do Mapa de Desfoque.</i>
        </td>
    </tr>
</table>
