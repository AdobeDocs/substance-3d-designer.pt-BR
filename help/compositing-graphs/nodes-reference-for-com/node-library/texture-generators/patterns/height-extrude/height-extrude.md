---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/height-extrude.html"
breadcrumb-title: ''
description: Use o nó Extrusão na Altura para realizar a extrusão de formas com base em mapas de altura para criar efeitos de profundidade semelhantes a 3D no textura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Height Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extrusão na Altura
user-guide-description: ''
user-guide-title: ''
source-git-commit: 827e738d5db4d64bf366d332a62a7bbd2fa840fc
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 3%

---


# Extrusão na Altura

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](height-extrude.resources/height-extrude.png){width="200px"}

<b>Em:</b> Geradores De Textura > Padrões

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O Extrusão na Altura renderiza a Profundidade Z 3D a partir de um mapa de altura de entrada. Assim como a [Extrusão de Forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) e o [Cubo 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md), ela permite girar uma câmera no Visualização 2D. Seu principal objetivo é servir como um gerador para a criação de formas 3D giradas a partir de um mapa de altura plano. Essas formas podem ser usadas com o [respingo de forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md).

A principal diferença com a [Extrusão de Forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-extrude/shape-extrude.md) é que o mapa de entrada não precisa ser um tipo de mapa “alfa” binário, mas um mapa em tons de cinza de intervalo completo. Isso significa que você tem mais controle sobre o height de extrusão (formas orgânicas e complexas), mas não tem controle sobre nada como perfis de chanfro (superfícies duras, formas mais simples).

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Ângulo da Câmera</b> | Ângulos de Euler da câmera, em meia volta. Observe que a rotação e a escala horizontais são aplicadas diretamente à entrada. |
| <b>Escala da Câmera</b> <i>0.001 - 3.0</i> | Escala global aplicada à saída. |
| <b>Escala de Height</b> <i>0.0 - 2.0</i> | Aplica um fator global nos valores do height de entrada. |
| <b>Deslocamento vertical</b> <i>-1.0 - 1.0</i> | Move a saída final para cima ou para baixo. |
| <b>Aterramento</b> <i>Ativado/Desativado</i> | Se Ground estiver desativado, um plano de fundo preto será exibido onde a entrada for 0, em vez de um plano semelhante ao solo. |
| <b>Formato Normal</b> <i>DirectX/OpenGL</i> | O parâmetro <b>Formato Normal</b> inverte a coordenada y do mapa normal. |
| <b>Intensidade normal</b> <i>0.0 - 256.0</i> | Igual ao parâmetro de <b>Intensidade</b> do nó <b>Normal</b>. Defina-o como 256 para obter um normal sem compartilhamento durante a rotação. |
