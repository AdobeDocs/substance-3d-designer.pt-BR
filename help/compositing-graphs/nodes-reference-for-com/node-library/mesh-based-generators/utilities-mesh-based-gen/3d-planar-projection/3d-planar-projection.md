---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/3d-planar-projection.html"
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
source-git-commit: fbf066c7185f74dcbf35156afc3873d192f77abc
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 7%

---


# Projeção planar 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/3d-planar-gray.png)![](../../../../../../assets/3d-planar.png)

<b>Entrada:</b> Geradores Baseados Em Malha > Utilitários

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Executa uma projeção planar com base em dados de malha cozida (mapas de posição e normais mundiais). Permite projetar e inserir decalques em emendas, independentemente do mapeamento UV original.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Mapa de posições</b> <i>Entrada de cores</i> | Mapa de posição feito bake |
| <b>Espaço Mundial Normal</b> <i>Entrada de cores</i> | Mapa normal do espaço feito bake |
| <b>Textura Projetada</b> <i>Entrada de cores</i> | Inserir textura para projetar no destino. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Posicionamento</b> |  |
| <b>Entrada do projeto</b> <i>Posição UV, Posição do Espaço Mundial</i> | Escolha se a posição de projeção é definida em 2D/UV ou no espaço 3D/Mundial. |
| <b>Posição UV de Destino</b> | Somente com a Entrada de posição UV, mais adequada para escolher um ponto na exibição 2D do mapa de posição. |
| <b>Posição de Destino</b> <i>(Valor da cor)</i> | Somente com a Entrada da posição do espaço mundial, é possível definir uma coordenada 3D exata. |
| <b>Destino Normal</b> <i>(Valor da cor)</i> |  |
| <b>Rotação</b> <i>0.0 - 1.0</i> | Gira a textura projetada ao longo do eixo normal. |
| <b>Escala</b> <i>0.0 - 1.0</i> | Defina a escala global para a textura projetada. |
| <b>Tamanho</b> <i>0.0 - 2.0</i> | Executar dimensionamento não uniforme na textura projetada. |
| <b>Mascaramento</b> |  |
| <b>Profundidade máxima</b> <i>0.0 - 1.0</i> | Controla a profundidade em que a textura projetada será exibida, quando cortada. |
| <b>Desvanecer Profundidade</b> <i>0.0 - 1.0</i> | Defina a transição para que a profundidade de corte seja repentina ou desbotada. |
| <b>Limite Normal</b> <i>-1.0 - 1.0</i> | Defina o limite para superfícies não exatamente alinhadas com a normal de projeção. |
| <b>Desvanecimento Normal</b> <i>0.0 - 1.0</i> | Defina a transição para superfícies não alinhadas a repentinas ou atenuadas. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3d-planar-projection-ex.gif" />
        </td>
    </tr>
</table>
