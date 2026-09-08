---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-explorer-window.html"
breadcrumb-title: ''
description: Use a janela do Explorer no Substance 3D Designer para procurar, organizar e gerenciar seus arquivos e recursos de projeto.
helpx_creative_field: ""
helpx_description: Designer > Interface > Explorer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Explorer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 2%

---


# Explorer

Esta página descreve o encaixe do Explorer no [Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html). Esse dock permite gerenciar pacotes e seus recursos.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Visão geral

O Dock do Explorer é onde você gerencia seus arquivos e recursos atualmente abertos no Substance 3D Designer. Ela mostra uma lista de todos os pacotes atualmente abertos, com cada pacote expandido como uma hierarquia para mostrar [recursos](../../resources/resources.md)dentro dele.

O Explorer é onde você começa e termina seus projetos, pois ele permite criar, salvar e exportar qualquer tipo de recurso.

</td>
<td style="border: 0;" valign="top">

![Doca do Explorer](../../assets/explorer-3.jpg "Doca do Explorer")

</td>
</tr>
</table>

Você pode fazer algumas ações importantes no Dock do Explorer:

* Criar novos pacotes e gráficos
* Carregar pacotes existentes
* Salvar e fechar pacotes carregados
* [Importar e vincular recursos](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)
* [Exportar resultados de gráficos para texturas](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)
* [Publish um pacote para um ativo do Substance 3D (SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)
* [Enviar pacotes para outros aplicativos da Substance 3D](send-to-interoperability/send-to-interoperability.md)
* [Criar mapas a partir de uma malha](../../bakers/bakers.md)

## Barra de ferramentas superior

Essa barra de ferramentas permite executar rapidamente funções relacionadas ao fluxo de trabalho geral. Todos os botões são *sensíveis ao contexto*, o que significa que eles ativam e alteram seu comportamento com base em sua seleção atual no Explorer.

![](../../assets/save.png) <b>Salvar</b> o pacote selecionado.

![](../../assets/sendto-icon.jpg) elemento(s) selecionado(s) no <b>Publish ou no [send](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md)</b>:

* [Publish qualquer pacote selecionado para um ativo do Substance 3D (SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md);
* Enviar o pacote selecionado para o [Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html), [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html) ou [Substance 3D Stager](https://www.adobe.com/products/substance3d-stager.html).

![](../../assets/republish.png) <b>Publish ou enviar como anterior:</b> Publish ou enviar os elementos selecionados com as mesmas configurações de antes. Esta opção só está disponível em um pacote que já foi publicado *pelo menos uma vez* na sessão *atual*.

![](../../assets/graph-cleaner.jpg) <b>Remover nós não usados</b> nos gráficos selecionados. A ferramenta segue estas regras:

* A ferramenta só estará disponível se os itens selecionados forem do *mesmo tipo*: somente gráficos, pastas ou pacotes;
* Quando a seleção inclui pastas ou pacotes, a ferramenta limpa todos os gráficos nela *recursivamente*;
* Se um dos gráficos de destino for um [gráfico de Substance](../../compositing-graphs/substance-compositing-graphs.md), uma segunda opção estará disponível, permitindo limpar todas as funções de parâmetro nos nós desse gráfico.

Saiba mais sobre a ferramenta na seção &#39;Remover nós não usados&#39; da página [Exibição de gráfico](../../interface/the-graph-view/the-graph-view.md).

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Menu suspenso Publish/Send](../../assets/explorer-sendto-displayed.jpg "Menu suspenso Publish/Send")

*Publish/Send*

</td>
<td style="border: 0;" valign="top">

![Menu suspenso Remover nós não usados](../../assets/explorer-graph-cleaner.jpg "Menu suspenso Remover nós não usados")

*Remover nós não usados*

</td>
</tr>
</table>

## Menus contextuais

A maior parte da interação com o Explorer é feita por meio de menus contextuais, que são exibidos clicando em RMB em um item na exibição de árvore do Explorer.

As opções disponíveis diferem dependendo do(s) item(ns) selecionado(s) e clicado(s):

+++Espaço vazio

O espaço vazio só está disponível abaixo dos pacotes abertos no momento. Clicar ao lado dos itens existentes não é considerado um espaço vazio.

<b>Novo Pacote</b>: Cria um novo pacote vazio;

<b>Abrir Pacote</b>: abre uma caixa de diálogo de arquivo para abrir um arquivo SBS.

+++

+++Pacote

<b>Novos </b>permitem criar novos gráficos ([gráfico de Substance](../../compositing-graphs/substance-compositing-graphs.md), [bitmap](../../resources/bitmap-resource/bitmap-resource.md) e [gráficos vetoriais](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)), bem como *pastas* para classificar conteúdo

<b>Importar</b> e <b>Vincular </b>permite trazer [recursos](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)

<b>Recarregar</b>, <b>Salvar, Salvar como</b> e<b> Salvar uma cópia como</b> permitem salvar em disco ou recuperar do disco uma versão salva anteriormente do pacote.

O <b>arquivo .sbsar do Publish</b> e o<b> Republicar arquivo .sbsar</b> permitem [publicar](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md) seu gráfico de Substance não compilado e não otimizado em um arquivo SBSAR eficiente e portátil para nós em outros aplicativos e integrações de Substance. Publish como anterior repete a ação anterior do Publish com as mesmas opções, ignorando a caixa de diálogo de opções para uma iteração mais rápida. A barra de ferramentas contém botões com a mesma funcionalidade.

<b>Exportar com dependências</b> é diferente de salvar e publicar. Ele pega seus arquivos do SBS, coleta todos os recursos e dependências mencionados e cria um pacote independente. A caixa de diálogo permite que você escolha quais bibliotecas coletar e se o arquivo deve ser um arquivo compactado (7-zip). Essa é uma boa opção para compartilhar um arquivo SBS com outra pessoa, sem se preocupar com dependências ausentes.

<b>Enviar para...</b> abre um submenu que permite [enviar](send-to-interoperability/send-to-interoperability.md) diretamente seu pacote para o [Substance 3D Sampler](https://www.adobe.com/products/substance3d-sampler.html), o [Substance 3D Painter](https://www.adobe.com/products/substance3d-painter.html), o [Substance 3D Stager](https://www.adobe.com/products/substance3d-stager.html) ou o [Substance Player](https://helpx.adobe.com/substance-3d-player/home.html).

<b>Copiar</b> copia o pacote selecionado.

<b>Colar</b> cola gráficos e/ou recursos copiados *no* pacote selecionado.

<b>Fechar pacote(s)</b> fecha todos os pacotes selecionados

<b>As saídas de computação</b> forçam o Designer a calcular todas as saídas de todos os gráficos no pacote.

<b>Mostrar no Explorer...</b> abre o local do pacote na janela do explorador de arquivos do seu sistema operacional

O <b>Gerenciador de Dependências</b> abre a janela do Gerenciador de Dependências para o pacote selecionado.

<b>Abrir Dependências</b> abre todas as dependências no Explorer (*[gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md) somente*).

+++

+++Grafo do Substance

<b>Abrir:</b> (Retornar) Abre este gráfico no [modo de exibição de gráfico](../../interface/the-graph-view/the-graph-view.md).

<b>Cópia:</b> *(Ctrl-C)* Copia o gráfico atual para a área de transferência.

<b>Remover:</b> (Excluir) Exclui o gráfico deste pacote.

<b>Renomear:</b> (F2) Renomeia este gráfico.

<b>Exibir Saídas no Modo de Exibição 3D:</b> Envia as saídas deste gráfico para [o Modo de Exibição 3D](../../interface/3d-view/3d-view.md) para exibição como material.

<b>Saídas de Computação:</b> Computa as Saídas deste gráfico e as mantém na memória.

<b>Exportar saídas...:</b> abre a caixa de diálogo para [exportar para bitmaps.](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)

+++

+++Recurso de cena 3D

<b>Abrir:</b> (Retornar) Usa esta Malha 3D na[Exibição 3D](../../interface/3d-view/3d-view.md), substituindo o cubo ou plano padrão.

<b>Copiar:</b> (Ctrl-C) Copia este recurso para a área de transferência.

<b>Colar:</b> (Ctrl-V) cola o recurso da área de transferência.

<b>Remover:</b> (Del) Exclui o recurso deste pacote.

<b>Renomear:</b> (F2) Renomeia este recurso.

<b>Recarregar:</b> force a recarga desta malha a partir do disco.

<b>Mostrar no Explorer:</b> abra uma janela do navegador de arquivos do sistema no local do recurso no disco.

<b>Realocar:</b> altere este Recurso para que seja vinculado a outro arquivo.

<b>Preparar informações do modelo...:</b> abre a caixa de diálogo [Preparação.](../../bakers/bakers.md)

+++

+++Pasta

<b>Novo:</b> permite criar novos gráficos ([gráfico de Substance](../../compositing-graphs/substance-compositing-graphs.md), [gráfico de função de Substance](../../function-graphs/function-graphs.md), [bitmap](../../resources/bitmap-resource/bitmap-resource.md) e [gráficos vetoriais](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) na pasta, bem como *pastas* para classificar conteúdo.

<b>Importar</b> e <b>Link: </b>Deixe você trazer [recursos](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) e colocá-los na pasta.

<b>Copiar:</b> (Ctrl-C) Copia a pasta e todo o seu conteúdo para a área de transferência.

<b>Colar:</b> (Ctrl-V) cola a pasta e todo o seu conteúdo da área de transferência.

<b>Renomear:</b> (F2) Renomeia esta pasta.

<b>Remover:</b> *(Del)* Exclui a pasta e todo o seu conteúdo de seu pacote.

<b>Saídas de Computação:</b> computa as saídas de todos os gráficos incluídos na pasta e as mantém na memória.

+++

## Barra de ferramentas inferior

A barra de ferramentas na parte inferior do Dock do Explorer fornece informações sobre um pacote ou um recurso de pacote:

<b>![](../../assets/explorer-dependencies.jpg) Dependências:</b> Quando um pacote é selecionado, suas dependências de pacote são listadas em um painel dedicado.

<b>![](../../assets/explorer-information.jpg) Informações:</b> Fornece metadados relacionados ao pacote ou recurso atualmente selecionado:

* Pacote: o caminho de arquivo completo do pacote
* [Recurso de bitmap](../../resources/bitmap-resource/bitmap-resource.md): o caminho de arquivo completo do recurso, seu [perfil ICC](../../color-management/color-management.md), tamanho da imagem e o [método de importação](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) (ou seja, *vinculado* ou *importado*)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Painel Dependências](../../assets/explorer-dependencies-displayed.jpg "Painel Dependências")

*Dependências*

</td>
<td style="border: 0;" valign="top">

![Painel de informações](../../assets/explorer-information-displayed.jpg "Painel de informações")

*Informações*

</td>
</tr>
</table>
