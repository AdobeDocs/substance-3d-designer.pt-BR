---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/scratches-generator.html"
breadcrumb-title: ''
description: Use o nó Gerador de Scratches para criar padrões de rascunho de procedimento para adicionar desgaste e danos aos materiais.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Scratches Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gerador de Scratches
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---


# Gerador de Scratches

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/scratches-generator.png)

## Gerador de Scratches (normal)

**Entrada:** *Geradores De Textura**/Padrões*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Isso coloca riscos aleatórios com várias opções de personalização, por exemplo, permitindo definir a direção, a distribuição e a distorção.

Há uma versão especial de Scratches Generator, Scratches Generator Normal, que gera Normalmaps com base na profundidade desses arranhões. A maioria das opções é exatamente a mesma, mas ela tem alguns parâmetros extras claramente marcados para as configurações de Normal (veja abaixo).

## Parâmetros

* **Número de spline**: *1 - 512* Quantidade de arranhões (splines) a serem colocados.
* **Máximo de Segmentos por Spline**: *2 - 256* Quantidade de segmentos/subdivisões ao longo do comprimento de um rascunho. Leva a curvas e distorções mais suaves. O efeito é mais perceptível com valores de Distorção mais altos.
* **Rotação de spline**: *0.0 - 1.0* Rotação uniforme de todas as splines, para orientá-las em uma direção.
* **Rotação de spline aleatória**: *0.0 - 1.0* Variação de ângulo, gira aleatoriamente cada spline.
* **Escala de spline**: *0.0 - 1.0* Dimensiona uniformemente todas as splines.
* **Escala de spline aleatória**: *0.0 - 1.0* Dimensiona aleatoriamente cada spline individualmente.
* **Distorção de spline**: *0.0 - 1.0* Nível de distorção uniforme em todas as splines.
* **Distorção de spline aleatória**: *0.0 - 1.0* Aleatoriamente o nível de distorção de cada spline individualmente.
* **Frequência de Distorção de spline**: *0.0 - 1.0* Define a frequência de distorção e controla a escala dos detalhes de distorção.
* **Largura da spline**: *0.0 - 2.0* Define a largura de todas as splines uniformemente.
* **Aleatório na Largura da spline**: *0.0 - 1.0* Torna aleatória a largura da spline de cada spline individualmente.
* **Posição da spline aleatória**: *0.0 - 1.0* Aleatoriamente torna a posição de cada spline individual. Quanto menor esse valor, mais splines serão agrupadas no centro da tela. Pode ser usado para criar manchas de arranhões.
* **Definir a Largura da Curva em px**: *Falso/Verdadeiro* Determina as unidades usadas para as configurações de largura da curvatura.
* **Luminância aleatória (somente versão em Tons de Cinza)**: *0.0 - 1.0* Torna aleatória a Luminância de cada spline individualmente.
* **Intensidade normal (somente versão normal)**: *0.0 - 1.0* Define a intensidade do efeito Normal para cada spline globalmente.
* **&#x200B; Normal Intensity Random &#x200B;**(Apenas na versão normal)***: *0.0 - 1.0*Torna aleatória a intensidade normal para cada spline individualmente.
* **&#x200B; Formato Normal &#x200B;**(Somente versão normal)***: *DirectX, OpenGL*\
  Alterna entre diferentes formatos de Mapas Normais (inverte o canal verde).
* **Modo de Atenuação**: *Nenhum, Início, Fim, Início + Fim* Define se e em que direção as linhas de spline desaparecem.
* **Comprimento do fade**: *0.0 - 1.0* Define o comprimento do efeito de fade, se habilitado acima.
* **Expansão não quadrada**: *Falso/Verdadeiro*\
  Permite a compensação de esmagamento e alongamento com proporções não quadradas.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/scratches-ex1.png" width="256px"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../../../assets/scratches-ex2.png" width="256px"/></div> |
| --- | --- |
|  |  |

</td>
</tr>
</table>
