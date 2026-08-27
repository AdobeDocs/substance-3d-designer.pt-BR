---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/creating-a-substance-compositing-graph/graph-instances-sub-graphs.html"
breadcrumb-title: ''
description: Use instâncias de gráfico e subgrafos para criar componentes de gráfico reutilizáveis e fluxos de trabalho de material modulares.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Creating a Substance compositing graph > Graph instances and subgraphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Instâncias e subgrafos do gráfico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 0%

---


# Instâncias e subgrafos do gráfico

![](../../../assets/sub-graph.png)

As instâncias de gráfico são nós que <b>fazem referência a outro gráfico</b>. Um gráfico referenciado por um nó de instância em um gráfico host pode ser chamado de <b>subgrafo</b> do gráfico host.

O uso de ocorrências torna um gráfico reutilizável muitas vezes em um ou mais gráficos, mesmo em diferentes pacotes.

## Por que devo usar instâncias de gráfico?

<b>Dividir gráficos em vários subgrafos</b> permite trabalhar *muito* de forma mais eficiente<b>.</b>

Toda vez que estiver duplicando uma cadeia de nós no Designer, você provavelmente poderia dividir essa cadeia em um subgrafo para facilitar a reutilização e a atualização.

>[!NOTE]
>
> Um arquivo de projeto que demonstra uma configuração simples de um subgráfico para um filtro *personalizado* está disponível na seção [Gráficos de Substance de exemplo](../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md) desta documentação.

### Como criar uma instância de gráfico?

Arraste um gráfico A do Explorer para outro gráfico B para criar um <b>nó de instância</b> que faça referência ao gráfico A.

Os nós podem ser divididos rapidamente em um novo gráfico selecionando os nós e usando “Criar gráfico a partir da seleção” no menu contextual. Você será solicitado a definir o identificador do novo gráfico, que deve ser exclusivo.

Observe que, se os nós selecionados estiverem conectados a outros nós no gráfico, você também deverá criar nós de [Entrada](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) e de [Saída](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) no novo gráfico para transportar essas conexões para o subgrafo.

Além disso, a substituição dos nós originais por um nó de instância que faz referência ao novo gráfico deve ser feita manualmente posteriormente.

Finalmente, você deve decidir se o subgrafo deve ser exposto aos usuários ao publicar seu projeto em um arquivo SBSAR compartilhável. Consulte o parâmetro &#39;Exposed in SBSAR&#39; nas [propriedades do gráfico](../../../compositing-graphs/graph-parameters/graph-parameters.md).

### Uma palavra sobre herança

Outro benefício do uso de subgrafos é que cada instância de um subgrafo pode <b>se adaptar ao contexto</b> em que está sendo usada. Em outras palavras, duas ocorrências do mesmo gráfico podem ter resoluções de saída, profundidades de bits e modos de divisão em blocos gráficos diferentes.

Este é um <b>conceito essencial</b> de trabalhar em gráficos e recomendamos que você saiba mais sobre a [herança em gráficos de Substance](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) quando estiver pronto para ir além com as instâncias.

Observe que, embora os conceitos de ocorrência de gráfico e subgrafo também se apliquem a gráficos de função Substance, a herança, conforme discutida nessa página, se aplica somente a gráficos Substance.

### Posso adicionar minhas próprias instâncias do gráfico à biblioteca de nós?

<b>Sim, isso é possível </b>mas requer alguma configuração específica. Saiba mais na página [Gerenciando conteúdo e filtros personalizados](../../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) desta documentação.

### É possível inspecionar o gráfico de origem de uma instância do gráfico?

![(tick)](../../../assets/check.svg) Sim, e *somente* para instâncias de gráficos carregados de um **arquivo Substance 3D (SBS)**. Estes nós de instância têm um rótulo *vermelho-escuro*.\
Clique com o botão direito do mouse no nó para abrir seu menu contextual e selecione a opção **Abrir referência**.

>[!NOTE]
>
> Ao inspecionar o gráfico de origem, você poderá usar os dados de entrada do gráfico da instância se a opção **Edição de contexto interno** estiver *marcada* na seção **Gráfico** das [Preferências](../../../interface/preferences-window/preferences-window.md).

![(menos)](../../../assets/forbidden.svg) *Não* é possível inspecionar gráficos carregados de instâncias **de ativos do Substance 3D (SBSAR)**, pois eles já estão compilados. Você só pode carregar o ativo no painel **Explorer** para inspecionar a lista de gráficos expostos e seus parâmetros. Estes nós de instância têm um rótulo *verde*.\
Clique com o botão direito do mouse no nó para abrir seu menu contextual e selecione a opção **Carregar pacote**.

>[!NOTE]
>
> **Nós atômicos**
> 
> Os nós *atômicos* são implementados diretamente por meio do código no mecanismo de Substance e são *não* instâncias de gráficos, portanto, o nome atômico: eles são os *menores blocos de criação* para *todos* os outros nós em [gráficos de Substance](../../../compositing-graphs/substance-compositing-graphs.md).
