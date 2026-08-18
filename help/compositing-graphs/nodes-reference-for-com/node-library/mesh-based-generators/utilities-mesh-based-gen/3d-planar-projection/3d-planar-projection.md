---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/3d-planar-projection.html"
breadcrumb-title: ''
description: Use o nó Projeção planar 3D para projetar texturas em superfícies de malha usando projeção planar para mapeamento de textura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > 3D Planar Projection
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Projeção planar 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# Projeção planar 3D

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3d-planar-gray.png)![](../../../../../../assets/3d-planar.png)

## Projeção planar 3D (cor)

**Entrada:** *Geradores Baseados Em Malha**/Utilitários*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Executa uma projeção planar com base em dados de malha cozida (mapas de posição e normais mundiais). Permite projetar e inserir decalques em emendas, independentemente do mapeamento UV original.

## Parâmetros

### Entradas

* **Mapa De Posição**: *Entrada De Cores* Mapa De Posição Assado
* **Espaço Mundial Normal**: *Entrada de Cores* Mapa do Espaço Mundial Normal Assado
* **Textura Projetada**: *Entrada de Cores* Textura de entrada para projetar no destino.

### Parâmetros

* **Posicionamento**
  * **Entrada do Projeto**: *Posição UV, Posição do Espaço Mundial* Escolha se a posição da projeção está definida em 2D/UV ou no espaço 3D/Mundo.
  * **Posição UV de Destino**:\
    Somente com a Entrada de posição UV, mais adequada para escolher um ponto na exibição 2D do mapa de posição.
  * **Posição de destino**: *(valor da cor)*Somente com a Entrada da Posição do Espaço Mundial, permite definir uma coordenada 3D exata.
  * **Destino Normal**: *(Valor da cor)*
  * **Rotação**: *0.0 - 1.0\
    Gira a textura projetada ao longo de seu eixo normal.*
  * **Escala**: *0.0 - 1.0*\
    Defina a escala global para a textura projetada.
  * **Tamanho**: *0.0 - 2.0* Execute um dimensionamento não uniforme na textura projetada.
* **Mascaramento**
  * **Profundidade máxima**: *0.0 - 1.0* Controla a profundidade em que a textura projetada aparecerá, quando ela será cortada.
  * **Desvanecimento da Profundidade**: *0.0 - 1.0* Defina a transição para que a profundidade de corte seja repentina ou desbotada.
  * **Limite Normal**: *-1.0 - 1.0* Defina o limite para superfícies não alinhadas exatamente com o normal de projeção.
  * **Desvanecer normal**: *0.0 - 1.0* Defina a transição para superfícies não alinhadas para repentina ou desvanecer.

## Imagens de exemplo

![](../../../../../../assets/3d-planar-projection-ex.gif)

</td>
</tr>
</table>
