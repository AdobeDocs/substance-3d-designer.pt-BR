---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/resources/vector-graphics-svg-resource.html"
breadcrumb-title: ''
description: Importe e use gráficos vetoriais de SVG como recursos no Substance 3D Designer para a criação de materiais de procedimento.
helpx_creative_field: ""
helpx_description: Designer > Resources > Vector graphics (SVG) resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Recurso de gráficos vetoriais (SVG)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 2%

---


# Recurso de gráficos vetoriais (SVG)

O Substance 3D Designer oferece suporte a uma forma limitada de gráficos vetoriais, por meio do formato de gráficos vetoriais escaláveis. Os arquivos de SVG podem ser trazidos como recursos de diferentes maneiras, para serem usados como recursos para seus gráficos.

Os arquivos de SVG [podem ser criados ou editados por meio do nó do SVG atômico](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md). Eles também podem ser criados pelo [UV para SVG baker.](https://experienceleague.adobe.com/pt-br/docs/substance-3d/bakers/bakers-settings/convert-uv-to-svg)

>[!NOTE]
>
> No momento, os arquivos do Adobe Illustrator (**.ai**) *não* são compatíveis.

## armazenamento de SVG

O armazenamento do SVG depende se ele está vinculado ou se foi importado. Os arquivos de SVG importados são incorporados ao arquivo SBS, o que exige [nenhum arquivo externo, como bitmaps](../../resources/bitmap-resource/bitmap-resource.md), e podem ser editados usando as [ferramentas de edição de vetor](../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md).

## atributos SVG

Os recursos de SVG em um pacote têm vários atributos que você pode personalizar. A maioria dos atributos não tem uma finalidade principal e é usada para filtros de biblioteca, mas uma minoria afeta a qualidade da renderização.

| Nome do atributo | Finalidade |
| --- | --- |
| Identificador | Usado para fazer referência ao recurso SVG em um pacote, deve ser exclusivo. |
| Caminho do arquivo | O caminho no disco do arquivo de SVG referenciado pelo recurso. |
| Descrição | A descrição exibida nas dicas de ferramentas do [Explorer](../../interface/the-explorer-window/the-explorer-window.md) e da [Biblioteca](../../interface/the-library/the-library.md) para este recurso. |
| Categoria | Usado para [classificar e organizar o recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) na [Biblioteca](../../interface/the-library/the-library.md). |
| Rótulo | Usado para [classificar e organizar o recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) na [Biblioteca](../../interface/the-library/the-library.md). |
| Autor | Usado para [classificar e organizar o recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) na [Biblioteca](../../interface/the-library/the-library.md). |
| URL do autor | Usado para [classificar e organizar o recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) na [Biblioteca](../../interface/the-library/the-library.md). |
| Tags | Usado para [classificar e organizar o recurso](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md) na [Biblioteca](../../interface/the-library/the-library.md). |
| Dados do usuário | Dados extras opcionais, não usados em gráficos vetoriais. |
| Mostrar na biblioteca | Determina se o recurso SVG deve estar oculto em [modo de exibição Biblioteca.](../../interface/the-library/the-library.md) |
| Qualidade dos gráficos vetoriais | Afeta a qualidade da renderização. O intervalo não é linear e a melhor qualidade é obtida em 0,5. |

## criação de SVG

Como há suporte apenas para um conjunto limitado de funcionalidades, a criação de SVG é restrita.

Em geral, o seguinte é verdadeiro:

* Apenas formas e caminhos primitivos simples podem desenhar corretamente;
* O traçado é compatível, mas resulta apenas em um traçado de largura de 1 pixel e o estilo do traçado é ignorado;
* Os estilos de linha tracejada serão definitivamente quebrados;
* O texto precisa ser convertido em caminhos/contorno para ser renderizado;
* Não há suporte para [caminhos compostos](https://helpx.adobe.com/ie/illustrator/desktop/manage-objects/reshape-transform-objects/create-compound-paths.html);
* Recursos avançados, como gradientes, não são compatíveis;
* Elementos de estilo para propriedades CSS não são suportados.

## Opções de exportação recomendadas

As opções de exportação são um pouco diferentes para cada aplicativo:

### Adobe Illustrator

O [Illustrator](https://www.adobe.com/br/products/illustrator.html) permite ter mais controle sobre as exportações de SVG se você prestar atenção às opções a seguir.

* Use apenas <b>Salvar como</b>, *não* Exportar como!
* O <b>Perfil de SVG</b> não importa muito, embora o perfil Minúsculo seja (principalmente) padrão para configurações que estão definitivamente corretas;
* <b>Fontes</b> devem ser definidas como <b>Converter em estrutura de tópicos</b> para funcionar;
* <b>As Propriedades de CSS</b> devem *não* ser definidas como Elementos de Estilo; todas as outras opções funcionarão;
* Desmarque <b>Preservar Recursos De Edição Do Illustrator</b>;
* Desmarcar <b>Responsivo</b>;
* Os traçados não funcionarão bem, use <b>Objeto > Caminho > Traçado de contorno</b> para que apareçam.

A imagem à direita demonstra as opções de exportação recomendadas, clique nela para exibi-la em tamanho máximo.

>[!IMPORTANT]
>
> As pranchetas podem afetar o resultado do arquivo de SVG gerado. Alguns modelos de arquivo do Illustrator apresentam várias pranchetas.\
> Tente ter apenas uma prancheta cortada corretamente e selecione-a na janela Prancheta ao salvar como SVG.

![Opções de exportação para o Illustrator SVG](vector-graphics-svg-resource.resources/vector-graphics-svg-resource-01.jpg "Opções de exportação para o Illustrator SVG"){width="512px"}

### Inkscape

O Inkscape salva nativamente como SVG, mas com menos controle sobre o formato do arquivo. Os arquivos do Inkscape funcionarão de forma nativa na aplicação, mas com algumas limitações:

* Os traçados mostram apenas 1px de largura no Substance 3D Designer. Use <b>Caminho > Traçado para caminho</b> para que funcionem,
* O texto não funcionará, use <b>Caminho > Objeto para o caminho</b> para fazer o texto funcionar.

### Adobe Photoshop

O Photoshop tem um exportador de SVG muito limitado (<b>Arquivo > Exportar > Exportar como..</b>) que atualmente não produz resultados corretos para o Substance 3D Designer. É possível obter as informações de forma e caminho, mas o Estilo sempre é salvo como Elementos, o que é incompatível.

Ele pode ser usado para máscaras de forma simples em preto e branco, em que a solução é extrair o Alpha do SVG usando a [Divisão de Alpha](../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-split/alpha-split.md).

Como alternativa, um SVG exportado para Photoshop pode ser [Importado](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md), o que permite que você [edite as informações de estilo de forma nativa dentro do aplicativo.](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)
