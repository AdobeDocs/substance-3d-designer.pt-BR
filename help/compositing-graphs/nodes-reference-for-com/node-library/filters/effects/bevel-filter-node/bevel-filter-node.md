---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/bevel-filter-node.html"
breadcrumb-title: ''
description: Use o nó do filtro de Chanfro para criar bordas chanfradas em formas e padrões para adicionar profundidade e dimensão.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Bevel (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Chanfro (Nó de filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 4%

---


# Chanfro (Nó de filtro)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](bevel-filter-node.resources/bevel.png){width="128px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Executa um efeito de chanfro de borda em um Heightmap em tons de cinza de entrada. Retorna Heightmap e Normalmap chanfrados com base nesse Heightmap.

Esse é um nó útil para aplicar perfis de curva exatos em um mapa de altura básico idealmente binário (preto/branco de contrato alto).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>entrada</b> <i>Entrada em tons de cinza</i> | Mapa de altura a converter. |
| <b>Curva personalizada</b> <i>Entrada em tons de cinza</i> | Gradiente que determina a curva/inclinação exata. O ideal é um nó Gradiente linear, no qual você pode executar qualquer tipo de ajuste, como [Níveis](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md) ou [Curvas](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md). Ativo somente quando “Usar curva personalizada” é Verdadeiro. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Distância</b> <i>-1.0 - 1.0</i> | O quanto o efeito de chanfro deve alcançar. |
| <b>Tipo de Canto</b> <i>Redondo, Angular</i> | Se o perfil de chanfro deve ser arredondado ou reto. |
| <b>Suavização</b> <i>0.0 - 5.0</i> | Quantidade de suavização adicional (desfoque) a ser executada após o chanfro. |
| <b>Usar Desfoque Não Uniforme</b> <i>Falso/Verdadeiro</i> | Se a suavização deve ser feita de maneira não uniforme. |
| <b>Usar curva personalizada</b> <i>Falso/Verdadeiro</i> | Alterna o uso de sua própria curva de height personalizada. Veja acima para obter mais informações. |
| <b>Intensidade normal</b> <i>0.0 - 50.0</i> | Intensidade do Normalmap gerado. |
| <b>Formato Normal</b> <i>DirectX, OpenGL</i> | Alterne entre diferentes formatos de Mapas Normais (inverte o canal Verde). |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="bevel-filter-node.resources/bevel-example.png" />
        </td>
    </tr>
</table>
