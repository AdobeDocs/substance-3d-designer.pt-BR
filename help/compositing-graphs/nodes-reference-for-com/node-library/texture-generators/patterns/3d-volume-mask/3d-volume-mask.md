---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-volume-mask.html"
breadcrumb-title: ''
description: Use o nó Máscara de volume 3D para criar máscaras volumétricas com base na posição 3D para efeitos de material avançados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Volume Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Máscara de volume 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---


# Máscara de volume 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-volume-mask.resources/3dvolumemask.png){width="256px"}

<b>Entrada:</b> Gerador > Padrão

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O nó **Máscara de Volume 3D** gera uma representação de uma *forma primitiva* com base no mapa de entrada **Posição**.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Posição</b> <i>Cor</i> | O mapa que descreve as *coordenadas de espaço 3D* nas quais a primitiva é representada.<br><br>As coordenadas **X/Y/Z** são mapeadas para os canais **R/G/B**, respectivamente. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Forma</b> <i>Inteiro</i> | A forma primitiva que deve ser representada:<br><br>- *Cubo*<br>- *Cilindro*<br>- *Esfera* |
| <b>Escala</b> <i>Flutuante</i> | Define a escala *global* da primitiva, aplicada *uniformemente* em todos os eixos. |
| <b>Tamanho</b> <i>Flutuante3</i> | Define o tamanho da forma em cada eixo. |
| <b>Entrada de Posição</b> <i>Inteiro</i> | O método de *representar o espaço* por meio da entrada **Posição**:<br><br>- *Posição UV*: use um *mapa UV*. As coordenadas X/Y (U/V) são mapeadas para os canais R/G, respectivamente. Presume-se que o eixo Z seja o vetor *ortogonal à frente*.<br>- *Posição do espaço mundial*: use um *mapa de posição* para mapear a primitiva no espaço 3D. As coordenadas X/Y/Z são mapeadas para os canais R/G/B, respectivamente. |
| <b>Posição UV</b> <i>Flutuante2</i> | A posição da primitiva no espaço UV.<br><br>*Observação*: este parâmetro só está disponível quando o parâmetro **Entrada de posição** está definido como *Posição UV*. |
| <b>Posição</b> <i>Flutuante3</i> | A posição da primitiva no espaço global.<br><br>*Observação*: este parâmetro só está disponível quando o parâmetro **Entrada de Posição** está definido como *Posição no Espaço Mundial*. |
| <b>Rotação</b> <i>Flutuante3</i> | Define a rotação da forma no espaço global. |
| <b>Largura da Difusão</b> <i>Flutuante</i> | Ajusta a largura do *gradiente de atenuação* da superfície primitiva para dentro. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant4.jpg" />
        </td>
    </tr>
</table>
