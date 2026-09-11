---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/using-the-sampler-nodes.html"
breadcrumb-title: ''
description: Saiba como usar nós de amostra no FXMaps para obter texturas de amostra e criar variações de material processuais.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Using the Sampler nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Usando os nós do Sampler
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4e61f5588fb279e139240ac5939d6b7e58e1027a
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# Usando os nós do Sampler

![](using-the-sampler-nodes.resources/sampler-graph.jpg)

O nó amostrador pode ser usado para obter amostras de valores de pixel em uma entrada de imagem conectada ao nó fx-map. Os valores amostrados podem então ser usados para orientar quaisquer parâmetros usando funções.

## Exemplo simples

Neste exemplo, uma cadeia de nós de quadrante foi criada para gerar uma grade de padrão. Uma função é criada no parâmetro Opacidade/luminância do último quadrante.

![](using-the-sampler-nodes.resources/sampler-function.jpg){width="300px"}![](using-the-sampler-nodes.resources/sampler-result-1.jpg){width="300px"}

O nó Sample obtém uma entrada float2 como as coordenadas de amostragem (x, y). Neste exemplo, usamos a variável $pos: para cada padrão, o valor do pixel é amostrado na posição do padrão na primeira entrada da imagem conectada ao nó FxMap.

O nó Cinza de amostra retorna um valor float1 no intervalo 0, 1.

O nó Cor de amostra retorna um valor float4 (rgba) no intervalo 0, 1.

## Exemplo avançado

Aqui, comparamos o valor amostrado a uma constante (0,3). Se o valor amostrado for maior que 0,3, a função retornará 1; caso contrário, retornará 0.

![](using-the-sampler-nodes.resources/sampler-function-advanced.jpg){width="300px"}![](using-the-sampler-nodes.resources/sampler-result-advanced.jpg){width="300px"}

## Baixar amostra

[![Ícone de arquivo SBS](using-the-sampler-nodes.resources/sbs-1_1.png){width="64px"}](https://shared-assets.adobe.com/link/d5f9adf3-0bb5-49a1-4eb9-a0506d4f3f32)
