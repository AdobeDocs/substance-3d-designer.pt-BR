---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-vertex-processor.html"
breadcrumb-title: ''
description: Use o nó Processador de vértice de caminhos para transformar e manipular vértices de caminho com opções avançadas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Vertex Processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Processador de vértice de caminhos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 1%

---


# Processador de vértice de caminhos

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](paths-vertex-processor.resources/paths-vertex-processor-icon.png "Ícone de nó")

<b>Ferramentas de Spline e Caminho </b> > Ferramentas de Caminho

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Aplica uma transformação na posição dos vértices dos <b>Caminhos</b> de entrada.

O nó deve ser usado da seguinte maneira:

1. Editar a função de parâmetro <b>Função por vértice </b>;
1. Use os nós <b>Get Float2</b> para adquirir; as variáveis *vertex.pos*, *prev.pos* e/ou *next.pos*
1. Realize algumas operações nesses valores (por exemplo, multiplique-as para dimensionar os caminhos);
1. Defina o resultado do seu cálculo como saída.

</td>
</tr>
</table>

Defina os <b>Vértices anteriores acessados</b> e os <b>Próximos vértices acessados</b> apropriados antes de consultar *prev.pos* ou *next.pos*\
Você também pode adicionar imagens de entrada e obtê-las como amostra da função. Você deve primeiro conectar uma entrada para poder fazer uma amostra da função. (Cuidado, a primeira entrada é *Imagem 1*!)\
Você também pode acessar as variáveis *prev[2].pos* (Float2), *next[2].pos* (Float2), *vertex.corner* (bool) e *path.id* (float).

>[!TIP]
>
> Para usuários avançados, a [Especificação de formato de caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md) explica como os dados dos caminhos são codificados em imagens coloridas e fornece dicas para manipular esses dados diretamente.

>[!NOTE]
>
> Consulte também [Processador de vértice de caminhos simples](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor-1/paths-vertex-processor-simple.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Caminhos</b> <i>Cor</i> | Uma lista de caminhos de segmentos codificados. Conecte esta entrada ao resultado de uma [Máscara para Caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) ou a outro nó de processamento *Caminho*. |
| <b>Entrada #</b> <i>Cores/Tons de Cinza</i> | Entradas para imagens que devem ser amostradas na função de parâmetro <b>Função por vértice</b>. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Caminhos</b> <i>Cor</i> | Os caminhos transformados. Você pode usar [Visualizar Caminhos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md) para ter uma ideia do que o resultado representa, usar outro nó de processamento de Caminhos ou inseri-lo em um [Caminhos para Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md) para processá-lo posteriormente como Splines. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Vértices Anteriores Acessados</b> <i>Inteiro</i> | O uso desse parâmetro permitirá obter a posição do vértice anterior ao longo do caminho (*prev.pos*) e do vértice anterior (*prev[2].pos*) usando os nós <b>Get</b> na função de parâmetro <b>Função por vértice</b>. |
| <b>Próximos Vértices Acessados</b> <i>Inteiro</i> | O uso desse parâmetro permitirá obter a posição do vértice a seguir ao longo do caminho (*next.pos*) e do vértice a seguir (*next[2].pos*) usando os nós <b>Get</b> na função de parâmetro <b>Função por vértice</b>. |
| <b>Contagem de entrada de imagem</b> <i>Inteiro</i> | O número de conectores de entrada <b>de #</b> visíveis para conectar imagens que devem ser amostrados na função de parâmetro <b>Função por vértice</b>.<br>Depois de concluir a configuração de todas as amostras desejadas, você pode ocultar fixares não utilizados reduzindo o valor deste parâmetro de volta a 0. |
| <b>Função por vértice</b> <i>Flutuante2</i> | Função aplicada para cada vértice. É necessário retornar a nova posição de vértice.<br>Consulte a seção <b>Descrição</b> nesta página para obter orientações. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 2](paths-vertex-processor.resources/PathsVertexProcessor-Demo2.gif "Exemplo de nó 2")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
