---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/height-extrude.html"
breadcrumb-title: ''
description: Use o nó Extrusão na Altura para realizar a extrusão de formas com base em mapas de height para criar efeitos de profundidade semelhantes a 3D em texturas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Height Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extrusão na Altura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---


# Extrusão na Altura

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-extrude.png){width="200px"}

## Extrusão na Altura

**Entrada:** *Geradores De Textura**/Padrões*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

O Extrusão na Altura renderiza a Profundidade Z 3D a partir de um mapa de Height de entrada. Assim como a [Extrusão de Forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) e o [Cubo 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md), ela permite girar uma câmera na exibição 2D. Seu principal objetivo é servir como um gerador para a criação de formas 3D giradas a partir de um mapa de altura plano. Essas formas podem ser usadas com o [respingo de forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md).

A principal diferença com a [Extrusão de Forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) é que o mapa de entrada não precisa ser um tipo de mapa “alfa” binário, mas um mapa em tons de cinza de intervalo completo. Isso significa que você tem mais controle sobre o height de extrusão (formas orgânicas e complexas), mas não tem controle sobre nada como perfis de chanfro (superfícies duras, formas mais simples).

## Parâmetros

* **Ângulo da Câmera**:\
  Ângulos de Euler da câmera, em meia volta. Observe que a rotação e a escala horizontais são aplicadas diretamente à entrada.
* **Escala da Câmera**: *0.001 - 3.0*\
  Escala global aplicada à saída.
* **Escala do Height**: *0.0 - 2.0*\
  Aplica um fator global nos valores do height de entrada.
* **Deslocamento Vertical**: *-1.0 - 1.0*\
  Move a saída final para cima ou para baixo.
* **Aterramento**: *Desligado/Ligado*\
  Se Ground estiver desativado, um plano de fundo preto será exibido onde a entrada for 0, em vez de um plano semelhante ao solo.
* **Formato Normal**: *DirectX/OpenGL*\
  O parâmetro **Formato Normal** inverte a coordenada y do mapa normal.
* **Intensidade Normal**: *0.0 - 256.0*\
  Igual ao parâmetro de **Intensidade** do nó **Normal**. Defina-o como 256 para obter um normal sem compartilhamento durante a rotação.

## Imagens de exemplo

</td>
</tr>
</table>
