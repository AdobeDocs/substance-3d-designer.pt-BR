---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/function-graphs/fxmaps/the-iterate-node.html"
breadcrumb-title: ''
description: Use o nó Iterar em FXMaps para criar padrões repetitivos e variações processuais em seus materiais.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > The Iterate Node
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: O nó Iterar
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---


# O nó Iterar

O nó Iterar permite multiplicar as imagens de um nó Quadrante e é essencialmente um nó “repetidor”. Um nó Quadrante em uma profundidade de 1 normalmente produziria 4 quadrantes. O nó Iterar permite que você repita suas imagens de saída quantas vezes desejar, com cada conjunto de repetições tratadas separadamente.

O nó Iterar não tem outras propriedades além do parâmetro “How repetitions do you want?”. O resultado é que as novas imagens são, por padrão, simplesmente sobrepostas e mescladas com as produzidas pelo nó Quadrante.

O nó Iterar repete a imagem de entrada recebida. O número de repetições é definido por sua propriedade Iteração:

A chave para usar o nó Iterar é que quaisquer funções dinâmicas anexadas a cada imagem repetida também serão processadas. Isso significa que cada repetição pode ter seu próprio conjunto de ajustes exclusivos. Você pode usar a propriedade Distribuição aleatória do nó Iterar para modificar como isso funciona. Você também pode acessar a variável de sistema *$number* em suas funções dinâmicas para determinar qual repetição está sendo renderizada no momento e modificar o resultado da função adequadamente.

Por exemplo: se você aplicar uma rotação aleatória a cada imagem em um nó Quadrante e, em seguida, alimentar a saída desse nó Quadrante para a entrada ativa de um nó Iteração, cada uma das imagens repetidas também terá sua própria rotação aleatória.

Todos os mesmos recursos dinâmicos disponíveis no nó Quadrante também se aplicam às imagens repetidas produzidas pelo nó Iterar. É como se o nó duplicasse o nó Quadrante no mesmo nível, em vez de adicionar outro nível de profundidade.

## O conector de passagem

Cada nó Iterate tem dois conectores ao longo de sua base. O conector esquerdo é um conector de passagem. A imagem que ele recebe é passada diretamente para o conector de saída do nó, onde é mesclada com todas as imagens repetidas:

Observe que a imagem de passagem sempre passa intacta, independentemente da configuração do parâmetro de Iteração.

![](the-iterate-node.resources/iterate.jpg)
