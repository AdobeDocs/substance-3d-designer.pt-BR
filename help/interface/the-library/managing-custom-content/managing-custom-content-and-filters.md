---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/interface/the-library/managing-custom-content-and-filters.html"
breadcrumb-title: ''
description: Saiba como gerenciar conteúdo e filtros personalizados na Biblioteca da Substance 3D Designer para acesso a ativos organizados.
helpx_creative_field: ""
helpx_description: Designer > Interface > The Library > Managing custom content and filters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gerenciamento de conteúdo e filtros personalizados
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '912'
ht-degree: 0%

---


# Gerenciamento de conteúdo e filtros personalizados

Esta página explica o método para criar categorias e filtros para gerenciar conteúdo personalizado na Biblioteca. Também inclui sugestões para fluxos de trabalho baseados em projetos.

## Visão geral

Depois de [adicionar conteúdo personalizado à biblioteca](../../../interface/preferences-window/project-settings/project-settings.md), você precisa torná-la *detectável*.

A Biblioteca usa vários *pontos de dados* para identificar o conteúdo, para filtrá-lo e exibir pesquisas. Esses pontos de dados incluem:

* Nome
* Extensão
* URL (ou seja, *nome do arquivo*)
* Atributos

Você pode organizar sua <b>Biblioteca</b> em categorias que contêm filtros específicos e ajustá-la às necessidades do seu projeto.\
Na verdade, as categorias e filtros personalizados podem ser *específicos do projeto* e ser salvos em [arquivos do projeto](../../../interface/preferences-window/project-settings/project-settings.md) (\*.sbsprj). Esses arquivos podem ser reunidos em [Arquivos de configuração](../../../interface/preferences-window/project-settings/project-settings.md) (\*.sbscfg) e distribuídos a uma equipe para que todos os artistas possam usar as* mesmas categorias da <b>biblioteca</b>* para qualquer projeto específico.

Isso significa que, com um ou mais arquivos do Project, você pode definir as pastas nas quais o conteúdo deve ser adicionado à <b>Biblioteca</b>, bem como as categorias e filtros que classificarão e organizarão esse conteúdo.

![Conteúdo personalizado na biblioteca](../../../assets/library-filters.png "Conteúdo personalizado na biblioteca")

## Atributos do grafo

Os gráficos contidos nos arquivos [SBS](../../../getting-started/overview/overview.md) e [SBSAR](../../../getting-started/overview/overview.md) podem ser *filtrados e pesquisados* na Biblioteca usando o conjunto de dados na seção [Atributos](../../../compositing-graphs/graph-parameters/graph-parameters.md) das propriedades do gráfico. Alguns desses atributos também podem ser definidos em alguns outros [tipos de recursos](../../../resources/resources.md).

## Filtros e pastas personalizados

Os filtros são parâmetros de pesquisa booleanos simples (Verdadeiro/Falso) que resultarão na exibição de um recurso dentro da Biblioteca quando esse <b>Filtro</b> for selecionado. Os recursos podem ser tudo o que estiver dentro de um pacote. Lembre-se do seguinte:

* Um <b>Filtro</b> corresponderá a todos os recursos, em *todos os caminhos observados*.
* Um <b>Filtro</b> pode conter várias condições, *todas elas devem ser avaliadas como True* (condição AND) para que o recurso seja exibido sob esse filtro.
* Um [recurso](../../../resources/resources.md) pode aparecer sob vários filtros, ele *não é exclusivo* para qualquer filtro.
* Um [Recurso](../../../resources/resources.md) de um caminho observado *ainda está disponível* na <b>Biblioteca</b>, mesmo que *não* em qualquer <b>Filtro</b>, usando a função <b>Pesquisar</b>.

### Como criar filtros e pastas

Categorias (isto é, pastas) e filtros são criados e editados usando os seguintes botões:

<b>![](../../../assets/library-icon-new-folder.png) Adicionar Pasta:</b> Cria uma pasta expansível na exibição Biblioteca. Você *não pode* criar subpastas.

<b>![](../../../assets/library-icon-new-filter.png) Adicionar Filtro:</b> Adiciona um novo Filtro dentro da pasta selecionada. Você *não pode* adicionar filtros às pastas padrão existentes.

<b>![](../../../assets/library-icon-edit.png) Editar Item:</b> Edita a Pasta ou o Filtro selecionado no momento. Você *não pode* editar nenhuma das propriedades das Pastas e Filtros padrão.

Para *remover* uma Pasta ou um Filtro, *clique com o botão direito* nele e selecione a opção <b>Remover</b> no menu contextual.

### Edição de filtros e pastas

As <b>pastas</b> e os <b>filtros</b> são identificados pelos seguintes dados:

* <b>Nome</b> exibido na exibição de árvore da Biblioteca.
* [Arquivo de Configuração do Projeto (SBSPRJ)](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) no qual este item está armazenado.

>[!WARNING]
>
> É *muito* importante configurá-los corretamente, para garantir que você esteja editando o *projeto correto*!

![Edição de filtro personalizado](../../../assets/library-filters-edit.png "Edição de filtro personalizado")

**Os filtros** geralmente precisam ter *condições* configuradas para atingir sua finalidade de filtragem. Essas condições são configuradas usando os seguintes critérios:

* **Tipo de Recurso**: define um [Tipo de Recurso](../../../resources/resources.md) específico, como [Gráficos](../../../compositing-graphs/substance-compositing-graphs.md)
* **Atributo** ao qual aplicar condição - veja a lista acima
* **Lógica de condição**: permite que o filtro inclua resultados com correspondências positivas, negativas, parciais e inteiras
* **Palavra-chave Condition:** a cadeia de caracteres em relação à qual os critérios **Attribute** e **Condition logic** são testados. Quando deixado em branco, qualquer recurso que corresponda a esses dois critérios será incluído

Você pode *adicionar ou remover* condições usando os botões &#39;**+**&#39; e &#39;**x**&#39; na extremidade direita da palavra-chave Condition.

>[!NOTE]
>
> Um filtro sem nenhuma condição definida resultará na exibição do conteúdo de *todas* **Biblioteca**.

## Práticas recomendadas

### Diretrizes recomendadas

* A regra geral da biblioteca padrão é que a <b>Pasta</b> está listada no atributo <b>Categoria</b>, enquanto o nome do <b>Filtro</b> é determinado pelo atributo <b>Marca</b>
* Não crie nós personalizados que se misturem com a biblioteca padrão, a menos que você *explicitamente* deseje que eles façam isso. Seus nós *serão* exibidos em Filtros padrão se eles corresponderem, portanto, você terá que usar um *sistema de marcação/nomenclatura diferente* para evitar isso
* Usar identificadores *exclusivos*, *por projeto*. Eles podem ser colocados em qualquer lugar desejado (como <b>Descrição</b>, <b>Categoria</b> ou <b>Dados do Usuário</b>), desde que você esteja *consistente* entre todos os projetos. Isso facilita muito a pesquisa e a filtragem de conteúdo *por projeto*
* Use o atributo <b>Autor</b> para controlar a pessoa inicialmente responsável pelo conteúdo, sem ter que vasculhar os registros do Controle de Versão
* Uma maneira eficiente de criar <b>Ícones</b> é usar a opção <b>Gerar</b> do atributo de gráfico [Ícone](../../../compositing-graphs/graph-parameters/graph-parameters.md) ou criar um [modelo](../../../interface/preferences-window/project-settings/project-settings.md) de gráfico para gerá-los. Dessa forma, você pode garantir a consistência e economizar trabalho na criação deles. Todos os ícones padrão da biblioteca foram criados no Designer dessa forma!

### Gerenciamento de conteúdo de escopo variável

* Você pode adicionar Recursos a *categorias existentes* se isso fizer mais sentido. Será menos trabalhoso gerenciar e manter filtros, e você pode usar um estilo de ícone especial para *diferenciá-los*.
* Você pode definir suas pastas e filtros em um *arquivo global* (nível de estúdio) de [Configuração de Projeto](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md) e adicionar conteúdo a eles simplesmente adicionando caminhos observados de *consecutivos* de [arquivos de projeto](../../../interface/preferences-window/project-settings/project-settings.md)
* Você pode definir pastas e filtros específicos para *cada projeto* para mantê-los separados
* Você pode misturar, combinar e usar métodos dos três anteriores: usar filtros existentes, definir novos globais e criar filtros exclusivos por projeto
