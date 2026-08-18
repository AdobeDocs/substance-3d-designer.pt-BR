---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape.html"
breadcrumb-title: ''
description: Use o nó Forma para gerar formas geométricas básicas para criar padrões e texturas no Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# Forma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-2.png){width="128px"}

## Forma

**Entrada:** *Geradores De Textura**/Padrões*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma variedade de formas de procedimento, com opções para modificar as formas de base. As formas são sempre perfeitamente interpoladas e de alta precisão.

Apesar de sua simplicidade, este é um nó muito útil: é o bloco de construção da maior parte da geração Heightmap processual! Combinando formas básicas com nós de transformação, você pode criar uma forma de Heightmap totalmente processual que é muito mais precisa do que qualquer bitmap.

## Parâmetros

* **Divisão em blocos gráficos**: *1 - 16*\
  Define a quantidade de vezes que o resultado deve ser colocado lado a lado.
* **Padrão**: *Quadrado, Disco, Paraboloide, Sino, Gaussiano, Espinho, Pirâmide, Tijolo, Gradação, Ondas, Meio Sino, Sino Ondulado, Crescente, Cápsula, Cone*, Hemisfério**\
  Seleciona a forma de padrão a ser usada.
* **Específico de Padrão**: *0.0 - 1.0*\
  Permite que você altere a forma do padrão selecionado. O efeito depende do padrão selecionado.
* **Escala**: *0.0 - 1.0* Dimensiona toda a forma.
* **Tamanho**: *0.0 - 1.0* Permite um dimensionamento não uniforme sobre o eixo X ou Y.
* **Ângulo**: *0.0 - 1.0* Gira toda a forma.
* **Rotação 45°**: *Falso/Verdadeiro* Gira em 45 graus predefinidos.
* **Expansão não quadrada**: *Falso/Verdadeiro*\
  Permite a compensação de esmagamento e alongamento com proporções não quadradas.
* **Divisão em blocos gráficos não quadrados**&#x200B;**:** *Falso/Verdadeiro*Quando o Expansão não quadrada estiver habilitado, ele irá cobrir a forma sem esmagamento.

## Imagens de exemplo

![](../../../../../../assets/shape-ex.gif)

</td>
</tr>
</table>
