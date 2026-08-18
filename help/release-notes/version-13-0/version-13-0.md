---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/release-notes/version-13-0.html"
breadcrumb-title: ''
description: Consulte as notas de versão do Substance 3D Designer versão 13.0 para saber mais sobre novos nós, Substance Engine 9.0 e nós do portal.
helpx_creative_field: ""
helpx_description: Designer > Release Notes > Version 13.0
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Versão 13.0
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '1671'
ht-degree: 2%

---


# Versão 13.0

Esta versão 13.0.0 do Substance 3D Designer traz muito amor aos artistas materiais, com uma enorme quantidade de novos nós, o Substance Engine 9.0 introduzindo loops pela primeira vez e com uma grande adição ao gráfico: o nó portal. E para agradar mais usuários, apresentamos uma nova tela inicial e fornecemos idiomas adicionais.

Como mencionado na versão anterior, esta versão não é mais compatível com gráficos de modelo de Substance: isso significa que você não pode mais abrir, editar ou exportar esses gráficos no Designer. Você pode encontrar todos os motivos pelos quais tomamos esta decisão nesta [postagem](https://community.adobe.com/t5/substance-3d-designer-discussions/substance-model-graphs-end-of-life/td-p/13693731)em nosso fórum da comunidade.

*Data de lançamento: 6 de junho de 2023*

![Material usando caminhos](../../assets/Paths2.png "Material usando caminhos")

*Ilustração de [Celine Dameron](https://www.artstation.com/cline)*

## Novo conteúdo

Esta versão 13.0 traz muito conteúdo novo. Você encontrará principalmente duas novas coleções de nós: Ferramentas de linha flexível e ferramentas de caminho.

* As [Ferramentas de linha flexível](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-tools.md) são uma coleção de nós para gerar e ajustar splines, bem como usá-las para mapear, espalhar ou deformar imagens.
* As [ferramentas de caminho](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-tools.md) são outro conjunto de nós para extrair, na forma de uma lista de segmentos, contornos de uma máscara e depois editá-los e aprimorá-los.

Todos esses nós oferecerão muitas possibilidades e terão, com certeza, muitas aplicações criativas. Confira a seção sobre [trabalhando com Caminhos e Ferramentas de linha flexível](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/working-with-path-and-spl/working-with-path-and-spline-tools.md) para obter um tour pelos conceitos importantes a serem compreendidos para se familiarizar com esse conjunto de ferramentas.

![Material que usa splines](../../assets/Splines.png "Material que usa splines")

*Ilustração de [Louise Melin](https://www.artstation.com/troglodette)*

### Ferramentas de linha flexível

Os novos nós dedicados às splines podem ser divididos em quatro categorias:

#### Criar

A primeira categoria é, naturalmente, a que gera splines:

* [Spline Cubic](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-cubic/spline-cubic.md): de dois pontos e duas tangentes;
* [Poli Quadrático de Spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic/spline-poly-quadratic.md): de um conjunto de pontos;
* [Círculo de spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-circle/spline-circle.md): seguindo uma forma de circulare.

Você também pode criar <b>pontes </b>entre splines para ter um conjunto completo de splines entre [2 splines](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-2-splines/spline-bridge-2-splines.md) ou [N splines](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-list/spline-bridge-list.md).

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Cúbico De Spline](../../assets/SplineCubic-Demo.gif "Cúbico De Spline")

</td>
<td style="border: 0;" valign="top">

![Poli Quadrático de Spline](../../assets/SplinePolyQuadratic-Demo.gif "Poli Quadrático de Spline")

</td>
<td style="border: 0;" valign="top">

![Círculo com Spline](../../assets/SplineCircle-Demo.gif "Círculo com Spline")

</td>
<td style="border: 0;" valign="top">

![Lista de pontes de spline](../../assets/SplineBridge-List_Demo.gif "Lista de pontes de spline")

</td>
</tr>
</table>

#### Montar

Em alguns casos, será necessário tratar várias splines como uma entidade única, portanto, são necessárias ferramentas para gerenciar um conjunto de splines. A [Lista de Mesclagem de Spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-merge-list/spline-merge-list.md) permite mesclar todas as splines em uma única, conectando os extremos na ordem. O nó [Anexar Spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-append/spline-append.md) permite anexar uma lista de splines a outra lista e, graças ao nó [Seleção de Spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-select/spline-select.md), você pode filtrar e selecionar splines específicas de uma determinada lista.

#### Modificar

Também fornecemos ferramentas para retrabalhar e ajustar seus splines. Você encontrará um nó para aplicar uma [transformação 2D](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-2d-transform/spline-2d-transform.md), como uma rotação, tradução, escala e outro para [distorcer](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-warp/spline-warp.md)<b> </b>a forma e dois outros nós para modificar o [thickness](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-sample-thickness/spline-sample-thickness.md)<b> </b>ou o [height](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-sample-height/spline-sample-height.md) das splines.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Transformação 2D De Spline](../../assets/Spline2DTransform-Demo1.gif "Transformação 2D De Spline")

</td>
<td style="border: 0;" valign="top">

![Distorção de spline](../../assets/SplineWarp-Demo.gif "Distorção de spline")

</td>
<td style="border: 0;" valign="top">

![Thickness de Exemplo de Spline](../../assets/SplineSampleThickness-Demo.gif "Thickness de Exemplo de Spline")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

#### Renderização

A última categoria é aquela para criar a forma ou o padrão final com base nos splines. A primeira ideia que lhe vem à mente será repetir uma determinada forma ao longo da spline: o nó [Dispersão na spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-on-spline-color/scatter-on-spline-color.md) permite fazer isso, com muitos parâmetros para controlar perfeitamente a distribuição (rotação, escala, deslocamento, cores, máscaras etc.).

Graças ao nó [Preenchimento de spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-fill/spline-fill.md)<b> </b>, você pode criar facilmente um padrão a partir de uma spline fechada. E se você quiser mapear qualquer textura nos splines, com alto grau de controle e precisão, o nó [Mapeador de spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-color/spline-mapper-color.md) foi criado para você!

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Dispersão em Escala de Cinza de Spline](../../assets/ScatterOnSplineGrayscale-Demo.gif "Dispersão em Escala de Cinza de Spline")

</td>
<td style="border: 0;" valign="top">

![Preenchimento de spline](../../assets/SplineFill-Demo.gif "Preenchimento de spline")

</td>
<td style="border: 0;" valign="top">

![Cor do mapeador de spline](../../assets/SplineMapperColor-Demo.gif "Cor do mapeador de spline")

</td>
<td style="border: 0;" valign="top">

![Mapeador de fluxo de spline](../../assets/SplineFlowMapper-Demo.gif "Mapeador de fluxo de spline")

</td>
</tr>
</table>

### Ferramentas de caminho

O nó [Máscara para caminhos](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md) permite extrair a borda de um padrão em tons de cinza, na forma de uma lista de segmentos.

Em seguida, você pode processar esses caminhos com os nós [Transformação de caminho 2D](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-2d-transform/path-2d-transform.md) ou [Distorção de caminhos](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-warp/paths-warp.md) para ajustar de acordo com suas necessidades.  Graças ao nó [Caminhos para spline](../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md), você pode converter seu Caminho em um Spline e, portanto, aproveitar todos os nós dedicados a splines mencionados anteriormente, como dispersão.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Mascarar para caminhos](../../assets/MaskToPaths-Demo2.gif "Mascarar para caminhos")

</td>
<td style="border: 0;" valign="top">

![Mascarar para Caminhos 2](../../assets/MaskToPaths-Demo1.gif "Mascarar para Caminhos 2")

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

E para ajudá-lo a aprender todos esses novos nós, publicamos dois novos tutoriais:

* [Introdução aos nós de spline](https://www.adobe.com/go/designer-tutorial-splines)
* [Introdução aos nós Caminho](https://www.adobe.com/go/designer-tutorial-paths)

## Novo Substance Engine v9

Todos os novos nós listados acima são baseados na nova versão do Substance Engine, e eles estão aproveitando ao máximo seu novo recurso principal: <b>loops</b>.

Os loops devem ser usados apenas dentro dos [gráficos de função Substance](../../function-graphs/function-graphs.md) e é mais provável que você os implemente em um [Processador de pixels](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), um [Fx-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) ou um [Processador de valor](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md). Os loops permitirão naturalmente que você repita facilmente uma função muitas vezes, até que uma condição seja respeitada. Ele vai ajudá-lo a clarear muito seus gráficos, e ganhar em precisão.

Este [tutorial](https://www.youtube.com/watch?v=Ggoy8G90oDI)dedicado ajudará você a começar a trabalhar com loops.

O Substance Engine v9 também traz as seguintes melhorias:

* Novo modo sólido no editor de gradiente do nó [Mapa de gradientes](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md) (ou seja, nenhuma interpolação)
* Nó atômico pow() em gráficos de função Substance
* Adicionar opções de quebra de borda (fixação à borda, repetição) em nós do Sampler
* Amostragem mais próxima nos nós [Distorção](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md) e [Distorção direcional](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md)

## Nó do portal

O nó [Portal](../../interface/the-graph-view/graph-items/graph-items.md) é uma nova extensão do nó [Ponto](../../interface/the-graph-view/graph-items/graph-items.md) com a possibilidade de ocultar conexões no seu gráfico.

Graças a esse recurso, você pode melhorar a legibilidade do gráfico ocultando conexões muito longas e também ter um acesso rápido aos nós principais de qualquer lugar no gráfico.

Este novo recurso está totalmente explicado neste [tutorial](https://www.adobe.com/go/designer-tutorial-portals) dedicado.

![Nó do portal](../../assets/PortalNodeFinal.gif "Nó do portal")

## Página inicial

Ao iniciar o Designer, você sabe que tem acesso a uma nova [tela inicial](../../interface/home-screen/home-screen.md), como a que você tem em outros produtos Adobe. Nessa tela, você pode:

* Criar rapidamente um novo gráfico;
* Consulte a lista de todos os arquivos abertos recentemente no Designer, com alguns detalhes como o tamanho, a data em que foi modificado pela última vez ou o caminho de arquivo completo;
* Uma página de aprendizado onde você pode encontrar links para recursos de aprendizado, como tutoriais para apresentar novos recursos ou para descobrir dicas rápidas;
* Links diretos para a tela Novidades, a tela Sobre, o site da Substance 3D, o fórum da comunidade de suporte etc.

![Tela inicial - Tela inicial](../../assets/HomeScreen.png "Tela inicial - Página inicial")

![Tela inicial - Saiba](../../assets/LearnPage.png "Tela inicial - Saiba")

## Novos idiomas

Esta versão vem com três idiomas adicionais:

* espanhol (Espanha);
* Italiano (Itália);
* Português (Brasil).

Lembre-se: se quiser alterar o idioma no Designer, basta acessar [Preferências](../../interface/preferences-window/preferences-window.md) e encontrar a lista de todos os idiomas disponíveis na seção Geral.

## Notas de versão

### 13.0.0

*(Lançado em 6 de junho de 2023)*

### Adicionado

* [Graph] Nó do portal
* [Integração] Nova tela inicial
* Nó de spline (cúbico) [Content]
* Nó de spline (Poly Quadratic) [Content]
* [Content] Nó do círculo de spline
* Nó da Lista de Pontos [Content]
* Nó da Ponte de spline [Content] (2 splines)
* Nó (Lista) da Ponte de Spline [Content]
* [Content] Nó de acréscimo de spline
* [Content] Nó de seleção de spline
* [Content] Nó da lista de mesclagem de spline
* [Conteúdo] Nó de transformação 2D de spline
* [Content] Nó de distorção de spline
* [Content] Nó do Height de amostra de spline
* [Content] Nó do Thickness de amostra de spline
* [Content] Nó de renderização de spline
* [Content] Dispersão no nó Cor de spline
* [Content] Dispersão no nó Spline Grayscale
* [Content] Nó de cor do mapeador de spline
* [Content] Nó de tons de cinza do mapeador de spline
* [Content] Nó de cor do mapeador da ponte de spline
* [Content] Nó em tons de cinza do Mapeador da ponte de spline
* [Content] Nó do mapeador de fluxo de spline
* [Content] Nó de cor do mapeador UV
* [Content] Nó em tons de cinza do Mapeador UV
* [Content] Caminhos para o nó Splines
* [Conteúdo] Nó Máscaras para caminhos
* [Conteúdo] Nó de transformação de caminhos 2D
* [Content] Nó de polígono de caminhos
* [Content] Nó Caminhos de visualização
* [Content] Nó de distorção de caminhos
* [Conteúdo] Nó de seleção de caminhos
* [Content] Nó do processador de vértice dos caminhos
* [Content] Caminhos Processador de vértice Nó simples
* [Content] Quad Transform no nó Caminho
* [Content] Raytraced Ambient Oclusão v2
* [Content] Raytraced Bent Normal v2
* [Content] Raytraced Shadows v2
* [Engine] Atualização para a versão 9
* [Engine] Nó de loop em gráficos de função
* [Mecanismo] Adicionar modo sólido ao gradiente
* [Engine] Nó atômico pow() no Gráfico de funções
* [Engine] Adicionar opções de quebra de borda (fixação à borda / repetição) no nó Sampler
* [Engine] Amostragem mais próxima no nó Distorção e Distorção direcional
* [Engine] Adiciona um modo “alfa perfurado” ao filtro Tornar Nítido para entradas de cores
* [Engine] FxMap: Morfeta do Hemisfério
* [Engine] Operações Atômicas Get/Set em gráficos de função
* [Motor] Funções: usar função precisa de log / log2 / exp, 2pow - Unificar funções entre o fogão e o motor
* [Engine] Adiciona um parâmetro de “deslocamento de intensidade” ao filtro de Distorção direcional
* [API] Suporte ao gerenciamento de predefinições para composição de gráficos
* [Funções] Alterar nome de entrada para nós atômicos de funções
* [Localização] Adicionar idiomas português (Brasil), italiano (Itália) e espanhol (Espanha)
* [Localização] Respeitar a regra “Idioma (País)” na lista de idiomas
* [Predefinições] Desativar os painéis “Visualização” e “Predefinições” nas propriedades do gráfico ao usar a edição no contexto
* [Substance models graph] Fim do suporte dos gráficos de modelos de Substance

### Correções

* [Exibição 3D] A exibição de sequências longas nas estatísticas da cena é cortada (somente macOS)
* [API] O módulo &#39;structure::Structure&#39; ainda está incluído na referência de API
* [API] Os nós pontos nos gráficos MDL não têm definição nem propriedades
* [API] Comportamento incorreto ao definir o parâmetro dos nós de função
* [Content] 3D Voronoi e 3D voronoi fractal geram um aviso de cozimento
* [Engine] O parâmetro &#39;Intensity Map Offset&#39; não tem efeito nos dados em tons de cinza no mecanismo SSE2
* [Explorer] A E/S do gráfico pode ser excluída
* [Graph] O bitmap é ignorado quando usado em instâncias
* [Graph] Posição incorreta do nó de ponto quando criado a partir de um nó
* [Graph] Foco incorreto na caixa de diálogo “Expor parâmetro” ao usar a tecla “Enter”
* [Gráfico] Resultado incorreto na verificação de histograma com bitmap na edição de contexto
* [Localização] Corrigir vários problemas de recorte
* [Parâmetros] Falha ao excluir um parâmetro de entrada
* [Publish] Os gráficos nas pastas são movidos para a raiz no pacote publicado
* [Resources] Falha ao atualizar um recurso carregado no disco
* [VisibleIf] Corrigir regressão na avaliação da visibilidade condicional
