---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-uniform-rotation.html"
breadcrumb-title: ''
description: Use o nó Rotação não uniforme para aplicar transformações de rotação não uniformes para criar efeitos de espiral e vórtice.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Uniform Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rotação não uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---


# Rotação não uniforme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](non-uniform-rotation.resources/nonuniformrotationgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](non-uniform-rotation.resources/nonuniformrotationcolor.png){width="200px"}

</td>
</tr>
</table>

<b>Entrada:</b> Filtros > Transformas

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O nó **Rotação Não Uniforme** gira a **Entrada** usando a entrada **Mapa de rotação**.

Os valores da imagem representam um *número de rotações*. A rotação é executada em torno da posição especificada pelo valor de **Posição de pivô** ou pela entrada de **mapa de Posição de pivô**.\
Valores positivos na entrada **Mapa de rotação** resultam em uma rotação *horária*.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada</b> <i>Tons de cinza/Cor</i> | A imagem em tons de cinza de entrada que deve ser girada. |
| <b>Mapa de rotação</b> <i>Tons de cinza</i> | O mapa usado para controlar a quantidade de rotação, em *número de rotações*. Os valores amostrados são multiplicados pelo **Multiplicador do ângulo de rotação**. Valores negativos resultam em uma rotação *no sentido anti-horário*. |
| <b>Mapa de Posição de pivô de Rotação</b> <i>Cor</i> | A imagem usada para especificar a posição da rotação *dinâmica*. A posição **X/Y** está mapeada para os canais **R/G** da imagem. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Multiplicador de Ângulo de Rotação</b> <i>Flutuante</i> | Ajusta a intensidade da entrada de **Mapa de rotação**. |
| <b>Deslocamento do Ângulo de Rotação</b> <i>Flutuante</i> | Aplica a quantidade adicional especificada de rotação. |
| <b>Usar o Mapa de Posição de pivô</b> <i>Booleano</i> | Use uma *entrada de bitmap* para especificar a posição da tabela dinâmica de rotação. A posição **X/Y** está mapeada para os canais **R/G** da entrada **Mapa de Posições**. |
| <b>Posição de pivô</b> <i>Precisão decimal 2</i> | A posição da tabela dinâmica em torno da qual a imagem é girada. |
| <b>Cor do plano de fundo</b> <i>Precisão decimal/Precisão decimal 4</i> | Cor do plano de fundo para exibir *fora* dos limites da imagem caso a divisão em blocos gráficos não esteja definida como **Divisão em blocos gráficos em H e V**. |
| <b>Modo de filtragem</b> <i>Inteiro</i> | Define como tratar os resultados de amostra ao *interpolar* entre pixels:<br><br>- *Mais próximo*: obterá uma amostra exatamente do *mesmo* valor (mais rápido)<br>- *Bilinear*: aplicará um filtro bilinear no resultado para uma aparência *mais suave* |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="non-uniform-rotation.resources/nonuniformrotation-demo-02-resized.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="non-uniform-rotation.resources/nonuniformrotation-variant-png.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="non-uniform-rotation.resources/nonuniformrotation-node.png" />
        </td>
    </tr>
</table>
