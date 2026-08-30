---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/shape-light.html"
breadcrumb-title: ''
description: Use o nó Luz de forma para adicionar fontes de luz com formato personalizado a ambientes HDRI para efeitos criativos de iluminação.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Shape Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luz da forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 5%

---


# Luz da forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-light.resources/panorama-shape.png){width="200px"}

<b>Entrada:</b> Visualização 3D > Ferramenta HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma forma retangular projetada esfericamente. A transformação da forma é orientada por um cursor de transformação.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada de imagem de fundo</b> <i>Entrada de cores</i> | Fundo opcional no qual compor a luz gerada. |
| <b>Entrada de Imagem de Forma</b> <i>Entrada de cores</i> | Imagem opcional para mapear para a luz da esfera. Usado somente quando o Modo de cor da forma está definido como Entrada de imagem. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Matriz de Formas</b> |  |
| <b>Matriz</b> <i>(Matriz de Transformação)</i> | Controle de transformação do resultado. O resultado pode ser modificado interagindo diretamente com a tela. |
| <b>Deslocamento</b> <i>-2.0 - 2.0</i> | Move ou traduz o resultado. O resultado pode ser modificado interagindo diretamente com a tela. |
| <b>Forma</b> <i>Retângulo, Disco</i> | Escolha a forma a ser inserida. |
| <b>Modo de Cores da Forma</b> <i>RGB, Temperatura (Kelvin), Entrada De Imagem</i> | Escolha o método a ser usado para definir a cor da forma. A Entrada de imagem permite o uso do segundo slot de entrada. |
| <b>Cor</b> <i>(Valor da cor)</i> | Somente com o Modo de cor da forma definido como RGB. Escolhe a cor da forma. |
| <b>Temperatura da forma</b> <i>800.0 - 20000.0</i> | Somente com o Modo de cor da forma definido como Temperatura. Define o valor de Kelvin para a cor da forma. |
| <b>Gama de Entrada da Imagem da Forma</b> <i>sRGB, Linear</i> | Somente com o Modo de cor da forma definido como Entrada de imagem. Determine como interpretar a entrada de imagem de forma. |
| <b>Exposição De Forma (EV)</b> <i>0.0 - 10.0</i> | Defina o valor de exposição para a forma gerada, de forma ideal para o valor de exposição da imagem de plano de fundo. |
| <b>Dureza da forma</b> <i>0.0 - 1.0</i> | Definir dureza das bordas da forma. |
| <b>Exposição a Ponto de Acesso (EV)</b> <i>0.0 - 10.0</i> | Definir a exposição do ponto ativo central. Observe que isso não é muito visível no modo RGB. |
| <b>Tamanho do Ponto de Acesso</b> <i>0.0 - 1.0</i> | Tamanho do Ponto de Acesso central. |
| <b>Queda do Ponto de Acesso</b> <i>0.0 - 1.0</i> | Queda do ponto de acesso central. |
| <b>Posição do Ponto de Acesso</b> <i>0.0 - 1.0</i> | Posição X e Y do ponto de acesso central. |
| <b>Habilitar Entrada em Segundo Plano</b> <i>Falso/Verdadeiro</i> | Alterna o uso da imagem de fundo opcional. Os compostos geraram luz na parte superior do plano de fundo. |
| <b>Cor do plano de fundo</b> <i>(Valor da cor)</i> | Se a Entrada do plano de fundo não for usada, defina um valor de plano de fundo de cor sólida aqui. |
| <b>Gama de Plano de Fundo</b> <i>sRGB, Linear</i> | Se a Entrada em segundo plano for usada, defina como interpretar a entrada em segundo plano. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-light.resources/shape-light-ex.gif" />
        </td>
    </tr>
</table>
