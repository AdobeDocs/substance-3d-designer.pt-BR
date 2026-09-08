---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/function-graphs/variables/get-a-variable-value.html"
breadcrumb-title: ''
description: Saiba como recuperar valores de variáveis nos gráficos de função do Substance 3D Designer usando o nó Obter variável.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Get a variable value
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Obter um valor de variável
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---


# Obter um valor de variável

Para usar uma variável em uma função, você precisa “chamá-la”, o que significa que precisa importar o valor da variável para a função.

Para fazer isso, você precisa usar um nó *Get*:

![](../../../assets/image2015-12-21-7-29-51.png)

Há diferentes tipos de nós Obter: escolha o correto de acordo com o tipo de valor que deseja importar:

![](../../../assets/image2015-12-21-7-31-4.png)

## Atribuir uma variável a um nó Get

Por padrão, um nó get exibirá um sinal de aviso: significa que ainda não está vinculado a nenhuma variável.

Para vincular uma variável, vá para os parâmetros e escolha uma variável na lista “Variáveis/Obter \*\*\*” (\*\*\*será substituído pelo tipo de valor que o nó Obter pode chamar).

O nome da variável será exibido no nó:

![](../../../assets/assign-getfloat.gif)

Observe que apenas as variáveis que são do mesmo tipo do nó Get aparecerão na lista.

>[!WARNING]
>
> Observe que as variáveis criadas com um nó *Set* não aparecerão em uma lista de nós *Get*.
> 
> Mas você ainda pode obter a variável escrevendo manualmente o nome na lista.
> 
> Não se esqueça de que você pode simplesmente chamar uma variável criada com um nó Set, se:
> 
> * Os nós Obter e Definir estão em gráficos de função que controlam parâmetros de um mesmo nó
> * O parâmetro controlado pelo gráfico de nó *Get* é o mesmo ou está localizado abaixo do parâmetro do gráfico de nó *Set*, na pilha de parâmetros.
