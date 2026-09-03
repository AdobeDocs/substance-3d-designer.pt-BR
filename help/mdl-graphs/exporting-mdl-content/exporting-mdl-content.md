---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/exporting-mdl-content.html"
breadcrumb-title: ''
description: Saiba como exportar conteúdo MDL do Substance 3D Designer para uso em renderizadores e aplicativos externos.
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Exporting MDL content
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Exportação de conteúdo MDL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1078'
ht-degree: 0%

---


# Exportação de conteúdo MDL

Esta página descreve os processos de exportação relacionados a [gráficos MDL](../../mdl-graphs/mdl-graphs.md) e materiais no Substance 3D Designer.

## Visão geral

Depois que um material MDL é criado no Designer, ele precisa ser exportado para um formato que possa *carregar a definição do material* e ser lido por renderizadores que ofereçam suporte a MDL. A MDL usa formatos proprietários para levar definições de materiais, chamados módulos MDL, gravados e empacotados em diferentes formatos, que podem ser exportados de dentro do Designer.

>[!NOTE]
>
> Todos esses formatos podem ser abertos diretamente com um *editor de texto* - às vezes, após descompactá-los com um gerenciador de arquivos - para inspecionar a definição de material que eles contêm.

## Módulo MDL (\*.mdl)

Este é o formato de arquivo de troca fundamental para definições de material. Um módulo MDL define o seguinte:

* as características e o comportamento do material
* seus parâmetros expostos e valores padrão
* suas anotações (ou seja, metadados): autor, tags, categorias, ...

A exportação de um módulo MDL é executada no nível de *pacote*. Para exportar um módulo MDL para um determinado pacote, clique no botão ![](exporting-mdl-content.resources/exporting-mdl-content-01.png) <b>Exportar Módulo MDL</b> no [Explorer](../../interface/the-explorer-window/the-explorer-window.md) ou selecione essa mesma opção no menu contextual do *pacote*. Selecione um nome e local de destino para o módulo MDL exportado e a caixa de diálogo <b>Exportar Relatório</b> será exibida com a lista de mensagens registradas durante o processo de exportação.

O módulo exportado conterá as definições de *todos* os materiais MDL definidos por um [gráfico MDL](../../mdl-graphs/mdl-graphs.md) no pacote.

>[!NOTE]
>
> Saiba mais sobre os módulos MDL nas seções 4 e 15 da [Especificação MDL](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9) da NVIDIA.

>[!NOTE]
>
> Avisos seguindo este modelo: `x appears to be invalid whereas it was expected to be an mdl::call` são causados pela maneira como os materiais MDL são processados nos gráficos MDL e são *seguros para ignorar*.

![Caminho de exportação de MDL](exporting-mdl-content.resources/exporting-mdl-content-02.png "caminho de exportação de MDL")

*Os caminhos “Exportar Módulo MDL” no Explorer e a caixa de diálogo Exportar Relatório resultante*

### Predefinição de MDL (\*.mdl)

Uma predefinição de módulo MDL é basicamente idêntica ao módulo em que se baseia, com a única diferença sendo que ela carrega um conjunto diferente de valores padrão - saiba mais [aqui](https://www.migenius.com/doc/realityserver/latest/resources/general/iray/api_reference/iray/html/classmi_1_1neuraylib_1_1IMdl__factory.html#details).

Uma predefinição para um material MDL atribuído a um material de cena `my_material` pode ser exportada dos seguintes locais:

* O painel [Explorer](../../interface/the-explorer-window/the-explorer-window.md), clicando em <b>RMB</b> no recurso de gráfico MDL e selecionando a opção <b>Exportar predefinição...</b> no menu contextual
* O painel [Exibição 3D](../../interface/3d-view/3d-view.md), usando a opção de menu <b>Materiais > meu\_material > Exportar predefinição...</b>

A opção do menu abre a caixa de diálogo <b>Exportar Predefinição de Material MDL</b>, que oferece as seguintes opções:

* <b>Diretório</b>: o local de destino para o qual o módulo MDL é exportado
* <b>Nome do Arquivo MDL</b>: o nome do módulo MDL
* <b>Incorporar Módulos MDL Importados</b>: se o módulo MDL depende de módulos importados - isto é, possui dependências de módulo, a verificação dessa opção resulta nas dependências de módulo a serem *incorporadas* ao módulo MDL exportado, tornando-o efetivamente *autossuficiente* em detrimento do tamanho do arquivo e da herança dinâmica

A predefinição exportada usará os *valores atuais* dos parâmetros do material na Exibição 3D como os *novos valores padrão*. Esses valores podem ser modificados usando a opção <b>Materiais > meu\_material > Editar</b>, que exibirá os parâmetros expostos do material no painel Propriedades.

>[!WARNING]
>
> Ao exportar um módulo MDL do painel [Explorador](../../interface/the-explorer-window/the-explorer-window.md), um módulo MDL contendo *todos* materiais MDL definidos por um gráfico MDL no pacote, a exportação de uma predefinição MDL da [Exibição 3D](../../interface/3d-view/3d-view.md) resulta em um módulo MDL contendo *somente* a definição dos materiais MDL aplicados ao *material selecionado* no menu - `my_material` neste exemplo.

![Caminho de exportação de predefinição MDL](exporting-mdl-content.resources/exporting-mdl-content-03.png "Caminho de exportação de predefinição MDL")

*O caminho “Exportar predefinição” na Visualização 3D e a caixa de diálogo Exportar predefinição de material MDL resultante*

## Arquivo morto do módulo MDL (\*.mdr)

Um arquivo de módulo MDL combina módulos MDL - veja acima - com recursos como *texturas* e arquivos readme em um *arquivo transportável único*.

A exportação de um arquivo morto do módulo MDL é executada no nível de *pacote*. Para exportar um arquivo morto do módulo MDL para um determinado pacote, clique no botão ![](exporting-mdl-content.resources/exporting-mdl-content-01.png) <b>Exportar Arquivo Morto do Módulo MDL</b> no [Explorer](../../interface/the-explorer-window/the-explorer-window.md) ou selecione essa mesma opção no menu contextual do *pacote*. Selecione um nome e local de destino para o arquivo morto do módulo MDL exportado e a caixa de diálogo <b>Exportar Relatório</b> será exibida com a lista de mensagens registradas durante o processo de exportação.

O arquivo morto do módulo exportado conterá o módulo MDL contendo as definições de *todos* os materiais MDL definidos por um [gráfico MDL](../../mdl-graphs/mdl-graphs.md) no pacote. Se um [gráfico de Substance](../../compositing-graphs/substance-compositing-graphs.md) for [instanciado em um gráfico MDL](../../mdl-graphs/compositing-graphs-and/substance-compositing-graphs-and-mdl-materials.md) e conectado a um fluxo que vai para o nó [Raiz](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md), as texturas que ele gera serão *salvas no arquivo morto*.

Além desses itens, o arquivo inclui um arquivo <b>MANIFEST</b> que descreve os seguintes metadados para o arquivo do módulo MDL:

* `mdl`: a versão do MDL usada para exportar o arquivo morto do módulo - por exemplo, “1.5”
* `version`: a versão do arquivo morto do módulo - por exemplo, “1.0.0”
* `module`: o nome do arquivo morto do módulo - por exemplo, “::pbr\_metallic\_roughness\_basic”
* `exports.material`: o nome dos materiais definidos no arquivo morto do módulo - por exemplo, “::pbr\_metallic\_roughness\_basic::MDL\_graph”

>[!NOTE]
>
> Saiba mais sobre o formato de arquivo morto MDL no Apêndice C da [Especificação MDL](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9) da NVIDIA.

![Caminho de exportação de MDR](exporting-mdl-content.resources/exporting-mdl-content-04.png "caminho de exportação de MDR")

*Os caminhos “Exportar Arquivo do Módulo MDL” no Explorer e a caixa de diálogo Exportar Relatório resultante*

## Módulo encapsulado MDL (\*.mdle)

Gráficos MDL com parâmetros expostos podem ser exportados como materiais MDL encapsulados. O encapsulamento *quebra os dados* em uma classe dedicada para que os dados *não possam ser acessados diretamente*.

Por exemplo, embora você ainda possa modificar os valores dos parâmetros expostos para controlar o comportamento de um material, a *definição* desses parâmetros *não está disponível* em um módulo MDL encapsulado.

A exportação de um módulo MDL encapsulado é executada no [Explorer](../../interface/the-explorer-window/the-explorer-window.md) no nível do gráfico MDL, selecionando a opção <b>Exportar como .mdle</b> no menu contextual de um gráfico MDL. Selecione um nome e local de destino para o módulo encapsulado MDL exportado e a caixa de diálogo <b>Exportar Relatório</b> será exibida com a lista de mensagens registradas durante o processo de exportação.

*Somente* a definição de material para o *gráfico MDL selecionado* será incluído no módulo MDL encapsulado exportado.

>[!NOTE]
>
> Saiba mais sobre definições de material encapsulado na seção 13.5 da [Especificação MDL](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9) e da [API SDK MDL](https://raytracing-docs.nvidia.com/mdl/api/mi_neuray_example_mdle.html) da NVIDIA.

![Caminho de exportação MDLE](exporting-mdl-content.resources/exporting-mdl-content-05.png "caminho de exportação MDLE")

*O caminho “Exportar como módulo” no Explorer e a caixa de diálogo Exportar Relatório resultante*
