---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/what-is-a-function.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# O que é uma função?

As funções no Substance 3D Designer permitem que o usuário gere resultados usando a lógica que, de outra forma, seria encontrada em uma linguagem de programação.

Mas, em vez de usar linhas de códigos, as funções no Designer mantêm a mesma abordagem nodal. À primeira vista, um gráfico de função parece muito semelhante a um gráfico regular.

![](what-is-a-function.resources/what-is-a-function-01.png)

Você pode encontrar funções em dois casos principais:

* para controlar o resultado de um parâmetro
* se você editar uma processador de pixels

## Controle o resultado de um parâmetro

No Substance 3D Designer, qualquer parâmetro pode ser controlado por uma função.

![](what-is-a-function.resources/what-is-a-function-02.png)

Portanto, você pode imaginar regras e dependências entre partes do seu gráfico, para obter resultados únicos.

Por exemplo, você pode decidir que a opacidade de um nó de mesclagem será metade da intensidade de um nó de distorção:

![](what-is-a-function.resources/what-is-a-function-03.gif)

Na verdade, você já pode ter criado funções sem estar ciente delas:

se você expôs um parâmetro, criou automaticamente uma função e uma variável: a função contém um nó get float que captura o valor da variável recém-criada:

![](what-is-a-function.resources/what-is-a-function-04.gif)
