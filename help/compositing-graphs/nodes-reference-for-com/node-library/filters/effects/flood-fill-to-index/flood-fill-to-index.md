---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-index.html"
breadcrumb-title: ''
description: Use o nó Flood Fill para indexar para preencher regiões com valores de índice para criar padrões numerados e rotulados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Index
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fill para Índice
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 3%

---


# Flood Fill para Índice

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-index.resources/floodfill-index.png){width="200px"}

<b>Entrada:</b> Filtros > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Flood Fill para Índice converte cada célula de Flood Fill em um valor de acordo com seu número de índice, começando com 0 no canto superior esquerdo. Ele pode ser usado para retornar tons de tons de cinza em uma forma normalizada (0,0 a 1,0, dividido por tantas células quantas encontradas por Flood Fill) ou como um valor não bloqueado HDR (0 a n onde n é o número de células).

Além disso, o Flood Fill para Índice usa [valores](../../../../../values-compositing-graphs/values-in-substance-compositing-graphs.md), retornando a quantidade de formas encontradas e a tabela de dados interna opcional.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Flood Fill Bbox</b> <i>Entrada de cores</i> | Mapa de entrada de Flood Fill padrão. Obrigatório. |
| <b>Informações sobre formas especiais</b> <i>Entrada de cores</i> | O mapa de Flood Fill extra precisa ser habilitado explicitamente no nó de Flood Fill anterior e precisa ser conectado!. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Saída</b> <i>Normalizado, Inteiro</i> | Determine se a saída está no intervalo 0-1 do LDR ou no intervalo 0-n do HDR. |
| <b>Ignorar Forma Menor Que</b> <i>0.0 - 1.0</i> | Valor de tolerância para ignorar formas pequenas. |
| <b>Mostrar Tabela de Dados de Flood Fill</b> <i>Falso/Verdadeiro</i> | Retorna dados extras (depuração) para uso avançado. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-index.resources/flood-fill-ex02.jpg" />
        </td>
    </tr>
</table>
