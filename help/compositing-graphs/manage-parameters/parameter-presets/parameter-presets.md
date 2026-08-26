---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/manage-parameters/parameter-presets.html"
breadcrumb-title: ''
description: Saiba como criar e usar predefinições de parâmetro no Substance 3D Designer para salvar e aplicar configurações de parâmetro.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exposing a parameter > Parameter presets
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Predefinições de parâmetro
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---


# Predefinições de parâmetro

As predefinições de parâmetro oferecem ao usuário a capacidade de armazenar e transferir grandes quantidades de valores pré-configurados para um conjunto de parâmetros.Eles podem ajudar em muitos cenários e são mais úteis quando uma grande quantidade de parâmetros com uma grande variedade de possibilidades está presente.

Há duas maneiras de armazenar e carregar predefinições. Ambas têm casos de uso diferentes, detalhados abaixo.

![Menu suspenso Carregar/Salvar predefinição](../../../assets/preset-menu.gif "Menu suspenso Carregar/Salvar predefinição"){width="512px"}

## Predefinições externas

As predefinições externas envolvem um arquivo externo no disco e um arquivo \*.SBSPRS. Eles podem ser transferidos entre diferentes gráficos e nós, mas somente dentro do aplicativo. O seu principal objetivo é exatamente este: transferir um número de valores demasiado grande para copiar um por um.

As predefinições externas estão disponíveis para todos os Parâmetros Específicos em [Instâncias de Gráfico](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md), para a maioria dos Parâmetros Específicos em [nós Atômicos](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md) ([as exceções são aqueles parâmetros que não podem ser expostos](../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)) e para os parâmetros de entrada expostos em um gráfico de Substance [parâmetros](../../graph-parameters/graph-parameters.md)parâmetros.

Eles são simplesmente salvos e carregados através deste menu. Os arquivos SBSPRS salvos podem ser carregados em qualquer outro nó ou gráfico.

>[!NOTE]
>
> Mesmo correspondências parciais funcionarão: os parâmetros armazenados em um SBSPRS que não existem no nó carregado, serão simplesmente ignorados. Isso significa que você pode transferir propriedades entre nós que são mais semelhantes, [como a versão colorida e em tons de cinza do Tile Sampler](../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)! Todos os parâmetros compartilhados serão carregados. A correspondência ocorre no identificador e no tipo.

![Edição de predefinições incorporadas](../../../assets/preset-embed.gif "Edição de predefinições incorporadas"){width="512px"}

## Predefinições incorporadas

As predefinições incorporadas funcionam de maneira diferente das predefinições externas. Sua principal vantagem é que eles estão contidos no arquivo SBS ou SBSAR, para que possam ser facilmente transferidos e carregados no Substance Painter, Maya e 3DS Max (atualmente não disponível no Substance 3D Sampler, UE4 e Unity). O usuário também não precisa mexer com arquivos SBSPRS.

Eles servem para um propósito diferente: não é possível transferi-los entre nós e gráficos (você teria que usar Predefinições externas para isso). Eles também podem ser criados somente nos Parâmetros de entrada das propriedades de um gráfico e somente no Modo de visualização.

O fluxo de trabalho é o seguinte:

1. Alternar para <b>Modo de visualização</b> para os <b>Parâmetros de entrada</b>
1. Definir valores para o resultado desejado
1. Clique em <b>+</b> ao lado do menu suspenso de predefinições para criar uma nova predefinição incorporada. Em seguida, a predefinição é imediatamente criada e armazenada

As predefinições incorporadas não podem ser modificadas posteriormente, embora possam ser renomeadas. Modificá-las e removê-las acontecem clicando no ícone de engrenagem ao lado do menu suspenso e do ícone +. Pressione o sinal de menos ao lado de uma predefinição para removê-la.

Nada mais precisa ser feito para ativar as predefinições: uma vez publicadas como SBSAR, suas predefinições estarão disponíveis no Substance Painter após a importação.

>[!IMPORTANT]
>
> A guia <b>Predefinições</b> é desabilitada ao usar a [edição do contexto](../../../interface/preferences-window/preferences-window.md).
