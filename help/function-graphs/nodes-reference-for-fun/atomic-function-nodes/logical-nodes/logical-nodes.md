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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---


# Nós lógicos

Os nós lógicos são usados para adicionar várias condições ao seu gráfico:

![](logical-nodes.resources/logical-nodes-01.png)

## O nó *And*

![](logical-nodes.resources/logical-nodes-02.png)

O nó And usa dois nós Booleanos como entrada:

* Se ambas as entradas forem True, a saída do nó *And* será *True*
* Em qualquer outro caso, o nó *And* retornará *False*

## O nó *Ou*

![](logical-nodes.resources/logical-nodes-03.png)

O nó Or usa dois nós booleanos como entrada:

* Se pelo menos uma das entradas for True (1), a saída do nó *Or* será *True*
* Se ambas as entradas forem False, o nó *Or* retornará *False*

## O nó *Não*

![](logical-nodes.resources/logical-nodes-04.png)

O nó Not assume um booleano como entrada: ele examinará o valor de entrada e retornará seu oposto:

* A entrada *Verdadeira* fornece saída *falsa*
* A entrada *Falso* fornece a saída *Verdadeira*
