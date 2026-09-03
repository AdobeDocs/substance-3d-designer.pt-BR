---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-hbao-filter-node.html"
breadcrumb-title: ''
description: Use o nó do filtro HBAO de Oclusão ambiente para gerar mapas de oclusão ambiente usando algoritmos baseados em horizonte para sombreamento realista.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (HBAO) (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Oclusão ambiente (HBAO) (nó de filtro)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 5%

---


# Oclusão ambiente (HBAO) (nó de filtro)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](ambient-occlusion-hbao-filter-node.resources/ambient-occlusion-hbao-filter-node-01.png){width="128px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Utiliza um Heightmap como entrada e gera um mapa de Oclusão Ambiente a partir dele. Ele usa a Oclusão ambiente baseada em Horizon, um algoritmo originalmente destinado para a geração AO em tempo real de espaço de tela. Muito útil para criar mapas de AO de procedimento a partir de Heightmaps de procedimento.

Para uma versão alternativa mais avançada, mas mais lenta, do AO, consulte [Oclusão ambiente (RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Usar Unidades Mundiais</b> <i>Falso/Verdadeiro</i> | Alterna o uso de unidades de mundo ou espaço de tela. Habilita parâmetros extras que permitem um controle mais preciso. |
| <b>Profundidade DE Height</b> <i>0.0 - 1.0</i> | Usado somente quando Unidades Mundiais está definido como Falso. Controla o dimensionamento global. |
| <b>Tamanho da superfície</b> <i>0.0 - 1000.0</i> | Usado somente quando Unidades Mundiais está definido como Verdadeiro. Controla o dimensionamento global. |
| <b>Escala do Height (cm)</b> <i>0.0 - 1000.0</i> | Usado somente quando Unidades Mundiais está definido como Verdadeiro. Controla o dimensionamento global. |
| <b>Raio</b> <i>0.0 - 1.0</i> | Controla a propagação do AO. |
| Qualidade <b>1</b> <i>4 amostras, 8 amostras, 16 amostras</i> | Define o nível de Qualidade determinando a quantidade de amostras usada para cálculo. |
| <b>Otimização de GPU</b> <i>Falso/Verdadeiro</i> | Permite a otimização interna da GPU, acelera o processamento. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-hbao-filter-node.resources/ambient-occlusion-hbao-filter-node-02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-hbao-filter-node.resources/ambient-occlusion-hbao-filter-node-03.png" />
        </td>
    </tr>
</table>
