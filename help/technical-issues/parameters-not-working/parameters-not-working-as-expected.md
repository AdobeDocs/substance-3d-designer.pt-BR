---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/technical-issues/parameters-not-working-as-expected.html"
breadcrumb-title: ''
description: Solucione problemas com parâmetros do gráfico de Substance que não funcionam como esperado e encontre soluções.
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Parameters not working as expected
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Os parâmetros não estão funcionando como esperado
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 5%

---


# Os parâmetros não estão funcionando como esperado

Esta página lista causas comuns para parâmetros que não funcionam como esperado no Substance 3D Designer e oferece etapas de solução de problemas para cada um.

## O parâmetro não está funcionando no modo Visualizar e o ativo do Substance 3D publicado (SBSAR)

<b>![(erro)](../../assets/error.svg) Problema</b>

Alguns parâmetros expostos para um gráfico *não estão listados* ao usar o [modo de visualização](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) no Designer ou na lista de parâmetros de [ativos do Substance 3D](https://helpx.adobe.com/br/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html) (SBSAR) publicados fora desse gráfico.

<b>![(tick)](../../assets/check.svg)Etapas recomendadas</b>

Os parâmetros ausentes são provavelmente [parâmetros estáticos](../../glossary/glossary.md), que *não podem ser editados dinamicamente* depois que o gráfico foi *preparado* - isto é, processado para executar seu algoritmo de forma rápida e eficiente. A cozinha ocorre no Designer sempre que o gráfico é *editado* ou *publicado*. Os parâmetros afetados por essas limitações estão listados na seção [Limitações](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) da página [Expondo um parâmetro](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) desta documentação.

Portanto, os parâmetros estáticos são visíveis e editáveis no Designer, mas estão *ocultos* em um ativo publicado do Substance 3D. Você pode usar o [Modo de visualização](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) para ver essas limitações em vigor antes de publicar em um ativo do Substance 3D.

Veja uma lista de parâmetros estáticos:

| Nó | Parâmetro |
| --- | --- |
| Todos os nós | Proporção de pixel no modo de divisão em blocos gráficos |
| [Cor uniforme](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md) | Modo de cores |
| [Processador de pixels](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) | Modo de cores |
| [Mesclar](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) | Modo de mesclagem Alpha área de corte de mesclagem |
| [FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) | Modo de mesclagem |
| [Quadrante](../../function-graphs/fxmaps/the-quadrant-node/the-quadrant-node.md) | Filtragem de imagem de entrada alfa da imagem de entrada de padrão |

## Resultado incorreto para gráfico de função Substance aplicado ao parâmetro

<b>![(erro)](../../assets/error.svg) Problema</b>

Um gráfico de função Substance aplicado a um parâmetro de nó não gera o valor esperado quando um inteiro negativo é usado.

<b>![(tick)](../../assets/check.svg) Etapas recomendadas</b>

No momento, não há suporte adequado para inteiros negativos. Como solução alternativa, use o valor inteiro negativo em um valor [Inteiro2](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) e extraia-o usando um nó [Inteiro do Swizzle](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md).
