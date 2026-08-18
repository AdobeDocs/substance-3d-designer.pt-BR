---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/function-graphs/what-is-a-function.html"
breadcrumb-title: ''
description: Saiba quais funções existem no Substance 3D Designer e como usá-las para criar redes de nós reutilizáveis.
helpx_creative_field: ""
helpx_description: "Designer > Function graphs > What is a function "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 'O que é uma função '
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# O que é uma função?

As funções no Substance 3D Designer permitem que o usuário gere resultados usando a lógica que, de outra forma, seria encontrada em uma linguagem de programação.

Mas, em vez de usar linhas de códigos, as funções no Designer mantêm a mesma abordagem nodal. À primeira vista, um gráfico de função parece muito semelhante a um gráfico regular.

![](../../assets/image2015-12-17-18-19-37.png)

Você pode encontrar funções em dois casos principais:

* para controlar o resultado de um parâmetro
* se você editar um processador de pixel

## Controle o resultado de um parâmetro

No Substance 3D Designer, qualquer parâmetro pode ser controlado por uma função.

![](../../assets/image2015-12-17-21-3-46.png)

Portanto, você pode imaginar regras e dependências entre partes do seu gráfico, para obter resultados únicos.

Por exemplo, você pode decidir que a opacidade de um nó de mesclagem será metade da intensidade de um nó de distorção:

![](../../assets/warpblend.gif)

Na verdade, você já pode ter criado funções sem estar ciente delas:

se você expôs um parâmetro, criou automaticamente uma função e uma variável: a função contém um nó get float que captura o valor da variável recém-criada:

![](../../assets/expose.gif)
