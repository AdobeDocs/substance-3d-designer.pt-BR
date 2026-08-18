---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/substance-compositing-graph-key-concepts.html"
breadcrumb-title: ''
description: Conheça os principais conceitos de gráficos de composição de Substance, incluindo nós, conexões e conceitos básicos de fluxo de trabalho.
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Substance graph key concepts
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Conceitos-chave de gráficos do Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 1%

---


# Conceitos-chave de gráficos do Substance

Esta página lista os conceitos importantes a serem entendidos para trabalhar com gráficos de Substance no Substance 3D Designer.

## Subgráficos/Publicação

[Publicar um gráfico](https://helpx.adobe.com/br/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html) ou criar um subgráfico são dois conceitos abstratos muito semelhantes. Isso significa que qualquer gráfico ou rede de nós pode ser “empacotado” em conjunto e transformado em um recurso autônomo e reutilizável. A criação de [subgráficos](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) é feita principalmente dentro do aplicativo para tornar determinado conteúdo reutilizável em um fluxo de trabalho inteligente e eficiente, pois isso evita a duplicação de um conjunto de nós repetidamente. A publicação envolve uma etapa adicional para exportar para o formato [Ativo do Substance 3D (SBSAR)](https://helpx.adobe.com/br/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html), tornando o gráfico de rede do nó utilizável fora do aplicativo, como quando você cria um material para o Mecanismo Irreal.

As entradas, as saídas e os parâmetros expostos são extremamente importantes para esse conceito, pois são as únicas maneiras de interagir com o gráfico depois que ele é usado como um subgráfico ou como um ativo publicado do Substance 3D. Os motivos são os seguintes:

* Nenhuma saída significaria que o gráfico <b>não gera nada</b>, nenhum dado.
* Nenhum Parâmetro exposto significa que o gráfico <b>não pode ser personalizado</b> de forma alguma. Você não seria capaz de definir coisas como a intensidade de um efeito, a opacidade de uma imagem sendo mesclada, a cor de uma área específica, etc...
* Sem Entradas significa que, em alguns casos, você não poderá personalizar o resultado de um gráfico com<b> seus próprios dados de imagem</b>, como mapas de malha cozida para gerar efeitos, uma imagem de entrada para executar um desfoque ou uma máscara personalizada para isolar determinadas áreas de uma imagem.

## Entradas e saídas

Uma [Saída](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)é um Nó que gera um único resultado 2D. É um ponto final, um ponto final para o seu gráfico, um resultado finalizado. Somente os dados conectados a uma saída podem ser exportados para fora do Designer ou até mesmo usados em outros gráficos.

Aqui estão algumas coisas que você deve saber sobre Saídas:

* Você pode ter quantas saídas desejar, mas deve ter <b>pelo menos uma saída</b>.
* Uma saída pode ter <b>qualquer resolução</b> de até 8192px de largura ou altura, pode ser<b> colorida ou em tons de cinza</b> e pode ser exportada para qualquer tipo de arquivo com suporte.
* As saídas podem e devem ser <b>nomeadas exclusivamente</b> para identificá-las. Isso ajuda na exportação.
* Cada conector do lado direito de qualquer Nó é na verdade uma Saída (consulte “Sub-gráficos para obter mais informações)

Uma [Entrada](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) é semelhante a uma Saída; é um slot vazio e aberto para você ou outro usuário conectar seus próprios dados. Permite a criação de gráficos que contenham dados de imagem externos definidos pelo usuário, como um filtro que modifique uma imagem de entrada (um desfoque ou um ajuste de contraste, por exemplo).

Aqui estão algumas coisas que você deve saber sobre entradas:

* As entradas são completamente <b>opcionais</b>, você só deve adicioná-las se necessário. Não há valor mínimo ou máximo.
* As entradas têm uma resolução definida (vinculada ao gráfico em geral) que você define, bem como se são em tons de cinza ou coloridas. Qualquer item conectado a ele será convertido para corresponder a isso.
* As entradas podem ser arquivos de bitmap do disco rígido, outros gráficos, camadas do Painter ou Alchemist, etc.
* Cada conector no lado esquerdo de qualquer Nó é uma Entrada (consulte “Sub-gráficos para obter mais informações)

## Herança

À medida que imagens e valores são passados de nós para outros, alguns *atributos* dessas imagens, ou seja, seus <b>Parâmetros Base</b>, também são *propagados* pelo gráfico, como resolução, precisão (ou seja, profundidade de bits), divisão em blocos gráficos e semente aleatória.

Esta propagação é definida pelos [métodos de herança](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) que cada nó aplica a esses atributos. Na verdade, os nós podem *herdar atributos* de outros nós ou do gráfico em que eles existem.\
Os métodos de herança podem ser:

* *Relativo ao pai*
* *Relativo à entrada*
* *Absoluto* - isto é, sem herança

A herança pode ser abstrata e complicada de gerenciar. Portanto, recomendamos que você dê uma olhada na [página dedicada](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) discutindo-a em detalhes.

## Parâmetros de exposição

A exposição de parâmetros é um conceito que pode ser muito profundo, mas pode ser resumido como a escolha de certas propriedades dos nós em seu gráfico e a criação de um elemento de controle de interface dedicado para eles, que fica facilmente disponível quando o gráfico é usado como um Sub-gráfico ou se é publicado como um Arquivo. Como não é mais possível selecionar nós com rapidez ou facilidade e ajustar suas propriedades, o objetivo é criar outro painel de controle principal que agrupe todas as propriedades relevantes para esse gráfico específico.

veja algumas coisas que você deve saber sobre Parâmetros expostos:

* Os Parâmetros Expostos <b>movem um controle do Nó para o gráfico</b>, essencialmente um nível acima na hierarquia.
* Os Parâmetros Expostos não podem mais ser alterados no nó, apenas no gráfico.
* Os parâmetros expostos podem ser totalmente personalizados com nomes, rótulos, valores, tipo de editor de interface e até mesmo ocultos e exibidos em determinadas condições.

A exposição de Parâmetros é um conceito abstrato e difícil para iniciantes,[há mais documentação dedicada sobre este tópico](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), mas é recomendável se familiarizar totalmente com outros aspectos básicos do software antes de mergulhar em exposição de parâmetros.
