---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-rtao.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# Oclusão ambiente (RTAO)

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![Ícone do nó RTAO](../../../../../../assets/rt-ao.png "ícone do nó RTAO")

<b>Entrada:</b> *Filtros/Efeitos*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrição

Gera um Mapa de Oclusão ambiente com base em uma entrada de mapa de height.

Esse filtro fornece resultados mais precisos em comparação ao HBAO, mas não deve ser usado em combinação com o mecanismo da CPU (SSE) devido ao tempo de cálculo.

Consulte [Oclusão Ambiente (HBAO) (Nó de Filtro)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-hbao/ambient-occlusion-hbao-filter-node.md) para obter uma alternativa mais rápida e simples.

</td>
</tr>
</table>

## Parâmetros

<b>Usar Tamanho físico</b> *Booleano*\
Alterne para usar as configurações de Tamanho físico para determinar a escala do height.

<b>Tamanho físico</b> *Flutuante3* (Disponível quando <b>Usar Tamanho físico</b> estiver definido como *Verdadeiro*)\
Ajusta a escala do height com base no tamanho físico real da superfície

<b>Amostras </b>*Inteiras*\
O número de raios usados para calcular a oclusão ambiente.\
Um valor mais alto fornece um resultado mais tranquilo e preciso em detrimento do desempenho.

<b>Escala de Height</b> *Flutuante* (Disponível quando <b>Usar Tamanho físico</b> estiver definido como *Falso*)\
Multiplicador da intensidade de entrada do mapa de height.

<b>Distribuição</b> *Inteiro* Define o método de distribuição. Afeta a queda em direção a áreas sombreadas,

<b>Distância Máxima</b> *Flutuante*\
Define a distância máxima que os raios podem percorrer para serem ocultados.

<b>Ângulo de propagação</b> *Flutuante*\
Define o ângulo de propagação para os raios em que serão disparados. Um valor de 1 é um hemisfério completo.

## Imagens de exemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Nó RTAO - Exemplo 1](../../../../../../assets/image2021-6-18-11-7-48.png "Nó RTAO - Exemplo 1")

</td>
<td style="border: 0;" valign="top">

![Nó RTAO - Exemplo 2](../../../../../../assets/image2021-6-18-11-9-0-1.png "Nó RTAO - Exemplo 2")

</td>
</tr>
</table>
