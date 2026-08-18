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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---


# Extrusão de forma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-extrude.png){width="128px"}

## Extrusão de forma

**Entrada:** *Geradores De Textura**/Padrões*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Um nó avançado que permite que entradas de “forma” binárias 2D sejam renderizadas em mapas de altura girados em 3D. Funciona de maneira semelhante a uma extrusão em um pacote 3D, em que uma forma é extrudida ao longo do eixo, criando um volume. Em combinação com a Máscara de gradiente de perfil, corpos do tipo Revolução/Torno também podem ser criados. Muito útil para criar formas artificiais complexas para mapas de altura.

## Parâmetros

### Entradas

* **Entrada de forma de extrusão**: *entrada em tons de cinza* se a Forma de extrusão estiver definida como Personalizada, conecte sua própria (de preferência) máscara de forma binária aqui.
* **Gradiente do perfil**: *Entrada em tons de cinza\
  Se o Tipo de Perfil for definido como Gradiente Vertical, ele poderá ser usado para definir a escala da forma ao longo do eixo, para corpos de Revolução.*
* **Máscara de Perfil**: *Entrada em Tons de Cinza*\
  Slot de máscara usado para ocultar ou mostrar a forma com extrusão ao longo do eixo. Pode ser usado para interromper a continuidade da forma ao longo de seu eixo. Interpretado apenas como binário: os valores de inserção em tons de cinza são arredondados para 0 ou 1.

### Parâmetros

* **Height de Extrusão**: *0.0 -* 1.0\
  Quantidade para extrudar a forma para cima a partir do centro.
* **Profundidade de extrusão**: *0.0 - 1.0* Quantidade de extrusão de forma por downwatds do centro.
* **Forma de Extrusão**: *Cubo, Cilindro, Entrada Personalizada* Use formas internas ou insira sua própria forma Personalizada externamente.
* **Tamanho da Forma de Extrusão**: *0.0 - 1.0* Usado apenas com Cubo e Cilindro Internos, determina o tamanho da forma base e pode ser dimensionado de forma não uniforme.
* **Escala**: *0.0 - 1.0*\
  Defina a escala global para o efeito. Com as formas incorporadas, essa é uma escala de forma de base uniforme e não afeta o Height ou a Profundidade.\
  Com a Entrada personalizada, isso dimensiona todo o resultado final de maneira uniforme.
* **Tipo de perfil**: *Reta, Gradiente vertical, Máscara* Controle principal para determinar o comportamento do efeito e o uso de mapas de entrada extras opcionais.\
  Em linha reta é o comportamento de Extrusão padrão, o Gradiente vertical permite valores de escala personalizados ao longo de todo o eixo, a Máscara permite ocultar seções ao longo do eixo por máscara.
* **Height de chanfro**: *0.0 - 1.0* Defina até onde o chanfro alcança ao longo do eixo de extrusão.
* **Intensidade de chanfro**: *0.0 - 1.0* Defina o quanto o chanfro retrai da forma original.
* **Curva de chanfro**: *-1.0 - 1.0* Defina uma curva convexa ou côncava do efeito de chanfro. Um valor de 0 significa reto, sem curva.
* **Chanfro espelhado**: *Falso/Verdadeiro* Alterne para aplicar o Chanfro na parte superior e inferior da forma.
* **Multiplicador de Downscale**: *0 - 2* Controle de downscaling fácil e integrado. Pode ser usado para adicionar a Suavização de borda rapidamente; certifique-se de também aumentar a resolução do nó.
* **Posição**:\
  Controle principal para resultado de rotação em espaço 3D. Correlaciona-se com a interferência de Gizmo na exibição 2D.
* **Intervalo de saída**: *[0, 1], [-1, 1]*Define os valores mínimo e máximo da saída. Se o intervalo for definido como [-1,1], os valores negativos serão apresentados em preto.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shape-extrude-1.png" width="256px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
