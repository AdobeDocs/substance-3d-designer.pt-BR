---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/resources/bitmap-resource.html"
breadcrumb-title: ''
description: Saiba como importar, criar e usar recursos de bitmap no Substance 3D Designer para a criação de materiais baseados em textura.
helpx_creative_field: ""
helpx_description: Designer > Resources > Bitmap resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Recurso de bitmap
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 2%

---


# Recurso de bitmap

Um recurso de bitmap é um recurso em um Pacote de Substance. É diferente do nó de bitmap atômico [. O nó de Bitmap Atômico](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) é uma representação específica desse bitmap dentro de um Substance[gráfico](../../compositing-graphs/substance-compositing-graphs.md).

Os bitmaps são alguns dos recursos não gráficos mais comuns no Substance 3D Designer. Em geral, seu uso se enquadra em uma das seguintes categorias:

* Um mapa baked, [armazenado internamente pelo Designer](../../bakers/bakers.md) ou externamente por outro aplicativo.
* Uma textura auxiliar, como um padrão, mapa de desgaste ou decalque.
* Uma máscara de tons de cinza simples para mesclagem, criada internamente usando o [nó de bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) ou com um aplicativo externo.

## Armazenamento de bitmap

Os bitmaps são geralmente o maior recurso com o qual o Designer lida. É bom que você entenda como o Designer lida com esses arquivos com seus dois tipos principais de arquivo.

### Em arquivos do Substance 3D (SBS)

A forma como os bitmaps são armazenados no SBS depende de você [Vincular ou Importá-los. Certifique-se de estar familiarizado com o conceito primeiro.](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) Os bitmaps importados podem ser editados usando as [ferramentas de pintura de bitmaps](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md).

Diferentemente dos Recursos de SVG (Gráficos de vetor), os bitmaps são sempre armazenados externamente, mesmo quando criados como um novo recurso ou importados. Para os novos Pacotes de Substance, eles são mantidos na memória até que o arquivo .SBS seja salvo no disco. Depois de salvos em disco, os bitmaps são armazenados em uma pasta */resources* ao lado do arquivo SBS.

### Em ativos do Substance 3D (SBSAR)

Em [arquivos SBSAR](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md), os bitmaps são incorporados, o que significa que eles têm um grande impacto no tamanho de arquivo SBSAR final. Você pode ler mais sobre o impacto no tamanho do arquivo ainda nesta página. Quando arquivos SBSAR são publicados, somente os bitmaps usados para calcular uma saída de um gráfico são incorporados. Todos os bitmaps não utilizados são otimizados e excluídos do pacote SBSAR final, sem efeito sobre o tamanho do arquivo.

## Tipo de arquivo, modo de cores e resolução

O Substance 3D Designer pode editar e reorganizar facilmente os dados de bitmaps, mas é melhor lembrar o seguinte:

* Defina suas resoluções para serem compatíveis com a potência 2, o que significa seguir o tamanho da textura em tempo real padrão, como <b>256, 512, 1024, 2048,</b> etc. O Designer redimensionará as texturas fora desse intervalo para a resolução correspondente mais próxima. Observe que elas não precisam estar em proporções quadradas.
* Há suporte para muitos tipos de arquivo, mas escolha um que seja melhor para o seu caso de uso. <b>A compactação sem perdas ou até mesmo os tipos de arquivos descompactados</b>, como PNG ou TGA, oferecem melhor qualidade do que JPG ou DDS.
* <b>configure o modo de cores corretamente</b>, dependendo se você precisa de cor, tons de cinza ou um canal alfa.

## Atributos de bitmap

Os recursos de bitmap em um pacote têm vários atributos que podem ser personalizados. A maioria dos atributos não tem um objetivo principal e é usada para filtros de biblioteca, embora uma minoria afete o tamanho do arquivo.

| Nome do atributo | Finalidade |
| --- | --- |
| Identificador | Usado para referenciar o recurso de bitmap em um pacote, deve ser exclusivo. |
| Caminho do arquivo | O caminho no disco do bitmap referenciado pelo recurso. |
| Descrição | A descrição exibida nas dicas de ferramentas do [Explorer](../../interface/the-explorer-window/the-explorer-window.md) e da [Biblioteca](../../interface/the-library/the-library.md) para este recurso. |
| Categoria | Usado para [classificar e organizar o recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) na [Biblioteca](../../interface/the-library/the-library.md). |
| Rótulo | Usado para [classificar e organizar o recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) na [Biblioteca](../../interface/the-library/the-library.md). |
| Autor | Usado para [classificar e organizar o recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) na [Biblioteca](../../interface/the-library/the-library.md). |
| URL do autor | Usado para [classificar e organizar o recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) na [Biblioteca](../../interface/the-library/the-library.md). |
| Tags | Usado para [classificar e organizar o recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) na [Biblioteca](../../interface/the-library/the-library.md). |
| Dados do usuário | Dados extras opcionais, não usados em bitmaps. |
| Mostrar na biblioteca | Determina se o bitmap deve ficar oculto na [exibição Biblioteca.](../../interface/the-library/the-library.md) |
| Formato de bitmap | Raw ou Jpeg, tem um grande efeito no tamanho de arquivo SBSAR. Consulte nossas [diretrizes de redução de tamanho de arquivo](../../best-practices/filesize-reduction-gui/filesize-reduction-guidelines.md) para saber mais. |
| Qualidade de compactação do bitmap | Afeta somente a compactação Jpeg, determina o equilíbrio qualidade/tamanho do arquivo. |

## Redução do tamanho do arquivo

Consulte a página [Diretrizes de redução de tamanho de arquivo](../../best-practices/filesize-reduction-gui/filesize-reduction-guidelines.md) na seção [Práticas recomendadas](../../best-practices/best-practices.md) para obter nossas recomendações sobre a minimização do tamanho de arquivo de bitmaps incorporados aos [ativos publicados do Substance 3D (SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md).
