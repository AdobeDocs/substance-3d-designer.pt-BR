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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---


# Luz da forma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-shape.png){width="200px"}

## Luz da forma

**Entrada:** *Exibição 3D/Ferramentas HDRI*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera uma forma retangular projetada esfericamente. A transformação da forma é orientada por um cursor de transformação.

## Entradas

* **Entrada de imagem de fundo**: *Entrada de cor* Plano de fundo opcional no qual compor a luz gerada.
* **Entrada de imagem da forma**: *Entrada de cores* Imagem opcional para mapear para a luz da esfera. Usado somente quando o Modo de cor da forma está definido como Entrada de imagem.

## Parâmetros

* **Matriz de Formas**
  * **Matriz**: *(Matriz de Transformação)*\
    Controle de transformação do resultado. O resultado pode ser modificado interagindo diretamente com a tela.
  * **Deslocamento**: *-2.0 - 2.0*\
    Move ou traduz o resultado. O resultado pode ser modificado interagindo diretamente com a tela.
* **Forma**: *Retângulo, Disco*\
  Escolha a forma a ser inserida.
* **Modo De Cores Da Forma**: *RGB, Temperatura (Kelvin), Entrada De Imagem*\
  Escolha o método a ser usado para definir a cor da forma. A Entrada de imagem permite o uso do segundo slot de entrada.
* **Cor**: *(valor da cor)*\
  Somente com o Modo de cor da forma definido como RGB. Escolhe a cor da forma.
* **Temperatura da forma**: *800.0 - 20000.0*\
  Somente com o Modo de cor da forma definido como Temperatura. Define o valor de Kelvin para a cor da forma.
* **Gama de Entrada da Imagem da Forma**: *sRGB, Linear*\
  Somente com o Modo de cor da forma definido como Entrada de imagem. Determine como interpretar a entrada de imagem de forma.
* **Exposição De Forma (EV)**: *0.0 - 10.0*\
  Defina o valor de exposição para a forma gerada, de forma ideal para o valor de exposição da imagem de plano de fundo.
* **Dureza da Forma**: *0.0 - 1.0*\
  Definir dureza das bordas da forma.
* **Exposição a Ponto de Acesso (EV)**: *0.0 - 10.0*\
  Definir a exposição do ponto ativo central. Observe que isso não é muito visível no modo RGB.
* **Tamanho do Ponto de Acesso**: *0.0 - 1.0*\
  Tamanho do Ponto de Acesso central.
* **Queda do Ponto de Acesso**: *0.0 - 1.0*\
  Queda do ponto de acesso central.
* **Posição do Ponto de Acesso**: *0.0 - 1.0*\
  Posição X e Y do ponto de acesso central.
* **Habilitar Entrada em Segundo Plano**: *Falso/Verdadeiro*\
  Alterna o uso da imagem de fundo opcional. Os compostos geraram luz na parte superior do plano de fundo.
* **Cor do plano de fundo**: *(Valor da cor)*\
  Se a Entrada do plano de fundo não for usada, defina um valor de plano de fundo de cor sólida aqui.
* **Gama de Plano de Fundo**: *sRGB, Linear* Se a Entrada de Plano de Fundo for usada, defina como interpretar a entrada de Plano de Fundo.

## Imagens de exemplo

![](../../../../../../assets/shape-light-ex.gif)

</td>
</tr>
</table>
