---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/exposing-parameters-in-mdl-graphs.html"
breadcrumb-title: ''
description: Saiba como expor parâmetros em gráficos MDL para tornar materiais personalizáveis e reutilizáveis no Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Exposing parameters in MDL graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Expondo parâmetros em gráficos MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---


# Expondo parâmetros em gráficos MDL

Esta página explica o processo de exposição de parâmetros em gráficos MDL para que eles possam ser conectados a valores e texturas fornecidos por *outros nós* no gráfico ou por *fontes externas*.

![Estado exposto das entradas do nó](exposing-parameters-in-mdl-graphs.resources/exposing-parameters-in-mdl-graphs-01.png "Estado exposto das entradas do nó")

*Estado exposto das entradas do nó*

## Expondo entradas de nó

Na maioria dos casos, os *conectores de entrada* das propriedades de um nó podem ser expostos para que seu *valor seja definido por outros nós* no gráfico. Esta é uma parte *crítica* de qualquer fluxo de trabalho em gráficos MDL e deve ser bem compreendida.

Quando um nó é selecionado na <b>Exibição de gráfico</b>, suas propriedades são exibidas no painel <b>Propriedades</b>. A maioria das propriedades é listada com um conjunto de botões à direita de seu rótulo:

* **![](exposing-parameters-in-mdl-graphs.resources/exposing-parameters-in-mdl-graphs-02.png)Copie o valor para um novo nó e vincule-o a este parâmetro**: cria um *conector de entrada* para esta propriedade e conecta-o a um *novo nó* que gera o valor atual desta propriedade
* **![](exposing-parameters-in-mdl-graphs.resources/exposing-parameters-in-mdl-graphs-03.png)Criar um fixar de entrada para este parâmetro**: cria um *conector de entrada* para esta propriedade
* **![](exposing-parameters-in-mdl-graphs.resources/exposing-parameters-in-mdl-graphs-04.png)Redefine este parâmetro para seu valor padrão**: quando nenhum valor estiver conectado ao conector de entrada desta propriedade, redefine seu valor para o padrão

![](exposing-parameters-in-mdl-graphs.resources/exposing-parameters-in-mdl-graphs-05.gif)

*Manipulando entradas de nó*

Clicar em qualquer um dos dois primeiros botões resulta em um *conector de entrada digitado* sendo adicionado ao nó. As propriedades do nó reagem ao *status da conexão* deste conector:

* **Desconectado**: o parâmetro ainda pode ser ajustado no painel **Propriedades** e a entrada de valor neste painel é *aplicada*
* **Conectado**: o parâmetro não pode mais ser ajustado no painel **Propriedades**. A entrada de valor neste painel é *substituída* pelo valor recebido pelo *conector de entrada*. A propriedade não pode ser redefinida para seu valor padrão

O conector de entrada pode ser *removido* clicando novamente no botão **Criar um fixar de entrada para este parâmetro**. Nesse ponto, o valor da propriedade retorna ao valor definido no painel **Propriedades**.

![Parâmetros de nó expostos](exposing-parameters-in-mdl-graphs.resources/exposing-parameters-in-mdl-graphs-06.png "Parâmetros de nó expostos")

*Parâmetros de nó expostos*

## Expor as entradas do gráfico

No gráfico MDL, expor um parâmetro ao nível do gráfico - ou seja, para que apareça como um parâmetro de entrada de material MDL - é feito expondo o nó que gera o valor.

Os nós que podem ser expostos têm uma opção <b>Expor</b> em seu menu contextual. Na maioria dos casos, são nós que geram um valor ou dados, como coordenadas de flutuação, cor ou textura.

Opção ![”Expor” no menu contextual de um nó](exposing-parameters-in-mdl-graphs.resources/exposing-parameters-in-mdl-graphs-07.png "&quot;Opção Expor&quot; no menu contextual de um nó")

Opção *”Expor” no menu contextual de um nó*

O parâmetro exposto é configurado diretamente no *nó exposto*, não nas propriedades do gráfico. As propriedades dos parâmetros expostos são as seguintes:

* <b>Identificador</b>: o nome exclusivo deste parâmetro de entrada no gráfico atual
* <b>Valor padrão</b>: o valor padrão para este parâmetro. Também pode ser usado como uma *visualização* de como será o parâmetro de entrada no Designer. As propriedades <b>Nome para exibição</b>, <b>No Grupo</b> e <b>Intervalos</b> são usadas para a visualização mais precisa possível
* <b>Intervalos</b>:
  * *Intervalo flexível*: define o intervalo padrão do widget usado para exibir esse parâmetro; por exemplo, um controle deslizante. Esta propriedade existe apenas para fins de interface e valores além do intervalo flexível podem ser inseridos manualmente
  * *Intervalo rígido*: define o intervalo de valores aceitos para este parâmetro. Os valores abaixo do intervalo são fixados com o valor mínimo, enquanto os valores acima do intervalo são fixados com o valor máximo. Os valores de intervalo flexível e padrão do parâmetro são *ajustados automaticamente* para se ajustarem a esse intervalo.
* <b>Descrição</b>: a descrição do parâmetro
* <b>No grupo</b>: o grupo de parâmetros ao qual este parâmetro de entrada pertence. Se não estiver em branco, o parâmetro será exibido no Designer como parte de uma seção recolhível nomeada em homenagem ao grupo
* <b>Nome de exibição</b>: o nome do parâmetro exibido na interface
* <b>Oculto</b>: quando definido como Verdadeiro, o parâmetro não fica visível nas entradas do gráfico e nas propriedades do material MDL
* <b>Tipo de gama</b>: a gama que deve ser usada ao obter amostras de valores de uma textura conectada a este parâmetro
* <b>Visível por padrão</b>: define a visibilidade desse parâmetro em integrações MDL nos casos em que alguns parâmetros podem estar ocultos
* <b>Modificador de tipo</b>: define se o valor é uniforme ou variável. Quando definido como auto, o parâmetro herda essa propriedade de sua entrada (por exemplo, para um valor Float: uniforme quando conectado a um Float, variando quando conectado a uma textura)
* <b>Uso do Sampler</b>: o identificador do uso do parâmetro, que é usado para *conectar a textura apropriada* s quando várias saídas são conectadas a um material MDL de uma só vez. Por exemplo, ao conectar um [gráfico de Substance](../../compositing-graphs/substance-compositing-graphs.md) a um material MDL na exibição 3D, as texturas são conectadas às entradas corretas com base na correspondência de seus identificadores de uso.

>[!WARNING]
>
> Enquanto as entradas de gráfico são configuradas em um nível de *nó*, sua ordem é gerenciada no nível de *gráfico* na seção **Entrada de gráfico** das [propriedades de gráfico](../../mdl-graphs/creating-an-mdl-graph/creating-an-mdl-graph.md).

![Expondo nós em entradas de gráfico](exposing-parameters-in-mdl-graphs.resources/exposing-parameters-in-mdl-graphs-08.gif "Expondo nós em entradas de gráfico")

*Expondo nós em entradas de gráfico*
