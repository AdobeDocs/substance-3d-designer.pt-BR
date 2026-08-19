---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/arc-pavement.html"
breadcrumb-title: ''
description: Use o nó Pavimento de arco para gerar padrões de pavimento em forma de arco para criar texturas curvas de estrada e caminho.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Arc Pavement
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Calçada Arc
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# Calçada Arc

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/arcpavement-ex.png)

## Calçada Arc

**Entrada:** *Geradores De Textura**/Padrões*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Gera um padrão de pavimento de arco parisiense. Este efeito não pode ser obtido com o [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)ou o [Bloco Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) padrão, portanto, este nó dedicado.

## Parâmetros

* **Escala**: *1 - 8* Define a escala/divisão em blocos gráficos globais.
* **Valor do Padrão**: *1 -* 32\
  Define a quantidade de tijolos usada em cada arco.
* **Valor Aleatório do Padrão**: *0.0 - 1.0*\
  Dispõe aleatoriamente a quantidade de tijolos em cada arco. Tem o efeito adicional de dar aos tijolos escalas diferentes.
* **Valor Mínimo de Padrão**: *1 - 10*\
  Controla a quantidade mínima de bricks ao randomizar arcos.
* **Valor dos Arcos**: *0 - 20*\
  Define a quantidade de arcos empilhados verticalmente. Altera o height de tijolos.
* **Padrão**: *Imagem De Entrada, Quadrado, Disco, Paraboloide, Sino, Gaussiano, Espinho, Pirâmide, Tijolo, Gradações, Ondas, Meio Sino, Sino Ondulado, Crescente, Cápsula, Cone*\
  Seleciona a forma de padrão a ser usada.
* **Filtragem De Imagem De Entrada**: *Bilinear + Mipmaps, Bilinear, Mais Próximo*
* **Escala de padrão**: *0.0 - 1.0* Define a escala para cada bloco.
* **Largura do Padrão**: *0.0 - 1.0*\
  Define a largura de cada ladrilho.
* **Height de Padrões**: *0.0 - 1.0*\
  Define o height para cada ladrilho.
* **Aleatório de Largura de Padrão**: *0.0 - 1.0*\
  Dispõe aleatoriamente a largura do ladrilho.
* **Height de padrão aleatório**: *0.0 - 1.0*\
  Height de ladrilho aleatório.
* **Aleatório de Largura de Padrão Global**: *0.0 - 1.0* Aleatório a largura do bloco, sem criar espaços maiores entre eles.
* **Diminuição do Height de padrões**: *0.0 - 1.0* Controla o esmagamento do height lado a lado nas extremidades de cada arco.
* **Aleatório de cores**: *0.0 - 1.0*\
  Dispõe aleatoriamente as cores dos ladrilhos.
* **Expansão não quadrada**: *Falso/Verdadeiro*\
  Permite a compensação de esmagamento e alongamento com proporções não quadradas.

## Imagens de exemplo

![](../../../../../../assets/arcpavement-ex.png)

</td>
</tr>
</table>
