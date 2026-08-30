---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/warnings-in-substance-compositing-graphs.html"
breadcrumb-title: ''
description: Entenda os avisos nos gráficos de composição de Substance e saiba como resolver problemas e erros comuns.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Warnings in Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Avisos em gráficos do Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 1%

---


# Avisos em gráficos do Substance

Esta página lista mensagens de erros e avisos que podem ser disparados por [gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md) no Substance 3D Designer e oferece etapas comuns de solução de problemas para cada um.

Os avisos são exibidos na dica de ferramenta do ícone de aviso para o recurso de gráfico no painel [Explorador](../../interface/the-explorer-window/the-explorer-window.md), bem como no canto inferior esquerdo da [Exibição de gráfico](../../interface/the-graph-view/the-graph-view.md) se o gráfico estiver carregado.

## ![(erro)](warnings-in-substance-compositing-graphs.resources/error.svg) Nenhum nó de saída definido

O gráfico não tem um nó [Saída](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md).

**![(tick)](warnings-in-substance-compositing-graphs.resources/check.svg) Solução**

Adicione um ou mais nós [Saída](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) ao gráfico e conecte a saída do último nó em um fluxo a ele.

>[!NOTE]
>
> Os modelos de gráfico disponíveis por meio da caixa de diálogo [Novo gráfico](../creating-compositing-gra/creating-a-substance-compositing-graph.md) têm nós de saída predefinidos prontos para serem usados.

![Corrigir o aviso &#39;Nenhum nó de saída definido&#39;](warnings-in-substance-compositing-graphs.resources/warnings-comp-output.gif "Corrigir o aviso &#39;Nenhum nó de saída definido&#39;"){width="512px"}

### ![(erro)](warnings-in-substance-compositing-graphs.resources/error.svg) A função do parâmetro *[x]* possui alguns avisos

O [gráfico de função](../../function-graphs/function-graphs.md) aplicado ao parâmetro especificado do nó especificado tem pelo menos um aviso.\
O parâmetro node é especificado entre colchetes após o rótulo do nó, seguindo o modelo Node[Parameter].

E.g. Cor uniforme[Cor De Saída], Processador de pixels[Função Por Pixel]

**![(tick)](warnings-in-substance-compositing-graphs.resources/check.svg) Solução**

Localize o nó que emite o aviso por seu rótulo e emblema de aviso na [Exibição de gráfico](../../interface/the-graph-view/the-graph-view.md) e selecione-o para exibir suas propriedades no painel [Propriedades](../../interface/properties/properties.md). Localize o parâmetro que emite o aviso e abra sua função clicando no botão **Editar função**.

Em seguida, avalie o(s) aviso(s) listado(s) no canto inferior esquerdo da exibição Gráfico e resolva os problemas. Você pode consultar a página [Avisos nos gráficos de função](../../function-graphs/warnings-function-graphs/warnings-in-function-graphs.md) para obter avisos de solução de problemas relatados nos gráficos de função.

![Aviso de correção de &#39;A função de parâmetro tem alguns avisos&#39;](warnings-in-substance-compositing-graphs.resources/warnings-comp-param-function.gif "Aviso de correção de &#39;A função de parâmetro tem alguns avisos&#39;")

### ![(erro)](warnings-in-substance-compositing-graphs.resources/error.svg) Os dados referenciados possuem alguns avisos

O recurso referenciado por um nó tem um ou mais avisos. Aqui estão alguns nós que fazem referência a um recurso:

* Um nó [instância de gráfico](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) faz referência a um gráfico
* Um nó [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) faz referência a um [recurso de Bitmap](../../resources/bitmap-resource/bitmap-resource.md)
* Um nó [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) faz referência a um recurso [SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* Um nó [Texto](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) faz referência a um [recurso de fonte](../../resources/font-resource/font-resource.md)

**![(tick)](warnings-in-substance-compositing-graphs.resources/check.svg) Solução**

No painel [Explorador](../../interface/the-explorer-window/the-explorer-window.md), localize o recurso referenciado e solucione todos os avisos gerados pelo recurso:

* Para gráficos, consulte outros itens nesta página
* Para qualquer outro tipo de recurso, consulte a página [Avisos de dependências](../../resources/warnings-from-dep/warnings-from-dependencies.md)

![Corrigir o aviso &#39;Dados referenciados têm alguns avisos&#39;](warnings-in-substance-compositing-graphs.resources/warnings-comp-referenced-data.gif "Corrigir o aviso &#39;Dados referenciados têm alguns avisos&#39;")

### ![(erro)](warnings-in-substance-compositing-graphs.resources/error.svg) Recurso de referência não encontrado

O recurso referenciado por um nó não foi encontrado no caminho salvo no arquivo do [Substance 3D](https://www.adobe.com/products/substance3d/3d-augmented-reality.html) (SBS). Aqui estão alguns nós que fazem referência a um recurso:

* Um nó [instância de gráfico](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) faz referência a um gráfico
* Um nó [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) faz referência a um [recurso de Bitmap](../../resources/bitmap-resource/bitmap-resource.md)
* Um nó [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) faz referência a um recurso [SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* Um nó [Texto](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) faz referência a um [recurso de fonte](../../resources/font-resource/font-resource.md)

**![(tick)](warnings-in-substance-compositing-graphs.resources/check.svg) Solução**

Para nós de [instância de gráfico](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)

Verifique se o gráfico de origem existe no pacote localizado no caminho salvo no atributo **Pacote**.\
Caso contrário, exclua o nó da instância e substitua-o por um nó de instância que faça referência a um pacote válido. Como alternativa, você pode recriar o pacote e o gráfico referenciados pelo nó da instância e recarregar o pacote do host clicando em RMB nele no painel [Explorer](../../interface/the-explorer-window/the-explorer-window.md) e selecionando a opção **Recarregar** no menu contextual.

Para nós [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md), [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md) ou [Texto](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)

Localize os recursos referenciados no painel do Explorer e verifique se eles existem no local salvo no atributo **Caminho do Arquivo**.\
Caso contrário, clique em RMB no item de recurso no Explorer e selecione a opção **Realocar...** no menu contextual para definir um novo arquivo de destino válido para esse recurso.

![Corrigir aviso &#39;Recurso de referência não encontrado&#39;](warnings-in-substance-compositing-graphs.resources/warnings-comp-referenced-resource.gif "Corrigir aviso &#39;Recurso de referência não encontrado&#39;")

### ![(erro)](warnings-in-substance-compositing-graphs.resources/error.svg) O nó de texto usa uma fonte inválida

Um nó [Texto](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) faz referência a uma fonte que não pode ser carregada ou analisada corretamente.

<b>![(tick)](warnings-in-substance-compositing-graphs.resources/check.svg) Solução</b>

Selecione o nó [Texto](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) e anote o valor de sua propriedade <b>Fonte</b>. Localize o arquivo de origem dessa fonte no sistema e verifique se ela está *íntegra*. Por exemplo, use-a em outro aplicativo, como um editor de texto. Substitua a fonte por um arquivo de fonte íntegro, conforme necessário, ou mude o nó de Texto para outra fonte.
