---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/importing-linking-and-new-resources.html"
breadcrumb-title: ''
description: Saiba como importar, vincular e criar novos recursos no Substance 3D Designer para seus projetos de material.
helpx_creative_field: ""
helpx_description: Designer > Resources > Importing, linking and new resources
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Importação, vinculação e novos recursos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0b8b2d2c05587d7fe84a71bb54244a492540d6dc
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 2%

---


# Importação, vinculação e novos recursos

O [Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html) oferece suporte a três modos de trazer ou criar novos recursos para uso no seu gráfico. Esses recursos podem ser de muitos tipos diferentes, incluindo, mas não se limitando a [bitmaps](../../resources/bitmap-resource/bitmap-resource.md), [gráficos vetoriais](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md), [cenas 3D](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/3d-mesh-resource-200574577.html)e [fontes](../../resources/font-resource/font-resource.md). Esta página explica os diferentes métodos e quando cada um é melhor usado.

Todos os métodos são acessados [clicando em RMB em um pacote no Explorer](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)[.](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)

A tabela a seguir fornece uma rápida visão geral da diferença nas funcionalidades entre os métodos.

|                                                                                                                                                                         | Novo | Importar | Vincular |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Gráficos ([gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md), [gráficos de função de Substance](../../function-graphs/function-graphs.md) | <div><img alt="(assinalar)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(erro)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(erro)" data-preserve-html="true" src="../../assets/error.svg"/></div> |
| [Bitmaps](../../resources/bitmap-resource/bitmap-resource.md),[ gráficos vetoriais (SVG)](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) | <div><img alt="(assinalar)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(assinalar)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(assinalar)" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| [Cenas 3D](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/3d-mesh-resource-200574577.html), [fontes](../../resources/font-resource/font-resource.md) | <div><img alt="(erro)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(erro)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(assinalar)" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| É criado ao lado do arquivo SBS | <div><img alt="(assinalar)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(assinalar)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(erro)" data-preserve-html="true" src="../../assets/error.svg"/></div> |
| Editável no Designer | <div><img alt="(assinalar)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(assinalar)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(erro)" data-preserve-html="true" src="../../assets/error.svg"/></div> |
| As edições externas são sincronizadas automaticamente | <div><img alt="(erro)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(erro)" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="(assinalar)" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| Incorporado no SBSAR publicado | <div><img alt="(assinalar)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(assinalar)" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="(assinalar)" data-preserve-html="true" src="../../assets/check.svg"/></div> |

## Novos recursos

Criar um novo recurso significa que um recurso no pacote será criado do zero. Todos os recursos somente do Designer só podem ser criados dessa maneira, como gráficos de Substance e gráficos de função de Substance.

Um caso especial é quando você cria um novo [bitmap](../../resources/bitmap-resource/bitmap-resource.md)ou [SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md): esses arquivos serão exibidos no Explorer e se comportarão como um recurso importado, mas sem exigir um arquivo externo. Eles podem ser modificados no Designer. Novos bitmaps e SVG criados dessa maneira são bons se você não precisa depender de um editor externo: por exemplo, quando você deseja apenas uma forma vetorial rápida e simples ou uma máscara de bitmap 2D pintada simples.

## Recursos importados

Importar um recurso significa que uma duplicata do arquivo de recurso será criada ao lado do seu arquivo SBS (na pasta *Graphname*.resources), [exceto para arquivos SVG](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md). Às vezes, também é referenciado como &#39;incorporando&#39; um recurso.

Um recurso importado pode ser editado no Designer usando as [ferramentas de pintura de bitmap](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md) ou as [ferramentas de edição de vetores](../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md) na [exibição 2D](../../interface/2d-view/2d-view.md), depois de inserido no gráfico. Os recursos importados não estão mais vinculados aos arquivos de origem originais: ou seja, se você alterar, remover ou atualizar o arquivo importado originalmente, isso não terá efeito sobre o recurso no Designer.

No caso de [arquivos AxF](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md), o processo é um pouco mais complicado; gráficos de Substance e recursos de bitmap são criados a partir do pacote AxF. No entanto, todos eles ainda podem ser editados em seus respectivos editores: visualização de gráfico ou visualização 2D.

>[!WARNING]
>
> Para novos pacotes, os recursos importados e novos não são salvos em disco até que você salve o pacote.

## Recursos vinculados

Vincular um recurso significa que o Designer fará referência ao arquivo de origem em seu local original no disco, mas ainda o apresentará no Explorer como se ele fizesse parte do seu pacote. Você não poderá editar o recurso real diretamente no Designer, apenas usá-lo como um componente no seu gráfico ou como uma fonte para mapas de culinária.

A vinculação é ideal se você sabe que precisará usar um editor externo para atualizar seu recurso enquanto trabalha simultaneamente no Designer. Mapas de cozimento é um exemplo importante: você pode ter bitmaps de referência do Designer de um aplicativo de cozimento externo, que recarregará e atualizará automaticamente o seu gráfico assim que esses arquivos forem alterados. Da mesma forma, as cenas 3D só podem ser vinculadas, portanto, sempre que você exportar um novo arquivo FBX de seu aplicativo 3D, o Designer atualizará automaticamente a malha usada na exibição 3D. Se você estiver preparando mapas a partir desta malha, terá que iniciar manualmente o processo de cozimento novamente, de preferência clicando em RMB e selecionando &#39;Atualizar todos os mapas baked&#39;.

## Excluindo recursos

Ao excluir um recurso de um pacote, a caixa de diálogo <b>Confirmar remoção do item</b> é exibida. Se algum item no processo de remoção for *referenciado por outros recursos* - como [instâncias de gráfico](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md) e [recursos de bitmap](../../resources/bitmap-resource/bitmap-resource.md) usados em [gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md) - a caixa de diálogo incluirá um *aviso e uma lista* desses itens.

>[!NOTE]
>
> Recomendamos ter cuidado com esses itens e tomar as ações necessárias para *antecipar quaisquer dependências quebradas* que resultariam da exclusão de itens de um pacote.\
> Essas ações podem incluir *remoção de todos os usos* desses recursos antes da exclusão.

![&#39;Recurso excluído em uso&#39; aviso](../../assets/confirm-item-removal.png "&#39;Recurso excluído em uso&#39; aviso"){width="512px"}
