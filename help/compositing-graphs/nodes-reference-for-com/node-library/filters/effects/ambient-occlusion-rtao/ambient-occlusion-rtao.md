---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-rtao.html"
breadcrumb-title: ''
description: Use o nó Oclusão ambiente (RTAO) para gerar mapas de oclusão ambiente em tempo real a partir de mapas de height para sombreamento realista.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (RTAO)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Oclusão ambiente (RTAO)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---


# Oclusão ambiente (RTAO)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone do nó RTAO](ambient-occlusion-rtao.resources/rt-ao.png "ícone do nó RTAO")

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera um Mapa de Oclusão ambiente com base em uma entrada de mapa de height.

Esse filtro fornece resultados mais precisos em comparação ao HBAO, mas não deve ser usado em combinação com o mecanismo da CPU (SSE) devido ao tempo de cálculo.

Consulte [Oclusão Ambiente (HBAO) (Nó de Filtro)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-hbao/ambient-occlusion-hbao-filter-node.md) para obter uma alternativa mais rápida e simples.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Usar Tamanho físico</b> <i>Booleano</i> | Alterne para usar as configurações de Tamanho físico para determinar a escala do height. |
| <b>Tamanho físico</b> <i>Flutuante3</i> <i>(Disponível quando <b>Usar Tamanho físico</b> estiver definido como <i>Verdadeiro</i>)</i> | Ajusta a escala do height com base no tamanho físico real da superfície |
| <b>Amostras</b> <i>Inteiro</i> | O número de raios usados para calcular a oclusão de ambiente.<br>Um valor mais alto fornece um resultado mais suave e preciso às custas do desempenho. |
| <b>Escala de Height</b> <i>Flutuante</i> <i>(Disponível quando <b>Usar Tamanho físico</b> estiver definido como <i>Falso</i>)</i> | Multiplicador da intensidade de entrada do mapa de height. |
| <b>Distribuição</b> <i>Inteiro</i> | Define o método de distribuição. Afeta a queda em direção a áreas sombreadas, |
| <b>Distância Máxima</b> <i>Flutuante</i> | Define a distância máxima que os raios podem percorrer para serem ocultados. |
| <b>Ângulo de Propagação</b> <i>Flutuante</i> | Define o ângulo de propagação para os raios em que serão disparados. Um valor de 1 é um hemisfério completo. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-rtao.resources/image2021-6-18-11-7-48.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-rtao.resources/image2021-6-18-11-9-0-1.png" />
        </td>
    </tr>
</table>
