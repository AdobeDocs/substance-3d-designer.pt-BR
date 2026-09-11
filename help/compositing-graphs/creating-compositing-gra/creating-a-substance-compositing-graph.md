---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/creating-a-substance-compositing-graph.html"
breadcrumb-title: ''
description: Saiba como criar gráficos de composição de Substance no Substance 3D Designer para criar fluxos de trabalho de textura de procedimentos.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Creating a Substance graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Criação de um gráfico do Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7e53313d3c368803a95ebb1f9eee712ae2a05817
workflow-type: tm+mt
source-wordcount: '1107'
ht-degree: 1%

---


# Criação de um gráfico do Substance

A criação de texturas no Designer começa com a criação de um gráfico de Substance, a partir de um modelo pré-criado ou de um gráfico vazio.

<a name="create-graph"></a>

## Criar um gráfico

Para iniciar o processo de criação de um novo gráfico de [Substance](../../compositing-graphs/substance-compositing-graphs.md), você pode usar um destes métodos:

* &#x200B;
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  Na tela inicial, clique no botão <b>Novo gráfico</b>.

  </td>
  <td style="border: 0;" valign="top">

  ![Caixa de diálogo Novo gráfico de Substance - Criar da Tela Inicial](creating-a-substance-compositing-graph.resources/newGraphDialog-create-homeScreen.png "Caixa de diálogo Novo gráfico de Substance - Criar da Tela Inicial"){zoomable="yes"}

  </td>
  </tr>
  </table>

* &#x200B;
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  Em qualquer item de pacote *existente* no [Explorer](../../interface/the-explorer-window/the-explorer-window.md), clique em <b>RMB</b> e vá para <b>Novo > Substance</b> no menu contextual.

  </td>
  <td style="border: 0;" valign="top">

  ![Caixa de diálogo Novo gráfico de Substance - Criar a partir do Explorer](creating-a-substance-compositing-graph.resources/newGraphDialog-create-explorer.png "Caixa de diálogo Novo gráfico de Substance - Criar a partir do Explorer"){zoomable="yes"}

  </td>
  </tr>
  </table>

* &#x200B;
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  Na barra de ferramentas principal, clique no botão ![](creating-a-substance-compositing-graph.resources/image2021-6-22-20-36-44.png) <b>Novo Substance</b>.

  </td>
  <td style="border: 0;" valign="top">

  ![Caixa de diálogo Novo gráfico de Substance - Criar da barra de ferramentas principal](creating-a-substance-compositing-graph.resources/newGraphDialog-create-mainToolbar.png "Caixa de diálogo Novo gráfico de Substance - Criar da barra de ferramentas principal"){zoomable="yes"}

  </td>
  </tr>
  </table>

* &#x200B;
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  No menu principal, vá para <b>Arquivo > Novo > gráfico de Substance...</b>

  </td>
  <td style="border: 0;" valign="top">

  ![](creating-a-substance-compositing-graph.resources/newGraphDialog-create-mainMenu.png)

  </td>
  </tr>
  </table>

* Pressione a tecla <b>Ctrl+N</b> (Windows) / <b>Cmd+N</b> (macOS).

Não importa o método escolhido, você verá a caixa de diálogo <b>Novo gráfico de Substance</b>.

<a name="graph-templates"></a>

## Modelos de gráfico

Independentemente do método usado para criar um novo gráfico de Substance, você sempre verá a caixa de diálogo <b>Novo gráfico de Substance</b>, que permite configurar o novo gráfico.

![Caixa de diálogo Novo gráfico de Substance - Materiais](creating-a-substance-compositing-graph.resources/newGraphDialog-materials.png "Caixa de diálogo Novo gráfico de Substance - Materiais"){zoomable="yes"}

### Modelos

O Designer inclui modelos de gráficos com nós pré-configurados para agilizar o seu trabalho. Eles podem incluir nós de [Saída](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md), nós simples para passar valores para essas saídas, como [Cores uniformes](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md), bem como nós de [Entrada](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md).

Clique duas vezes em um modelo na lista ou selecione-o e clique no botão <b>Criar</b> para criar um novo gráfico de Substance usando esse modelo. Por padrão, o novo gráfico é colocado em um novo pacote não salvo.

>[!TIP]
>
> Começar do zero
> 
> Para começar com um gráfico totalmente em branco, selecione o modelo <b>Vazio</b> na categoria &#39;Vazio&#39;.

>[!NOTE]
>
> Alternando modelos
> 
> Se você selecionar o modelo errado, *não poderá* alternar para um modelo diferente após criar o gráfico.
> 
> Para migrar o gráfico existente para outro modelo, você pode criar um novo gráfico usando o modelo apropriado e copiar e colar o gráfico para o novo modelo. Reconecte os nós conforme apropriado, nós de saída em particular.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Cada modelo é listado por seu rótulo e subtítulo.

O subtítulo fornece mais contexto sobre o *caso de uso* do modelo: o modelo de material no qual ele se baseia, o software com o qual ele deve se integrar etc.

No modo <b>Miniaturas</b>, o subtítulo é colocado sob o rótulo em um texto menor e mais escuro.

Nos modos de exibição <b>Lista</b>, <b>Pacotes</b> e <b>Diretórios</b>, o subtítulo é anexado ao rótulo assim: *Rótulo - Subtítulo*.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Caixa de diálogo de novo gráfico de Substance - Cartão de miniatura](creating-a-substance-compositing-graph.resources/newGraphDialog-thumbnailCard.png "Caixa de diálogo de novo gráfico de Substance - Cartão de miniatura")

</td>
</tr>
</table>

<a name="material-samples"></a>

### Amostras de materiais

A categoria <b>Amostras de materiais</b> inclui uma [seleção selecionada de gráficos](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md) para aprender e experimentar.

Você também pode acessar as amostras diretamente na tela inicial, usando o botão <b>Ir para amostras</b>.

Todas as amostras são baseadas no [modelo de material de OpenPBR](../../interface/3d-view/material-properties/material-properties.md#openpbr).

![Amostras de materiais - Banner da tela inicial](creating-a-substance-compositing-graph.resources/materialSamples-banner.png "Amostras de materiais - Banner da tela inicial"){zoomable="yes"}

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Dica de ferramenta de informações

Passar o mouse sobre o ícone de informações para cada item de modelo exibe uma dica de ferramenta com informações adicionais sobre o modelo:

<b>Tipo:</b> o tipo de ativo que o modelo deve produzir. Isto é editável nas [propriedades do gráfico](../../compositing-graphs/graph-parameters/graph-parameters.md).

<b>Descrição:</b> detalhes sobre o modelo, como o fluxo de trabalho no qual ele se integra, seu caso de uso pretendido e recomendações para seu uso.

<b>Saídas:</b> Os nós de [Saída](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md) do modelo, se houver.

</td>
<td style="border: 0;" valign="top">

![Caixa de diálogo Novo gráfico de Substance - Dica de ferramenta de modelo](creating-a-substance-compositing-graph.resources/newGraphDialog-tooltipTemplate.png "Caixa de diálogo Novo gráfico de Substance - Dica de ferramenta de modelo"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Modos de visualização

A lista de modelos pode ser exibida em modos diferentes usando o botão <b>Modos de exibição</b>.

A filtragem executada pela categoria selecionada e pelo arquivo de projeto é aplicada em todas as exibições.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Caixa de diálogo Novo gráfico de Substance - Modos de exibição](creating-a-substance-compositing-graph.resources/newGraphDialog-viewModes.png "Caixa de diálogo Novo gráfico de Substance - Modos de exibição"){zoomable="yes"}

</td>
</tr>
</table>

+++Modos de visualização
![Caixa de diálogo Novo gráfico de Substance - Exibição de miniaturas](creating-a-substance-compositing-graph.resources/newGraphDialog-viewMode-thumbnails.png "caixa de diálogo Novo gráfico de Substance - Exibição de miniaturas"){zoomable="yes"}



<b>Miniaturas</b>

Cartões com miniaturas que fornecem uma visualização ou um ícone do tipo de modelo.

![Caixa de diálogo Novo gráfico de Substance - Exibição em lista](creating-a-substance-compositing-graph.resources/newGraphDialog-viewMode-list.png "Caixa de diálogo Novo gráfico de Substance - Exibição em lista"){zoomable="yes"}



<b>Lista</b>

Os modelos são listados somente por seu rótulo.

![Caixa de diálogo do novo gráfico de Substance - Exibição de pacotes](creating-a-substance-compositing-graph.resources/newGraphDialog-viewMode-packages.png "caixa de diálogo do novo gráfico de Substance - Exibição de pacotes"){zoomable="yes"}



<b>Pacotes</b>

Os modelos são listados por seu rótulo como filhos do arquivo de pacote ao qual pertencem.

Passe o mouse sobre um item de arquivo de pacote para exibir uma dica de ferramenta com seu caminho completo.

![Caixa de diálogo Novo gráfico de Substance - exibição de diretórios](creating-a-substance-compositing-graph.resources/newGraphDialog-viewMode-directories.png "caixa de diálogo Novo gráfico de Substance - exibição de diretórios"){zoomable="yes"}



<b>Diretórios</b>

Os modelos são listados por seu rótulo como filhos do diretório que hospeda o arquivo de pacote ao qual pertencem.

Passe o mouse sobre um item de diretório para exibir uma dica de ferramenta com seu caminho completo.

+++

### Propriedades

Depois de selecionar o modelo, você pode configurar informações básicas sobre o novo gráfico. Ele pode ser alterado a qualquer momento após a criação do gráfico.

<b>Nome do gráfico</b>: o identificador do gráfico. Ele precisa ser exclusivo para um determinado pacote e não pode incluir espaços nem alguns caracteres especiais.

<b>Tamanho</b>: a resolução pai do gráfico, que controlará a resolução de saída da maioria dos nós - consulte a página [Tamanho de saída](../../compositing-graphs/output-size/output-size.md) para saber mais. Por padrão, a largura e a height são vinculadas entre si. Para desvinculá-las, clique no botão de vínculo entre as caixas de combinação Largura e height.

<b>Criar gráfico em</b>: você pode usar esta caixa de combinação para criar um *novo* pacote para o novo gráfico ou adicionar o novo gráfico a qualquer pacote *existente* já carregado no painel [Explorer](../../interface/the-explorer-window/the-explorer-window.md).

### Dica de ferramenta da Ajuda

Passe o mouse sobre o ícone de ponto de interrogação para exibir uma dica de ferramenta com um botão que vincula diretamente a esta página, para que você possa consultar esta documentação novamente conforme necessário.

![Caixa de diálogo Novo gráfico de Substance - Dica de ferramenta de Ajuda](creating-a-substance-compositing-graph.resources/newGraphDialog-tooltipHelp.png "Caixa de diálogo Novo gráfico de Substance - Dica de ferramenta de Ajuda"){zoomable="yes"}

<a name="managing-templates"></a>

## Gerenciar modelos

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Filtrar por categoria

As categorias são usadas para agrupar modelos relacionados entre si por caso de uso ou tipo de ativo.

Use a caixa de combinação <b>Categoria</b> para selecionar a categoria pela qual deseja filtrar os modelos.

</td>
<td width="41.67%" style="border: 0;" valign="top">

![Caixa de diálogo Novo gráfico de Substance - Filtrando por categoria](creating-a-substance-compositing-graph.resources/newGraphDialog-categories.png "Caixa de diálogo Novo gráfico de Substance - Filtrando por categoria"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Os modelos podem ter uma categoria configurada em seus <b>Dados de modelo</b> [atributo de gráfico](../../compositing-graphs/graph-parameters/graph-parameters.md), que é usado como filtro para restringir a lista de modelos:

&lt;category>;&lt;subtitle>

Categorias personalizadas podem ser configuradas nos modelos fornecidos pelos arquivos de projeto (veja abaixo). Em seguida, estas categorias serão adicionadas à lista na caixa de combinação.

</td>
<td width="50.00%" style="border: 0;" valign="top">

![Caixa de diálogo Novo gráfico de Substance - Configurando a categoria do modelo](creating-a-substance-compositing-graph.resources/newGraphDialog-templateCategorySetup.png "Caixa de diálogo Novo gráfico de Substance - Configurando a categoria do modelo"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Filtrar por arquivo de projeto

Se algum dos [arquivos de projeto](../../interface/preferences-window/project-settings/project-settings.md) ativos fornecer um ou mais caminhos de modelo, os gráficos nos arquivos de pacote encontrados nesses caminhos serão adicionados à lista de modelos.

Em seguida, use o botão <b>Filtrar por arquivo de projeto</b> para restringir a lista de modelos aos fornecidos por um arquivo de projeto específico.

</td>
<td width="33.33%" style="border: 0;" valign="top">

![Caixa de diálogo Novo gráfico de Substance - Filtrando por arquivo de projeto](creating-a-substance-compositing-graph.resources/newGraphDialog-projectFiles.png "Caixa de diálogo Novo gráfico de Substance - Filtrando por arquivo de projeto"){zoomable="yes"}

</td>
</tr>
</table>
