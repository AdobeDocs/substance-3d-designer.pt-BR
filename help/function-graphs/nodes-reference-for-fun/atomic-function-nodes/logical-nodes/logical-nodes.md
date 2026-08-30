---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/logical-nodes.html"
breadcrumb-title: ''
description: Acessar nós lógicos em gráficos de funções do Substance 3D Designer para executar operações e comparações de lógica booleana.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Logical
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lógico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---


# Nós lógicos

Os nós lógicos são usados para adicionar várias condições ao seu gráfico:

![](logical-nodes.resources/image2015-12-23-11-23-21.png)

## O nó *And*

![](logical-nodes.resources/image2015-12-23-11-30-9.png)

O nó And usa dois nós Booleanos como entrada:

* Se ambas as entradas forem True, a saída do nó *And* será *True*
* Em qualquer outro caso, o nó *And* retornará *False*

## O nó *Ou*

![](logical-nodes.resources/image2015-12-23-11-30-44.png)

O nó Or usa dois nós booleanos como entrada:

* Se pelo menos uma das entradas for True (1), a saída do nó *Or* será *True*
* Se ambas as entradas forem False, o nó *Or* retornará *False*

## O nó *Não*

![](logical-nodes.resources/image2015-12-23-11-31-46.png)

O nó Not assume um booleano como entrada: ele examinará o valor de entrada e retornará seu oposto:

* A entrada *Verdadeira* fornece saída *falsa*
* A entrada *Falso* fornece a saída *Verdadeira*
