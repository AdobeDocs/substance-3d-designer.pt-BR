---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/tri-planar.html"
breadcrumb-title: ''
description: Use o nó Triplano para projetar texturas de três planos ortogonais a fim de obter um mapeamento de textura perfeito em geometria complexa.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Tri Planar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Tri Planar
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---


# Tri Planar

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/triplanar-1.png){width="128px"}

![](../../../../../../assets/triplanar-grayscale.png){width="128px"}

## Tri Planar (Tons de Cinza)

**Entrada:** *Geradores Baseados Em Malha**/Utilitários*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Este nó avançado executa o mapeamento de projeção triplanar em 2D, com base nos dados Posição cozida e Espaço Mundial Normal. Isso significa que, essencialmente, converte completamente as coordenadas UV em um mapeamento (na maioria das vezes) sem costura com base na própria malha.

Esta é uma boa maneira de evitar costuras sem ter que reassar cada vez (é possível conseguir algo semelhante com o padeiro). A desvantagem é que este nó é bastante pesado e, portanto, não rápido.

Lembre-se de que as suas bolachas devem ser de alta precisão: bolos de 8 bits não conduzirão a resultados muito bons.

## Parâmetros

### Entradas

* **Posição**: *Entrada de cores*\
  Mapa da posição cozida. Idealmente, uma precisão de 16 bits ou superior.
* **Espaço Mundial Normal**: *Entrada de Cores*\
  Mapa do espaço do mundo cozido, Idealmente 16-bit ou maior precisão.
* **Entrada X**: *Entrada de cor (entrada em tons de cinza)*Mapa de entrada para remapear do UV para o espaço mundial via projeção triplanar. Usado para todos os eixos quando Entradas de imagem estiver definido como 1; para o eixo X, se estiver definido como 3.
* **Entrada Y**: *Entrada colorida (entrada em tons de cinza)*Somente se as entradas de imagem estiverem definidas como 3. Mapa de entrada para remapear de UV para o espaço mundial no eixo Y.
* **Entrada Z**: *Entrada colorida (entrada em tons de cinza)*Somente se as entradas de imagem estiverem definidas como 3. Mapa de entrada para remapear de UV para o espaço mundial no eixo Z.

### Parâmetros

* **Projeção**: *Todos os eixos, somente X, somente Y, somente Z* Define com quais eixos se misturar.
* **Entradas de imagem**: *1 entrada, 3 entradas*\
  Defina se deseja usar um Mapa para todos os Eixos ou um mapa específico por Eixo.
* **Modo de Mesclagem**: *linear, avançado* Aumenta a precisão.
* **Contraste de Mesclagem**: *0.001 - 1.0* Contraste de transição, mesclar entre transições suaves ou ásperas.
* **Fator de Normalização**: *0.0 - 1.0*\
  Melhora a mesclagem da projeção restaurando a perda de contraste na área de mesclagem.
* **Divisão em blocos gráficos**: *0.0 - 10.0* Número de vezes para colocar em blocos gráficos as texturas de entrada.
* **Rotação Global**: *0.0 - 1.0*\
  Rotação global para todos os eixos.
* **Corrigir Projeção Espelhada**: *Falso/Verdadeiro* Defina como manipular as Projeções Espelhadas.
* **Rotação X**: *0.0 - 1.0* Rotação individual sobre o eixo X de projeção.
* **Rotação Y**: *0.0 - 1.0* Rotação individual sobre o eixo Y de projeção.
* **Rotação Z**: *0.0 - 1.0* Rotação individual sobre o eixo Z de projeção.
* **Deslocamento X**: *0.0 - 1.0* Deslocamento sobre o eixo X da projeção.
* **Deslocamento Aleatório X**: *0.0 - 1.0*\
  Permitir a aleatoriedade do deslocamento do eixo X.
* **Deslocamento Y**: *0.0 - 1.0* Deslocamento sobre o eixo Y de projeção.
* **Deslocamento Aleatório Y**: *0.0 - 1.0*\
  Permite a aleatorização do deslocamento do eixo Y.
* **Deslocamento Z**: *0.0 - 1.0* Deslocamento sobre o eixo Z da projeção.
* **Deslocamento Aleatório Z**: *0.0 - 1.0*\
  Permite a aleatoriedade do deslocamento do eixo Z.

## Imagens de exemplo

</td>
</tr>
</table>
