---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/font-resource.html"
breadcrumb-title: ''
description: Importe e use recursos de fonte no Substance 3D Designer para adicionar texto e tipografia aos materiais.
helpx_creative_field: ""
helpx_description: Designer > Resources > Font resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Recurso de fonte
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# Recurso de fonte

Os Recursos de Fonte devem ser usados junto com o [nó de Texto atômico](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md). Eles permitem que você use fontes que não estão instaladas no sistema ao fazer referência a um arquivo de fonte em qualquer lugar do disco.

>[!NOTE]
>
> **Fontes em SBSAR**
> 
> As fontes são sempre incorporadas em um SBSAR, independentemente se forem de um recurso vinculado ou usando uma fonte instalada pelo sistema. A vantagem deste método é que não há necessidade de instalar e, ao exportar um arquivo SBS com dependências, você pode ter certeza de que os arquivos de fonte vêm junto.

## Uso de recursos de fonte personalizados

* Clique com o botão direito em um pacote, escolha <b>Link > Fonte</b>
* Selecione um arquivo .otf ou .ttf.
* Coloque um [Nó de texto](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) no [gráfico](../../compositing-graphs/substance-compositing-graphs.md).
* Na propriedade <b>Fonte </b>, todos os recursos de fonte estarão na parte superior da lista.

Observe que a lista de fontes não é atualizada automaticamente com as propriedades abertas. Você terá que alternar para outra janela de propriedade e voltar para um nó Texto para ver as fontes recém-vinculadas.
