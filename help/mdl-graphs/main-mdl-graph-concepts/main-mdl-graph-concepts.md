---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/main-mdl-graph-concepts.html"
breadcrumb-title: ''
description: Aprenda os principais conceitos dos gráficos de Linguagem de definição de material no Substance 3D Designer para criação de material.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Main MDL graph concepts
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Principais conceitos do gráfico MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '1033'
ht-degree: 0%

---


# Principais conceitos do gráfico MDL

Esta página apresenta os principais conceitos que são *específicos* para [gráficos MDL](../../mdl-graphs/mdl-graphs.md) e devem ser bem compreendidos para aproveitar ao máximo este tipo de gráfico no Substance 3D Designer.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Iray

Os materiais do MDL usam uma descrição destinada a soluções de renderização baseadas fisicamente., para as quais o renderizador [Iray](../../interface/3d-view/iray/iray.md) incorporado ao Designer oferece suporte. Portanto, a exibição do resultado de um gráfico MDL *requer que o renderizador Iray* esteja selecionado em um painel [exibição 3D](../../interface/3d-view/3d-view.md) ativo.

</td>
<td style="border: 0;" valign="top">

[![Logotipo da NVIDIA Iray](../../assets/iray-logo.jpg)](https://www.nvidia.com/en-us/design-visualization/iray/)

</td>
</tr>
</table>

Ao criar ou carregar um gráfico MDL, o primeiro painel de exibição 3D [desafixado](../../interface/customizing-your-wor/customizing-your-workspace.md) encontrado pelo Designer *alterna automaticamente* para o renderizador [Iray](../../interface/3d-view/iray/iray.md). Se nenhuma exibição 3D estiver disponível, um *novo* painel de exibição 3D será criado e alternado para o renderizador Iray para hospedar a renderização do material MDL que está sendo editado.

Quando o renderizador Iray é selecionado em um painel de exibição 3D, o menu Materiais desse painel permite alternar entre os materiais MDL disponíveis, que incluem materiais carregados no painel Explorer e materiais na biblioteca MDL do Designer. Saiba mais sobre como trabalhar com materiais MDL em Iray na seção [Iray](../../interface/3d-view/iray/iray.md) desta documentação.

## Nó raiz

O resultado de um gráfico MDL é definido pelo nó <b>Raiz</b>. Qualquer nó do gráfico pode ser definido como raiz desde que seus dados de saída sejam do tipo <b>material</b>, ou seja, uma *definição de material*. Um gráfico MDL pode ter *somente um* nó Raiz.

Geralmente, um nó que pode ser definido como Raiz pode ser *autossuficiente*, pois já contém uma definição de material que pode ser personalizada passando dados para suas *entradas*.\
Por exemplo, se você deseja trabalhar em um material semelhante ao vidro, talvez queira usar uma definição de material Vidro como nó Raiz como ponto de partida, mas isso *não é obrigatório*. Muitos nós de materiais são modelados, que podem ser transformados em qualquer material complexo usando a extensa lista de nós MDL.

O nó Raiz inclui uma miniatura exibindo uma visualização de sua saída atual.

![Nó raiz do gráfico MDL](../../assets/mdl-root-hl.png "Nó raiz do gráfico MDL")

*Nó raiz em um gráfico MDL e suas propriedades exibidas no painel [Propriedades](../../interface/properties/properties.md)* &lbrace;3 **

## Conectores e tipos

Como há muito mais tipos de dados em gráficos MDL do que em outros gráficos no Designer, você pode testemunhar aparências exclusivas de conectores de nós. Os conceitos importantes a serem compreendidos estão listados abaixo.

Forma do conector

A *forma do conector* indica se o tipo de dados é *uniforme* (círculo) ou *variável* (quadrado).

“Uma variável de um tipo uniforme só pode ser definida com um valor uniforme. Uma variável de um tipo variável pode ser definida para um valor variável, bem como para um valor uniforme. O valor resultante na variável é sempre considerado variável.” (Fonte: Seção 6.3 da [Especificação MDL](https://raytracing-docs.nvidia.com/mdl/specification/MDL_spec_1.7.2_17Jan2022.pdf))

Veja alguns exemplos:

* uma amostra de <b>Textura</b> é *variável*, pois os valores são afetados pelo pixel amostrado
* um valor de <b>Cor</b> é *uniforme*, pois é transmitido igualmente, independentemente do contexto
* um <b>BRDF</b> é *variável*, pois os valores são afetados pelo ângulo de incidência
* um valor de <b>Flutuante</b> ou <b>Booleano</b> é *uniforme*, pois é passado igualmente, independentemente do contexto

Cor do conector

O *tipo de dados* que sai de um conector de saída ou é esperado por um conector de entrada é codificado por cores e exibido entre parênteses após o identificador/rótulo ao passar o mouse sobre o conector.

>[!WARNING]
>
> Somente conectores para *tipos de dados correspondentes* podem ser vinculados. O único objetivo da codificação por cores é aumentar a legibilidade em relação ao tipo de dados que estão sendo passados no gráfico, e quais conectores podem ser ligados juntos.

![Tipos de conector de nó MDL](../../assets/mdl-connector-types.png "Tipos de conector de nó MDL"){width="512px"}

*O aspecto dos conectores varia de acordo com o tipo de valor de E/S, exibido entre parênteses após o identificador de E/S*

## Criação de nó filtrado

Você pode adicionar qualquer nó disponível na categoria <b>mdl</b> da <b>Biblioteca</b> do gráfico *arrastando o nó* da <b>exibição Biblioteca</b> para a <b>exibição Gráfico</b> ou pressionando a <b>Barra de Espaço</b> para abrir o <b>menu Nó</b> na exibição Gráfico quando *nada estiver selecionado*. Nesse caso, uma lista de nós *não filtrados* é exibida.

Entretanto, há casos em que a lista de nós no menu Nó é filtrada para exibir somente nós do tipo de dados correspondente para a entrada ou saída de destino:

* se um *nó for selecionado* na exibição Gráfico e a <b>Barra de espaço</b> for pressionada
* se você clicar em <b>LMB</b>, segurar e *arrastar* um link para fora de um *conector de nó*

Convém lembrar as *regras* aplicadas à filtragem:

* se o menu Nó for exibido ao pressionar a <b>Barra de espaço</b> quando um nó *único* for selecionado, a lista incluirá nós em que o tipo de dados da *primeira entrada* corresponda ao tipo de dados de *saída* do nó selecionado
* se o menu Nó for exibido ao pressionar a <b>Barra de espaços</b> quando *vários* nós forem selecionados, a lista incluirá nós em que o tipo de dados da *primeira entrada* corresponda ao tipo de dados da *última saída* do nó *última seleção*
* se o menu Nó for exibido ao *arrastar um link* para fora de um conector de *saída*, a lista incluirá nós em que o tipo de dados da *primeira entrada* corresponda ao tipo de dados da *saída* selecionado
* se o menu Nó for exibido ao *arrastar um link* de um conector de *entrada*, a lista incluirá nós em que o tipo de dados da *saída* corresponda ao tipo de dados da *entrada selecionada*

![Criação de nó filtrado](../../assets/mdl-filtered-node-creation.gif "Criação de nó filtrado")

*Criação de nó filtrado no gráfico MDL; observe as alterações da lista de acordo com o tipo de valor do conector*

## Texturas e entradas de gráfico

Os materiais MDL podem receber dados de fontes externas, na forma de valores e texturas, por exemplo. Isso é obtido ao <b>expor um nó</b>, ao contrário do [gráfico de Substance](../../compositing-graphs/substance-compositing-graphs.md) em que existem nós de entrada dedicados para essa finalidade.

Os dados podem ser passados para o nó exposto dependendo de seu *tipo*. Por exemplo, valores Float podem ser passados para um nó <b>float</b> exposto, e uma textura pode ser passada para um nó <b>color</b> exposto (nesse caso, os valores RGBA do pixel amostrado são passados como um valor de cor).

![Entradas de gráfico expostas](../../assets/mdl-graph-inputs-samplers.png "Entradas de gráfico expostas")

*Os nós expostos criam entradas de gráfico que são entradas de valor bruto e classificadores de texturas*
