---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps.html"
breadcrumb-title: ''
description: Saiba como usar FXMaps no Substance 3D Designer para aplicar gráficos de função a texturas para geração de padrões de procedimento.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: FXMaps
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---


# FXMaps

**O nó FX-Map permite a criação de imagens de procedimento**. É um dos recursos mais poderosos da tecnologia Substance.

Um FX-Map representa um tipo especial de gráfico, conhecido como Cadeia de Markov. Cadeias de Markov representam um processo básico simples: repetidamente replicando e subdividindo uma imagem repetidamente. Em cada etapa, uma imagem pode ser girada, traduzida e mesclada à vontade. Os resultados podem variar de padrões simples a ruídos complexos. Os FX-Maps são a base para muitos dos Substance de exemplo instalados com o Substance 3D Designer.

## Criar gráficos FX-Map

Se quiser ver um gráfico FX-Map, basta adicionar um [nó FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) a um [gráfico de Substance](../../compositing-graphs/substance-compositing-graphs.md). Em seguida, clique com o botão direito do mouse no nó e pressione CMD + E (OS X) ou CTRL + E (Windows) para abrir seu gráfico. Esse gráfico FX-Map aparecerá em uma nova guia no painel Gráficos. Para alternar entre o gráfico e o gráfico de Substance, clique na guia.

## Para que servem os FX-Maps?

Os usos mais comuns dos FX-Maps são a criação de padrões repetitivos, como listras e tijolos, e ruídos, como o de Perlin, Browniano e Gaussiano. Os ruídos são particularmente úteis na criação de texturas orgânicas de aparência natural, como dirt, dust, concretos, superfícies de pedra, respingos de líquidos e assim por diante.

Gráficos FX-Map não funcionam da mesma forma que os gráficos de Substance: Em gráficos de Substance, cada nó é independente e não tem conhecimento de sua posição no gráfico geral, nem se importa de onde seus dados de imagem vêm ou para onde estão indo.

Examinaremos cada um dos três nós do gráfico FX-Map em mais detalhes no próximo capítulo, mas, resumidamente, cada nó do FX-Map oferece uma das três operações:

### Quadrante

Isso divide a imagem nessa etapa do gráfico em quatro quadrantes. Este é o tipo de nó mais comum. Uma cadeia de nós do Quadrante pode criar imagens muito complexas, bem como padrões complexos.

Na verdade, os nós do Quadrante representam um nível, ou **oitava**, em um gráfico de árvore quádrupla. Os gráficos FX-Map ocultam essa estrutura em árvore, representando cada nível na árvore com um único Quadrante: cada vez que você conecta um nó de Quadrante a outro, você está realmente criando um nível de árvore completo.

A razão para esta técnica de “fraude” é remover a necessidade de representar cada nó em cada nível de uma árvore individualmente: depois de apenas quatro camadas de profundidade, você precisaria usar 4 x 4 x 4 x 4 nós, que são 256 nós individuais! Em vez disso, cada nó do quadrante “sabe” em que nível está na árvore e gera suas imagens adequadamente.

Isso provavelmente não fará muito sentido para muitos leitores, mas entraremos em mais detalhes em breve.

### Iterar

Repete a imagem passada para o conector direito sobre a imagem passada para o conector esquerdo pelo número definido de iterações.

Este nó é mais frequentemente usado com um ou mais gráficos de Funções dinâmicas para mover ou girar a imagem de entrada de alguma forma em cada iteração.

### Alterar

Isso pega duas entradas e simplesmente alterna entre uma e outra, conforme definido pela configuração do Seletor. Assim como no nó Iterar, a configuração Seletor é frequentemente escolhida por uma Função dinâmica.

## Variáveis de Sistema FX-Maps

Os FX-Maps são compatíveis com variáveis de sistema. Essas variáveis sempre começam com um símbolo de dólar (”$”) e são as seguintes:

| Nome | Particularidade | Tipo de dados | Finalidade |
| --- | --- | --- | --- |
| $time | - | float1 | Essa variável retorna o tempo em segundos desde que o mecanismo de renderização de Substance foi iniciado.É ideal para Substance que precisam ser animados de acordo com o tempo. (E.g. os ponteiros de um relógio.)Em alguns aplicativos, incluindo o Substance Player, um Substance que usa $time fará com que uma linha do tempo apareça na interface do usuário. |
| $profundidade | - | float1 | Retorna o número de oitava (nível) do nó FX-Map. Isso permite que um nó modifique seu comportamento de acordo com o nível na árvore quádrupla que representa. |
| $depthpow2 | - | float1 | Como acima, mas retorna 2 elevado à potência do número de oitava (nível). Esse é um valor auxiliar que é útil para alguns cálculos comuns. |
| $number | Iterar somente nós | float1 | Retorna o número do padrão desenhado. Isso pode ser acessado pelos gráficos de Função dinâmica que controlam um nó Iterar para modificar seu comportamento em cada etapa de iteração. (Observe que $number começa a contar de 0, não de 1.) |
| $size | - | float2 | Retorna o tamanho do nó atual (em pixels). |
| $sizelog2 | - | float2 | Como acima, mas retorna o tamanho como valores power-of-2 (por exemplo: para a imagem 2048\*2048, $sizelog2 retorna 11). |
| $pos | Somente nós do quadrante | float2 | Retorna a posição de nascimento do padrão. O resultado é sempre um valor entre 0 e 1. |
