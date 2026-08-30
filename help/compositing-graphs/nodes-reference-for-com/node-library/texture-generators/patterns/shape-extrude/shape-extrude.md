---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-extrude.html"
breadcrumb-title: ''
description: Use o nó Extrusão de forma para realizar a extrusão de formas e criar efeitos de profundidade semelhantes a 3D em texturas do Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extrusão de forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 5%

---


# Extrusão de forma

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-extrude.resources/shape-extrude.png){width="128px"}

<b>Em:</b> Geradores De Textura > Padrões

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Um nó avançado que permite que entradas de “forma” binárias 2D sejam renderizadas em mapas de altura girados em 3D. Funciona de maneira semelhante a uma extrusão em um pacote 3D, em que uma forma é extrudida ao longo do eixo, criando um volume. Em combinação com a Máscara de gradiente de perfil, corpos do tipo Revolução/Torno também podem ser criados. Muito útil para criar formas artificiais complexas para mapas de altura.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada de forma de extrusão</b> <i>Entrada em tons de cinza</i> | Se a Forma de extrusão estiver definida como Personalizada, conecte sua própria (de preferência) máscara de forma binária aqui. |
| <b>Degradê de Perfil</b> <i>Entrada em tons de cinza</i> | Se o Tipo de perfil estiver definido como Gradiente vertical, ele poderá ser usado para definir a escala da forma ao longo do eixo para corpos de Revolução. |
| <b>Máscara de Perfil</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para ocultar ou mostrar a forma com extrusão ao longo do eixo. Pode ser usado para interromper a continuidade da forma ao longo de seu eixo. Interpretado apenas como binário: os valores de inserção em tons de cinza são arredondados para 0 ou 1. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Extrusão do Height</b> <i>0.0 - 1.0</i> | Quantidade para extrudar a forma para cima a partir do centro. |
| <b>Extrusão de Profundidade</b> <i>0.0 - 1.0</i> | Quantidade para aplicar extrusão à forma por downwatds do centro. |
| <b>Forma de Extrusão</b> <i>Cubo, Cilindro, Entrada Personalizada</i> | Use formas incorporadas ou insira a sua própria forma personalizada externamente. |
| <b>Tamanho da Forma de Extrusão</b> <i>0.0 - 1.0</i> | Usado apenas com Cubo e Cilindro integrados, determina o tamanho da forma de base e pode ser dimensionado de forma não uniforme. |
| <b>Escala</b> <i>0.0 - 1.0</i> | Defina a escala global para o efeito. Com Formas Internas, essa é uma escala de forma de base uniforme e não afeta o Height ou a Profundidade.<br><br>Com a Entrada Personalizada, essa ação dimensiona todo o resultado final de maneira uniforme. |
| <b>Tipo de Perfil</b> <i>Reta, Gradiente vertical, Máscara</i> | Controle principal para determinar o comportamento do efeito e o uso de mapas de entrada extras opcionais.<br><br>Reta é o comportamento de Extrusão padrão, Gradiente vertical permite valores de escala personalizados ao longo do eixo inteiro, Máscara permite ocultar seções ao longo do eixo por máscara. |
| <b>Height de chanfro</b> <i>0.0 - 1.0</i> | Defina até onde o chanfro alcança ao longo do eixo de extrusão. |
| <b>Intensidade de chanfro</b> <i>0.0 - 1.0</i> | Defina quanto o chanfro será retraído da forma original. |
| <b>Curva de chanfro</b> <i>-1.0 - 1.0</i> | Defina uma curva convexa ou côncava do efeito Chanfro. Um valor de 0 significa reto, sem curva. |
| <b>Chanfro Espelho</b> <i>Falso/Verdadeiro</i> | Alterne para aplicar o Chanfro na parte superior e inferior da forma. |
| <b>Reduzir Multiplicador</b> <i>0 - 2</i> | Controle integrado de downscaling fácil. Pode ser usado para adicionar a Suavização de borda rapidamente; certifique-se de também aumentar a resolução do nó. |
| <b>Posição</b> | Controle principal para resultado de rotação em espaço 3D. Correlaciona-se com a interferência de Gizmo na Visualização 2D. |
| <b>Intervalo de saída</b> <i>[0, 1], [-1, 1]</i> | Defina os valores mínimo e máximo de saída. Se o intervalo for definido como [-1,1], os valores negativos serão apresentados em preto. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-extrude.resources/shape-extrude-1.png" />
        </td>
    </tr>
</table>
