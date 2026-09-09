---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/sphere-light.html"
breadcrumb-title: ''
description: Use o nó Luz da esfera para adicionar fontes de luz esféricas a ambientes HDRI para um controle de iluminação aprimorado.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Sphere Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luz da esfera
user-guide-description: ''
user-guide-title: ''
source-git-commit: 49bf753c2fa3d673b519b3ed87cc8bc82616bee6
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 4%

---


# Luz da esfera

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](sphere-light.resources/panorama-sphere-light.png){width="200px"}

<b>Entrada:</b> Visualização 3D > Ferramenta HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma forma de esfera projetada esfericamente. A transformação da esfera é impulsionada por um gizmo de transformação.

A luz da esfera é bastante versátil e tem opções que lhe permitem não só gerar luzes redondas simples, mas também planetas ou outros corpos celestes. Se você não precisa de opções mais avançadas de iluminação e rotação, dê uma olhada na [Luz de Forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md).

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
| <b>Modo de Posição</b> <i>Distância da origem, Posição Mundial</i> | Escolha entre dois modos de posicionamento. A distância da origem é semelhante às coordenadas polares, a esfera é definida em relação ao centro do panorama, a posição do mundo funciona como coordenadas 3D padrão. |
| <b>Coordenadas de Posição</b> |  |
| <b>Vetor para cima</b> <i>Z Para Cima, Y Para Cima</i> | Somente com o modo Posição mundial, determine a orientação do sistema de coordenadas. |
| <b>Posição Mundial da Esfera</b> <i>-2.0 - 2.0</i> | Somente com o modo Posição mundial define a posição da esfera no espaço global. |
| <b>Posição</b> | Somente com o modo de Distância da origem. Define a posição em relação ao centro. Pode ser manipulado no Visualização 2D. |
| <b>Distância da origem</b> <i>0.0 - 20.0</i> | Somente com o modo de Distância da origem. Define a distância para a origem, afeta o tamanho visível da esfera. |
| <b>Modo de Cores da Forma</b> <i>RGB, Temperatura (Kelvin), Entrada De Imagem</i> | Escolha o método a ser usado para definir a cor da forma. A Entrada de imagem permite o uso do segundo slot de entrada. |
| <b>Cor</b> <i>(Valor da cor)</i> | Somente com o Modo de cor da forma definido como RGB. Escolhe a cor da forma. |
| <b>Temperatura da forma</b> <i>800.0 - 20000.0</i> | Somente com o Modo de cor da forma definido como Temperatura. Define o valor de Kelvin para a cor da forma. |
| <b>Gama de Entrada de Imagem da Esfera</b> <i>sRGB, Linear</i> | Somente com o Modo de cor da forma definido como Entrada de imagem. Determine como interpretar a entrada de imagem de forma. |
| <b>Rotação de esfera</b> <i>0.0 - 1.0</i> | Somente com o Modo de cor da forma definido como Entrada de imagem. Gira a esfera ao redor de seu centro para orientar a imagem mapeada. |
| <b>Exposição (EV)</b> <i>0.0 - 10.0</i> | Defina o valor de exposição para a forma gerada, de forma ideal para o valor de exposição da imagem de plano de fundo. |
| <b>Raio da esfera</b> <i>0.0 - 1.0</i> | Define o raio/tamanho da esfera. |
| <b>Dureza da esfera</b> <i>0.0 - 1.0</i> | Define a dureza/declínio da esfera. |
| <b>Sombreamento</b> <i>Nenhum, Escurecimento de Membros, Luz de Sombreamento</i> | Defina se algum sombreamento deve ser aplicado à esfera. Permite que a esfera não apareça como um objeto sólido e sem iluminação. Escurecimento do membro significa um leve escurecimento que aparece nas bordas. Luz do Sombreamento significa que a esfera é iluminada por uma Luz do Sombreamento opcional. |
| <b>Posição Mundial da Luz do Sombreamento</b> <i>-1.0 - 1.0</i> | Se o Sombreamento estiver definido como Luz do Sombreamento, a posição da luz na esfera é controlada aqui. |
| <b>Transparência Penombra</b> <i>0.0 - 1.0</i> | Se Sombreamento estiver definido como Luz do Sombreamento, controla a queda do sombreamento. |
| <b>Habilitar Entrada em Segundo Plano</b> <i>Falso/Verdadeiro</i> | Alterna o uso da imagem de fundo opcional. Os compostos geraram luz na parte superior do plano de fundo. |
| <b>Cor do plano de fundo</b> <i>(Valor da cor)</i> | Se a Entrada do plano de fundo não for usada, defina um valor de plano de fundo de cor sólida aqui. |
| <b>Gama de Plano de Fundo</b> <i>sRGB, Linear</i> | Se a Entrada em segundo plano for usada, defina como interpretar a entrada em segundo plano. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="sphere-light.resources/sphere-light-ex.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="sphere-light.resources/spherelight-ex1.png" />
        </td>
    </tr>
</table>
