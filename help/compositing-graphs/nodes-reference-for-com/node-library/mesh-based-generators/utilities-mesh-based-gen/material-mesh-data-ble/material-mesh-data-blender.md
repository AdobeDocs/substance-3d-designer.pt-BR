---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-mesh-data-blender.html"
breadcrumb-title: ''
description: Use o nó Misturador de dados de malha de material para mesclar dados de malha de material para criar transições suaves entre diferentes zonas de material.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Mesh Data Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Misturador de dados de malha de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---


# Misturador de dados de malha de material

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-mesh-data-blender.png){width="128px"}

## Misturador de dados de malha de material

**Entrada:** *Geradores Baseados Em Malha**/Utilitários*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

O objetivo desse nó é facilitar bastante a adição de detalhes com base em dados armazenados. Ele vem com vários controles deslizantes para modificar um material de entrada completo, com base em todos e quaisquer mapas baked como entrada. Experimente, pois há muitas opções.

É útil para fazer coisas como adicionar realce de borda com base em curvatura ou outros mapas, mesclar em algum AO com a cor difusa/básica, adicionar Oclusão de Specular com base em curvatura e/ou AO etc.

## Parâmetros

### Entradas

* **Entrada de Material Completa (Grupo “Material”):** Conjunto completo de mapas de material.\
  Eles são modificados por esse nó e retornados novamente como saída.
* **Oclusão De Ambiente**: *Entrada Em Tons De Cinza*\
  Mapa baked usado para efeitos internos e mascaramento.
* **Curvatura**: *Entrada em tons de cinza*\
  Mapa baked usado para efeitos internos e mascaramento.
* **Height**: *Entrada em Tons de Cinza*
* **Normal**: *Entrada De Cores*
* **Cor Do Vértice**: *Entrada De Cores*
* **Espaço Mundial Normal**: *Entrada de Cores*

### Parâmetros

* **Canais**
  * Ative e desative os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza. Afeta a disponibilidade dos parâmetros abaixo.
* **Mapas baked**
  * Se os mapas baked listados devem ou não ser usados para cálculos. Afeta a disponibilidade dos parâmetros abaixo.
* **AO Difuso**: *0.0 - 1.0* Quantidade de Oclusão Ambiente a ser mesclada no Difuso.
* **Bordas cortantes difusas**: 0,0 - 1,0\
  Quantidade do mapa de curvatura para mesclar no Difuso.
* **Cor Difusa Da Cor Do Vértice**: 0,0 - 1,0\
  Quantidade de cozimento da Cor do vértice para mesclar no Difuso.
* **Pré-Iluminação Difusa**: 0.0 - 1.0\
  Quantidade de pré-iluminação (falsa), com base nos World Space Normals.
* **Equilíbrio difuso de iluminação do desenho animado**: 0,0 - 1,0\
  Alterna entre iluminação realista e animada para Difusa.
* **Desenho animado difuso pré-camadas de iluminação**: 0 - 10\
  Controla a aparência dos cálculos de iluminação animada.
* **Contornos Difundidos De Desenho Animado**: 0.0 - 1.0\
  Controla a aparência dos cálculos de iluminação animada.
* **Cor base AO**: 0.0 - 1.0\
  Quantidade de Oclusão ambiente para mesclar na cor de base.
* **Bordas cortantes de cor base**: 0,0 - 1,0\
  Quantidade do mapa de curvatura para mesclar com a cor de base.
* **Cor Base Da Cor Do Vértice**: 0,0 - 1,0\
  Quantidade de cozimento da Cor de vértice para mesclar na Cor de base.
* **Intensidade normal do material**: 0,0 - 1,0\
  Intensidade de mistura do Mapa normal (tangente) assado.
* **SpecularAO**: 0.0 - 1.0\
  Intensidade de mistura do AO no Specular.
* **Bordas cortantes brilhantes do Specular**: 0,0 - 1,0\
  A intensidade de mistura da Curvatura no Specular.
* **Contornos de Desenho de Specular**: 0.0 - 1.0\
  Força de mistura de um efeito de contorno de borda de Specular de desenho animado, com base na Curvatura.
* **Bordas cortantes escuras e reluzentes**: 0,0 - 1,0\
  A intensidade de mistura da Curvatura na Textura reluzente.
* **Aspereza de bordas cortantes brilhantes**: 0,0 - 1,0\
  A intensidade de mistura da Curvatura na Aspereza.
* **Contornos do Desenho Animado de Aspereza**: 0.0 - 1.0\
  Força de mistura de um efeito de contorno de borda de aspereza de desenho animado, com base na Curvatura.
* **Bordas cortantes brilhantes metálicas**: 0,0 - 1,0\
  A intensidade de mistura da Curvatura no Metálico.
* **Contornos de desenhos animados metálicos**: 0.0 - 1.0\
  Força de mistura de um efeito de contorno de borda metálico de desenho animado, com base na Curvatura.
* **Intensidade do AO Materiel**: 0,0 - 1,0\
  Misture a força do AO mapa baked com o AO gerado por material, que grau combinar ambos os mapas de AO em.
* **Intensidade de material do Height**: 0,0 - 1,0\
  Combine a força do Height de mapa baked com o Height gerado por material, em que grau combinar os dois mapas de altura.
* **Tipo De Mesclagem De Material De Height**: Reforçar, Interpolação\
  Modo de mesclagem para combinar ambos os mapas de altura.

## Imagens de exemplo

![](../../../../../../assets/blenddata-ex.gif)

</td>
</tr>
</table>
