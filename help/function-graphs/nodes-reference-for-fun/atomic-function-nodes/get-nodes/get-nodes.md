---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/get-nodes.html"
breadcrumb-title: ''
description: Acesse os nós Obter nos gráficos de função do Substance 3D Designer para recuperar valores de variáveis e dados.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Variáveis
user-guide-description: ''
user-guide-title: ''
source-git-commit: f28a2ba2531cfc4456744ff151432ed8308275ec
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 6%

---


# Variáveis

Variáveis são uma forma de <b>armazenar valores</b> para buscá-los posteriormente (<b>Obter</b>) e/ou modificá-los (<b>Definir</b>).

![gráfico de função Substance - Obter gráfico de função float](get-nodes.resources/assign-getfloat.gif "Substance - Obter float"){zoomable="yes"}

O que um nó Get essencialmente faz é pegar uma variável dinâmica e retorná-la a partir da saída Get Nodes para uso em uma função. Estes nós Get formam o vínculo entre os Parâmetros de Entrada definidos nos [parâmetros de gráfico](../../../../compositing-graphs/graph-parameters/graph-parameters.md) e nas [funções de parâmetro](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md).

Sempre que usar um nó Obter, você deverá selecionar um valor disponível no menu suspenso. Obter nós <b>obterá um valor do tipo correspondente</b>. Isso significa que você verá apenas as opções válidas no menu de um nó Obter; nunca será possível escolher uma opção inválida. Se uma variável não estiver disponível, isso significa que há uma incompatibilidade de tipos

Há um número de <b> Variáveis “Sistema”</b>: variáveis especiais predefinidas que você não pode se declarar. Estes são bastante importantes e para os nós abaixo é listado quais variáveis do sistema estão disponíveis.

Quando um parâmetro é [exposto](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), ele consiste em aplicar uma função de parâmetro nele que inclua apenas um nó Get do tipo correto.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Obter

</td>
<td style="border: 0;" valign="top">

### Definir

</td>
<td style="border: 0;" valign="top">

### É definido

</td>
</tr>
</table>

## Obter

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Obter flutuação2 - Ícone](get-nodes.resources/fn_variables_getfloat2.png "Obter flutuação2 - Ícone"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Esses nós permitem buscar o valor de uma variável que existe *no escopo atual*.

O nome da variável que está sendo buscada é definido na área de Propriedades.

</td>
</tr>
</table>

Nós &#39;Get&#39; algumas limitações que você precisa ter em mente:

* <b>Eles são digitados</b>, portanto, é necessário verificar se a variável contém um valor do mesmo tipo que o nó. As inconsistências de tipo são relatadas no Console.
* <b>Eles não verificam a existência da variável</b> no escopo atual. Variáveis não encontradas são relatadas no Console.
* Em funções complexas que usam nós de fluxo de controle, como Sequência, tenha cuidado com a <b>ordem na qual você define e obtém variáveis</b>. Quando o Designer detecta um caso de “Obter antes de definir”, ele é relatado no Console.

>[!NOTE]
>
> Variáveis internas
> 
> Vários nós &#39;Get&#39; oferecerão variáveis internas para acessar valores existentes de acordo com o contexto atual - por exemplo: a posição atual do pixel em um Processador de pixels, o modo de divisão em blocos gráficos atual de um nó, ...
> 
> Todas as variáveis internas estão listadas em [esta página dedicada](../../../../function-graphs/variables/system-variables/system-variables.md).

### Obter nós

+++Flutuações
![Obter flutuação - Ícone](get-nodes.resources/fn_variables_getfloat.png "Obter flutuação - Ícone"){width="200px"}



Obter Float

![Obter flutuação2 - Ícone](get-nodes.resources/fn_variables_getfloat2.png "Obter flutuação2 - Ícone"){width="200px"}



Obter Float2

![Obter flutuante3 - Ícone](get-nodes.resources/fn_variables_getfloat3.png "Obter flutuante3 - Ícone"){width="200px"}



Obter Float3

![Obter flutuação4 - Ícone](get-nodes.resources/fn_variables_getfloat4.png "Obter flutuação4 - Ícone"){width="200px"}



Obter Float4

+++

+++Inteiros
![Obter inteiro - Ícone](get-nodes.resources/fn_variables_getint.png "Obter inteiro - Ícone"){width="200px"}



Obter Integer

![Obter inteiro2 - Ícone](get-nodes.resources/fn_variables_getint2.png "Obter inteiro2 - Ícone"){width="200px"}



Obter Integer2

![Obter inteiro3 - Ícone](get-nodes.resources/fn_variables_getint3.png "Obter inteiro3 - Ícone"){width="200px"}



Obter Integer3

![Obter inteiro4 - Ícone](get-nodes.resources/fn_variables_getint4.png "Obter inteiro4 - Ícone"){width="200px"}



Obter Integer4

+++

+++Outros
![Obter booleano - Ícone](get-nodes.resources/fn_variables_getboolean.png "Obter booleano - Ícone"){width="200px"}



Obter booleano

![Obter cadeia de caracteres - Ícone](get-nodes.resources/fn_variables_getstring.png "Obter cadeia de caracteres - Ícone"){width="200px"}



Obter string

+++

## Definir

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Definir: ícone de nó](get-nodes.resources/fn_variables_set.png "Definir: ícone de nó"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Texto

</td>
</tr>
</table>

## É definido

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Está definido: ícone de nó](get-nodes.resources/fn_variables_isdefined.png "Está definido: ícone de nó"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Texto

</td>
</tr>
</table>
