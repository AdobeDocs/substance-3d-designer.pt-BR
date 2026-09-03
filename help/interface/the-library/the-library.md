---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/interface/the-library.html"
breadcrumb-title: ''
description: Use a Biblioteca no Substance 3D Designer para acessar e gerenciar predefinições de nó, materiais e conteúdo personalizado.
helpx_creative_field: ""
helpx_description: Designer > Interface > Library
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Biblioteca
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1043'
ht-degree: 0%

---


# A biblioteca

Esta página apresenta o painel da **Biblioteca** do Substance 3D Designer, seu layout e as ferramentas que ele oferece para pesquisa e filtragem de conteúdo.

![Biblioteca](the-library.resources/the-library-01.png "Biblioteca")

## Visão geral

O painel <b>Biblioteca</b> é um *gerenciador de recursos* de exibição dividida, onde você pode encontrar e reunir todos os seus *ativos* com os quais precisa trabalhar no seu gráfico.

Ele monitora *pastas* no disco rígido ou na rede, que são adicionadas à lista de [Caminhos observados da biblioteca](https://docs.substance3d.com/display/SDDOC/Project+Settings#ProjectSettings-proj-libraryLibrary) nas [Configurações do projeto](../../interface/preferences-window/project-settings/project-settings.md). Todas as alterações que ocorrem nessas pastas (adição, remoção e atualização de conteúdo) são *transitadas* para a <b>Biblioteca</b>.

>[!WARNING]
>
> **Sobre conteúdo personalizado**
> 
> Embora seus recursos personalizados sejam adicionados à **Biblioteca**, eles podem não estar visíveis devido às regras de filtragem definidas para as categorias existentes. Recomendamos que você crie seus próprios filtros organizados em pastas, para garantir que seu conteúdo possa ser encontrado de forma confiável ao trabalhar em seus projetos.\
> Consulte a seção [Gerenciando conteúdo e filtros personalizados](./managing-custom-content/managing-custom-content-and-filters.md) da documentação para obter mais informações.

A **Biblioteca** pode monitorar todos os ativos que têm suporte dos [Recursos](../../resources/resources.md):

* Gráficos de [Pacotes de Substance](../../getting-started/overview/overview.md) (SBS) e [Arquivos de Substance](../../getting-started/overview/overview.md) (SBSAR)
* [Imagens de bitmap](../../resources/bitmap-resource/bitmap-resource.md)
* [Imagens vetoriais](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* [Gráficos de função](../../function-graphs/function-graphs.md)
* [Arquivos AxF](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md)
* [Fontes](../../resources/font-resource/font-resource.md)
* [Cenas 3D](../../resources/3d-scene-resource/3d-scene-resource.md)

O painel está dividido em duas partes principais:

* A seção **Categorias** à esquerda
* A seção **Conteúdo** à direita

## Categorias

Localizada à esquerda do painel <b>Biblioteca </b>, a seção <b>Categoria</b> contém todos os ativos *categorias* (por exemplo, pastas) e *filtros*, como uma exibição de árvore.\
Você pode clicar em qualquer item neste modo de exibição de árvore para exibir seu conteúdo, juntamente com o conteúdo de *todos os seus itens filho*.

### As categorias

As categorias e filtros padrão contêm todos os ativos enviados com o Designer. Eles não podem ser editados ou removidos.\
As categorias padrão incluem:

* Favoritos: reúne todos os ativos que você sinalizou como “Favoritos”
* [Itens de gráfico](../../interface/the-graph-view/graph-items/graph-items.md): lista objetos especiais para organizar gráficos
* [Nós atômicos](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md): lista nós atômicos para [gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md)
* [Nós FX-Map](../../function-graphs/fxmaps/fxmaps.md): inclui nós específicos para gráficos computados por [nós FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)
* [Nós de função](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/atomic-function-nodes.md): lista nós atômicos para [gráficos de função](../../function-graphs/function-graphs.md)
* [Geradores de textura](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/texture-generators.md): contêm nós que representam [gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md) que geram conteúdo de forma autônoma
* [Filtros](../../compositing-graphs/nodes-reference-for-com/node-library/filters/filters.md): contém nós que representam [gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md) que modificam uma entrada
* [Ferramentas de spline e caminhos](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-paths-tools.md): o catálogo de nós [Spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-tools.md) e [Paths](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-tools.md)
* [Função SDF](../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions): inclui nós para criação de Funções SDF 3D, a serem usados com os nós [respingo de forma v2](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md) e [visualizador 3D](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.md)
* [Funções](../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md): inclui nós que representam [gráficos de função](../../function-graphs/the-function-graph/the-function-graph.md)
* [exibição 3D](../3d-view/3d-view.md): oferece conteúdo relacionado a mapas usados para iluminação baseada em imagem em uma cena 3D, como na [exibição 3D](../../interface/3d-view/3d-view.md), como mapas de ambiente e nós para a criação de mapas de ambiente
* Materiais PBR: materiais pré-fabricados que podem ser usados como espaços reservados para testar outros nós, “receitas” ou uma configuração de espaço de trabalho personalizada. Para saber mais sobre a criação de materiais, recomendamos dar uma olhada em nossas [amostras de materiais](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md) dedicadas.
* [Valores](../../compositing-graphs/nodes-reference-for-com/node-library/values/constant.md): nós para gerar valores simples em gráficos de Substance.

## Conteúdo

O conteúdo da <b>Biblioteca</b> é exibido como *miniaturas rotuladas*. Essas miniaturas terão um aspecto diferente dependendo dos seguintes fatores:

* [gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md) em arquivos [SBS](../../getting-started/overview/overview.md) e [SBSAR](../../getting-started/overview/overview.md) são representados por sua *primeira saída* ou por seu *ícone personalizado* se algum tiver sido definido pelo autor do gráfico
* [Bitmaps](../../resources/bitmap-resource/bitmap-resource.md) e [gráficos vetoriais (SVG)](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) são representados por uma *renderização em miniatura* do próprio bitmap
* [Cenas 3D](../../resources/3d-scene-resource/3d-scene-resource.md), [Gráficos de função](../../function-graphs/the-function-graph/the-function-graph.md), [fontes](../../resources/font-resource/font-resource.md) e arquivos [AxF](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md) são representados por *ícones genéricos* para cada tipo

>[!WARNING]
>
> **No caso de problemas de miniaturas**
> 
> Nossa etapa de solução de problemas recomendada para quaisquer problemas relacionados às miniaturas da biblioteca (imagem incorreta, renderização travada no ícone de atualização etc.) é acionar manualmente uma *atualização de miniaturas*.\
> Para fazer isso, use o botão **Reconstruir miniaturas** na seção [Biblioteca](../../interface/preferences-window/preferences-window.md) da [janela Preferências](../../interface/preferences-window/preferences-window.md).

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Uso de um ativo da biblioteca

Para usar um ativo da biblioteca, *arraste-o e solte* no local desejado.\
Você pode selecionar *vários* itens na seção <b>Conteúdo</b> mantendo a tecla <b>Ctrl</b> pressionada enquanto clica nos itens. Nesse caso, a operação de arrastar e soltar colocará nós no gráfico para a *seleção inteira*.

</td>
<td width="41.67%" style="border: 0;" valign="top">

![Descartando um nó da Biblioteca](the-library.resources/the-library-02.gif "Descartando um nó da Biblioteca")

</td>
</tr>
</table>

### Pesquisar um ativo por nome

A barra <b>Pesquisar</b>, localizada na parte superior esquerda da seção <b>Conteúdo</b>, permite pesquisar *qualquer ativo por nome*. Ao procurar conteúdo dessa maneira, a seleção atual na seção <b>Categorias</b> é ignorada e o *conteúdo inteiro* da <b>Biblioteca</b> é pesquisado.\
Você pode filtrar os resultados da pesquisa por *tipo de gráfico*, usando o ícone ![](the-library.resources/the-library-03.png) <b>Filtrar por...</b> ao lado da barra <b>Pesquisa</b>.

>[!NOTE]
>
> A barra de pesquisa levará em consideração o nome do ativo que você está procurando, mas também as *marcas* que o ativo pode conter ou a *categoria* à qual ele pertence.\
> Por exemplo, digitar &#39;*Normal*&#39; listará todos os ativos que podem ser usados para gerar ou modificar um mapa normal. Esta é uma boa maneira de descobrir novos nós e, portanto, novas possibilidades!

![Pesquisa de ativos na Biblioteca](the-library.resources/the-library-04.png "Pesquisa de ativos na Biblioteca")

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Visualização de ativos da biblioteca

Usando o botão suspenso ![](the-library.resources/the-library-05.png) <b>Modo de Exibição</b>, você pode selecionar o tamanho de exibição para itens de conteúdo.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Modo de exibição de ativos da biblioteca](the-library.resources/the-library-06.png "Modo de exibição de ativos da biblioteca")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

O botão ![](the-library.resources/the-library-07.png) **Alternar Rótulos** permite exibir ou ocultar os rótulos dos nós.

</td>
<td style="border: 0;" valign="top">

![Alternar rótulo](the-library.resources/the-library-08.png "Alternar rótulo")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Ao colocar o cursor em um item de conteúdo, uma dica de ferramenta aparecerá após um curto período de tempo exibindo uma *descrição* do item, se o autor tiver fornecido uma.\
*Clique com o botão direito do mouse* no item para exibir informações adicionais, incluindo um caminho para o arquivo de origem desse item.

</td>
<td style="border: 0;" valign="top">

![Dica de ferramenta de informações do ativo](the-library.resources/the-library-09.png "Dica de ferramenta de informações do ativo")

</td>
</tr>
</table>

>[!NOTE]
>
> Para [nós de instância](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md), ou seja, nós não atômicos, este caminho é um *hiperlink* que exibirá o arquivo no navegador de arquivos do sistema.\
> Os nós atômicos usam um caminho com alias especial (por exemplo, `graphatomic://`, `structure://`, ...) que não podem ser clicadas porque apontam para uma biblioteca interna.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Favoritos

Você pode adicionar qualquer item da seção <b>Conteúdo</b> à lista <b>Favoritos</b> usando o botão ![](the-library.resources/the-library-10.png) <b>Adicionar a Favoritos</b>. O botão também permite *remover* conteúdo desta lista se já estiver adicionado.\
Quando o conteúdo é adicionado a esta lista, ele fica disponível na categoria <b>Favoritos</b> da <b>Biblioteca</b> e será exibido na *parte superior* da lista de menus <b>Nó</b> ao procurar um nó no gráfico, desde que os termos de pesquisa correspondam a ele.

</td>
<td style="border: 0;" valign="top">

![Favoritos na Biblioteca](the-library.resources/the-library-11.png "Favoritos na Biblioteca")

</td>
</tr>
</table>
