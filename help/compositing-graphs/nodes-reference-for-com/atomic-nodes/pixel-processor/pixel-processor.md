---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/pixel-processor.html"
breadcrumb-title: ''
description: Use o nó Processador de pixels para processar pixels individuais usando expressões personalizadas para manipulação avançada de textura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Pixel processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Processador de pixels
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 1%

---


# Processador de pixels

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: Processador de pixels](../../../../assets/comp_pixelprocessor_1.png "Nó atômico: Processador de pixels"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Gera uma imagem na qual o valor de cada pixel é o resultado do [gráfico de função Substance](../../../../function-graphs/the-function-graph/the-function-graph.md) especificado.

O Processador de pixels permite executar uma função personalizada para cada pixel retornado como saída, em uma entrada opcional.

É de longe o nó mais versátil, pois permite que qualquer operação matemática seja executada e retorne resultados dentro do seu gráfico.

</td>
</tr>
</table>

Semelhante ao [FX-Map](../../../../function-graphs/fxmaps/fxmaps.md), ele requer a configuração da funcionalidade interna para executar qualquer ação. A diferença entre o Processador de pixels e o FX-Map é que ele não está focado no posicionamento de padrões, com várias funções controlando a forma e o posicionamento dos padrões. Em vez disso, uma única função é executada em paralelo para cada pixel, onde cada pixel não tem conhecimento dos resultados de cálculo de seus vizinhos.

O Processador de pixels é semelhante ao [Processador de valor](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md), que é executado somente com valores únicos e pode fornecer uma boa otimização em comparação ao Processador de pixels.

Para qualquer pessoa acostumada a criar funções de [sombreador](../../../../glossary/glossary.md) em editores baseados em nó, o Processador de pixels deve oferecer um ambiente familiar.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> Um arquivo de projeto anotado que demonstra usos simples do nó de Processador de pixels está disponível na seção [Gráficos de Substance de amostra](../../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md) desta documentação.
> 
> O nó [Processador de valor](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) é um bom ponto de partida para aprender sobre [gráficos de função Substance](../../../../function-graphs/the-function-graph/the-function-graph.md).
> 
> Considere também que trabalhar com esse tipo de gráfico e executar operações matemáticas é obrigatório para tirar qualquer coisa desse nó.
> 
> Também recomendamos que você se familiarize com o conceito de [UVs](../../../../glossary/glossary.md), [amostragem de textura](../../../../glossary/glossary.md) e vetores.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Conectores de saída

</td>
<td style="border: 0;" valign="top">

### Exemplos

</td>
</tr>
</table>

## Parâmetros

|  |  |
| --- | --- |
| <b>Modo de cores</b> *Booleano* | Alterna entre uma imagem em tons de cinza e uma imagem colorida de saída. |
| <b>Função por pixel</b> *Flutuante/Flutuante4* | [gráfico de função Substance](../../../../function-graphs/the-function-graph/the-function-graph.md) avaliado por pixel na imagem de saída.   Use o conjunto de nós [Obter Precisão decimal2](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) para a variável <b>$pos</b> para acessar a posição [normalizada](../../../../glossary/glossary.md) do pixel atual. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Imagem de entrada #</b> *Tons de cinza/Cor* | Use um nó [Cor de exemplo](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) ou [Tons de cinza de amostra](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) para acessar os valores na entrada do índice especificado. |

## Conectores de saída

|  |  |
| --- | --- |
| <b>Saída</b> *Tons de cinza/Cor* |  |

## Exemplos

*Em breve.*
