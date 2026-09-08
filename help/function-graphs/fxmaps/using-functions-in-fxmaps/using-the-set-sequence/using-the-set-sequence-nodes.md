---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence-nodes.html"
breadcrumb-title: ''
description: Saiba como usar nós SetSequence em FXMaps para criar padrões sequenciais e variações de procedimentos.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Using the SetSequence nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Usando os nós SetSequence
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '773'
ht-degree: 0%

---


# Usando os nós Conjunto/Sequência

Esta página descreve os nós **Conjunto** e **Sequência** e fornece um caso de uso de exemplo no contexto de **FX-Maps**.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Visão geral

Ao trabalhar com funções no <b>FX-Maps</b>, você estará ocasionalmente em situações em que deseja gerar um valor a partir do *[gráfico de função Substance](../../../../function-graphs/the-function-graph/the-function-graph.md)* de um parâmetro para que possa *usá-lo em outro.* Mas, por padrão, um gráfico de função de Substance só gera o valor *um*: aquele que orienta o parâmetro relacionado.

</td>
<td style="border: 0;" valign="top">

![Nós de definição e sequência](../../../../assets/image2017-3-17-15-5-5.png "Nós de definição e sequência")

</td>
</tr>
</table>

Nesse caso, você pode usar a combinação dos nós <b>Conjunto</b> e <b>Sequência</b>, o que permitirá controlar variáveis em uma ou várias funções.

Esse processo envolve duas etapas:

1. O nó <b>Definir</b> permitirá que você crie uma nova variável para que você possa chamá-la em outro lugar e atribuir um valor a ela.
1. O nó <b>Sequência</b> é usado para executar a lógica na etapa 1 em sua totalidade, *antes de executar outra ramificação* do gráfico - por exemplo, a lógica realmente envolvida na saída do valor esperado para o gráfico atual

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

## O nó Set

O nó <b>Definir</b> permite que você defina uma nova variável e atribua a ela o tipo e o valor conectados à *entrada* do nó.

O *nome* da variável é inserido pelo usuário nas propriedades do nó.

Por padrão, a variável definida por este nó é *somente* acessível dentro do escopo do *pai* deste gráfico de função de Substance - por exemplo, o nó que hospeda o parâmetro definido pela função.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Definir nó](../../../../assets/image2017-3-17-15-12-52.png "Definir nó")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Neste exemplo, o nome da variável foi definido como **`myVariable`** e seu valor é **1**.

</td>
<td style="border: 0;" valign="top">

![Definir exemplo de nó](../../../../assets/image2018-8-30-17-45-35.png "Definir exemplo de nó")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

## O nó Sequência

O nó <b>Sequência</b> oferece controle sobre o *fluxo de execução* dos gráficos de função Substance, garantindo que a *primeira ramificação seja totalmente executada antes da segunda ramificação*.

A saída da *segunda ramificação* é passada para a saída do nó.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Nó de sequência](../../../../assets/image2017-3-17-15-17-38.png "Nó de sequência")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Neste exemplo, o nó <b>Sequência</b> é definido como a saída do gráfico. A saída da função é, portanto, a saída do valor <b>0.5</b> pelo nó <b>Float</b>.

No entanto, antes que isso aconteça, a variável `<b>myVariable</b>` é definida com um valor de flutuação de <b>1.0</b>. Esta variável pode ser usada *em outro local* no contexto do nó.

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó de sequência](../../../../assets/image2018-8-30-17-49-41.png "Exemplo de nó de sequência")

</td>
</tr>
</table>

Os nós de **sequência** podem ser *encadeados* para controlar o fluxo de execução do gráfico.

Por exemplo, você pode *definir* uma variável primeiro, *atualizar* seu valor em um ponto posterior e *ler* seu valor final, enquanto garante que essas ações ocorram *em uma ordem específica*.

![Nó de sequência encadeado](../../../../assets/image2018-8-30-17-52-27.png "Nó de sequência encadeado")

## Visibilidade variável

Lembre-se de que uma variável declarada é *não* acessível de qualquer lugar!\
Embora uma variável declarada em um nível pai possa ser acessível em níveis filho, o contrário é *não verdadeiro*.

Assim, as variáveis definidas no nó são *não* acessíveis no nível do gráfico, enquanto as variáveis definidas no nível do gráfico *podem* ser acessadas nas funções de parâmetro do nó.

Por exemplo, esta regra está no cerne da *exposição de um parâmetro*, pois a exposição envolve estas etapas:

1. Criação de um parâmetro de entrada de gráfico
1. Acessá-lo no gráfico de função Substance do parâmetro
1. Definindo seu valor como a saída da função

Vamos construir um pequeno exemplo: imagine que queremos que o valor de <b>Rotação</b> de um nó <b>Quadrante</b> seja influenciado pelo valor de <b>Cor/Luminosidade</b>: quanto mais brilhante for a luminosidade, mais rotação.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

O que faremos é realizar todo o cálculo na função de parâmetro <b>Cor/Luminosidade</b>. Este parâmetro será calculado *primeiro*, portanto qualquer variável definida nele estará disponível para os outros parâmetros de nó.

</td>
<td style="border: 0;" valign="top">

![Propriedades do quadrante](../../../../assets/image2018-8-30-18-1-6.png "Propriedades do quadrante")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Nossa função será simples: a luminosidade será um valor aleatório entre **0** e **1**. Esse valor será armazenado na variável `myRotation`. Em seguida, definimos o valor como a saída da função.

Isso significa que o valor do parâmetro **Cor/Luminosidade** será aleatório *e* será armazenado na variável `myRotation`.

Observe que a propriedade **Position** já está definida por um valor aleatório, e um nó **Iterate** é usado para obter vários padrões posicionados aleatoriamente.

</td>
<td style="border: 0;" valign="top">

![Função de Cor/Luminosidade do quadrante](../../../../assets/image2018-8-30-18-4-46.png "Função de Cor/Luminosidade do quadrante")

</td>
</tr>
</table>

![Padrões dispersos](../../../../assets/image2018-8-30-18-5-30.png "Padrões dispersos")

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Agora que a variável `myRotation` existe e tem um valor, vamos acessar o gráfico de função Substance da propriedade <b>Rotação de Padrão</b>.

</td>
<td style="border: 0;" valign="top">

![Menu de função de parâmetro da rotação de padrão](../../../../assets/image2018-8-30-18-7-57.png "Menu de função de parâmetro da rotação de padrão")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Na função, lemos o valor do parâmetro `myRotation` usando um nó **Get Float** - sabemos que a variável contém um valor float - e o definimos como a saída da função.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Saída de Get float da rotação do padrão](../../../../assets/image2018-8-30-18-10-58.png "Saída de Get float da rotação do padrão")

</td>
</tr>
</table>

A luminosidade agora também controla a rotação.

![Padrões girados](../../../../assets/image2018-8-30-18-12-25.png "Padrões girados")
