---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/values-in-substance-compositing-graphs.html"
breadcrumb-title: ''
description: Saiba mais sobre tipos de valor e manipulação de dados em gráficos de composição de Substance para criação eficaz de materiais.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Values in Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Valores em gráficos do Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 46563ec789547cc1add76655dbad02f5099927a6
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 2%

---


# Valores em gráficos do Substance

Desde a Introdução do [Mecanismo do Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html) v7 na versão 2019.1.0, agora é possível processar valores no gráfico de Substance e[não apenas em funções](../../function-graphs/function-graphs.md). Dados de valor são os mesmos dados usados em Funções ( Inteiros, Precisões decimais e Booleanos, entre outros), tornando-os distintamente diferentes dos dados de imagem Colorida ou em Tons de Cinza, que representam valores de pixel para uma imagem inteira. Especificamente, ao mencionar dados de Valores, isso significa *Inteiro 1, Inteiro 2, Inteiro 3 e Inteiro 4, Precisão decimal 1, Precisão decimal 2, Precisão decimal 3 e Precisão decimal 4 e Booleano*. Cada um tem um código de cores distinto, e na maioria das vezes não são trocados entre si.

Existem alguns casos de uso para isso, como:

* Retornando e processando dados que não são de imagem, como propriedades de material de valor único ou metadados extras. Por exemplo, o valor IOR de um material.
* Otimizando cálculos de gráfico que não precisam ser calculados por pixel (uma alternativa ao [Processador de pixels](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)). Por exemplo, uma cor sólida aleatória.
* Vinculando propriedades de um nó a outro processando dados de imagem em valores. Por exemplo, os valores Mínimo e Máximo de uma imagem para ajustar Níveis.

## Novos nós e entradas de valor

Dois novos nós atômicos funcionam com valores:

|  |  |
| --- | --- |
| <div><img alt="ícone do nó do processador de valor" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="values-in-substance-compositing-graphs.resources/valueprocessor.png" title="ícone do nó do processador de valor" width="100px"/></div>  <b>[Processador de valor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)</b> | O [Processador de valor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md) usa Qualquer número de Entradas de Tons de Cinza ou Cores e permite retornar um único Valor de cálculos com base nessas entradas. |
| <div><img alt="Ícone do nó Entrada de valor" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="values-in-substance-compositing-graphs.resources/inputnumeric.png" title="Ícone do nó Entrada de valor" width="100px"/></div>  **[Entrada de valor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)** | A [Entrada de valor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)permite criar um slot de entrada em subgráficos que são explicitamente definidos como um valor. |

Além disso, outros nós lidam com eles de uma maneira específica:

O [Nó de saída](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) se ajusta automaticamente para se tornar uma Saída de valor se você conectar uma conexão de valor a ela, assim como fazia antes com Tons de cinza e Cores.

![Nó do valor de saída](values-in-substance-compositing-graphs.resources/values-output.gif "Nó do valor de saída"){width="512px"}

Há uma nova guia em cada nó único ([Atômico](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)e [Biblioteca](../../compositing-graphs/nodes-reference-for-com/node-library/node-library.md)/Instância) que permite definir entradas de Valor.

![Adicionando valores de entrada no nó](values-in-substance-compositing-graphs.resources/values-inputs.gif "Adicionando valores de entrada no nó")

## Trabalhar com valores

O uso de valores é um pouco diferente do trabalho de gráfico de Substance regular:

Conexões de valor só podem ser feitas de um [Processador de valor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md), de uma [Entrada de Valor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) ou de um [Subgráfico](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md). Isso realmente significa que um Processador de valor é a única maneira de criar uma conexão de Valor do zero, não há nó “Valor estático” ou qualquer coisa semelhante. Em vez disso, crie uma Processador de valor, posicione um Valor estático e defina-o como saída para obter o mesmo resultado.

Processador de valor só pode retornar um único Valor. Se você quiser retornar vários Valores, ou conjuntos ou Grupos de Valores, terá que criar um [Subgráfico](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md).

Para realçar onde os Valores são expostos ou em uso, qualquer Nó que tenha Entradas de Valor ou Saídas de Valor é realçado com uma borda amarela espessa:

![Trabalhando com valores](values-in-substance-compositing-graphs.resources/yellowhighlight.png "Trabalhando com valores")
