---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/interface/properties.html"
breadcrumb-title: ''
description: Use o painel Propriedades no Substance 3D Designer para exibir e editar propriedades de nó e parâmetros de gráfico.
helpx_creative_field: ""
helpx_description: Designer > Interface > Properties
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Propriedades
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---


# Propriedades

Esta página apresenta o painel <b>Propriedades </b> do Substance 3D Designer, seu layout e as diferentes implementações, categorias e parâmetros que você pode encontrar. Ele está focado nas propriedades de [gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md). [gráficos de funções](../../function-graphs/function-graphs.md) e [gráficos FX-Map](../../function-graphs/fxmaps/fxmaps.md) têm layouts mais simples.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Visão geral

O painel <b>Propriedades </b> é um painel sensível ao contexto que muda com base na sua seleção na [Exibição de Gráfico](../../interface/the-graph-view/the-graph-view.md) e na janela do [Explorer](../the-explorer-window/the-explorer-window.md).

</td>
<td style="border: 0;" valign="top">

![Áreas de propriedades](../../assets/image2020-11-9-13-49-48.png "Áreas de propriedades")

</td>
</tr>
</table>

Ele permite que você altere as propriedades dos nós e recursos selecionados, juntamente com a [Exibição de gráfico](../../interface/the-graph-view/the-graph-view.md), é provavelmente seu segundo painel de interface do usuário mais usado no Designer.

O painel Propriedades é dividido em algumas implementações diferentes, dependendo de sua seleção, por exemplo:

* <b>Parâmetros Base</b> e <b>Entrada-</b> ou <b>Parâmetros Específicos</b> para nós
* <b>Atributos</b> e <b>Metadados</b> para a maioria dos nós e Pacotes

Um recurso importante do Ecossistema de Substance, [Expor parâmetros](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), é feito por meio do painel Propriedades.

>[!NOTE]
>
> A maioria dos campos numéricos oferece suporte a *fórmulas matemáticas básicas* como entrada. Por exemplo, `17+3.5`, `7/3`, `(4+2)*3`. Pressione *Enter* para validar a fórmula e o resultado será inserido no campo. Se a fórmula for inválida, o campo reverterá para seu valor anterior.\
> Alguns campos numéricos em outras partes do aplicativo, como a caixa de diálogo [Expor parâmetro](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), também oferecem suporte a esse recurso.

## Gráficos de nós e Substance

Os nós e [gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md) têm um conjunto de categorias de propriedades ligeiramente sobreposto, e sua funcionalidade é semelhante.

Os <b>Parâmetros Base</b> e os <b>Atributos</b> são idênticos entre Nós e Gráficos.

Os nós oferecem <b>Parâmetros Específicos</b> ou<b> Parâmetros de Instância</b> (dependendo de se forem [nós Atômicos](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md) ou [Instâncias](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)), bem como <b>Valores de Entrada</b> para trabalhar com [valores](../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md).

Os nós atômicos [de entrada](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)e [de saída](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)são exceções, pois apresentam os <b>Atributos de Integração</b> e as <b>Condições</b> para visibilidade. Esses dois conjuntos de propriedades também podem ser acessados centralmente nas propriedades do gráfico, em Entradas e Saídas.

Os gráficos têm algumas categorias extras. <b>Parâmetros de Entrada</b> lista [parâmetros expostos](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), <b>Entradas</b> e <b>Saídas</b> lista todas as propriedades dos nós de Entrada e Saída. [Você pode encontrar todas as propriedades do Gráfico explicadas em detalhes em uma página dedicada.](../../compositing-graphs/graph-parameters/graph-parameters.md)

## Recursos e pacotes

O painel Propriedades também responde às alterações de seleção no [Explorer](../the-explorer-window/the-explorer-window.md). Ele pode servir como outra maneira de selecionar um gráfico (em vez de clicar duas vezes em uma área vazia) e também permite alterar as propriedades de Pacote e [Recurso](../../resources/resources.md).

Os pacotes têm seções **Informações**, **Atributos** e **Metadados**. [Os metadados do pacote estão descritos em uma página dedicada.](../../package-metadata/package-metadata.md)

Os recursos têm propriedades específicas para seu tipo, [detalhadas em páginas dedicadas](../../resources/resources.md).
