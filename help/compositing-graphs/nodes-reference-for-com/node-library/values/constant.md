---
helpx_url: ""
breadcrumb-title: ''
description: Acesse nós de constante no Substance 3D Designer para definir valores constantes em gráficos de Substance.
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Constante
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---


# Constante

Nós constantes são uma maneira de criar um valor estático para uso dentro de gráficos de Substance.

Você pode localizar esses nós na seção **Valores > Constantes** da Biblioteca.\
Todos eles incluem um nó [Processador de valor](../../atomic-nodes/value-processor/value-processor.md) simples que gera o valor.

+++ Nós constantes na biblioteca

![constants-library.png](constant.resources/constants-library.png)

+++

<p style="text-align: center;"><img src="./constant.resources/constants-float-01.png" alt="Nó de Precisão decimal constante" /></p>

## Inteiros

Inteiros constantes geram números inteiros e têm uma etapa de 1.

[Eles podem ser convertidos em Float](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md), o que é recomendado ao executar qualquer operação mais complexa do que adições, subtrações e comparações simples.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Ícone de tipo inteiro](../../../../assets/fn-constant-integer.png "Ícone de tipo inteiro")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Inteiro</b>

Um inteiro possui um único componente. É útil como um índice para fazer seleções, como:

* selecionando uma opção apresentada ao usuário como um menu suspenso (consulte &#39;Lista suspensa&#39; em [esta página](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)).
* selecionando a entrada de um nó [Multi switch](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md).<b></b>

>[!IMPORTANT]
>
> <b>Não há suporte para *inteiros negativos</b> em funções de parâmetro*. Consulte [esta página](../../../../technical-issues/parameters-not-working/parameters-not-working-as-expected.md) na seção “Problemas técnicos” para obter uma solução alternativa.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Ícone de tipo Integer2](../../../../assets/fn-constant-integer2.png "Ícone de tipo Integer2")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Inteiro2</b>

Um nó Integer2 gera um vetor inteiro estático de 2 componentes com componentes (X, Y).

Um caso de uso comum de Integer2 é definir os tamanhos de grade X e Y, como no nó [Tile Generator](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Ícone de tipo Integer3](../../../../assets/fn-constant-integer3.png "Ícone de tipo Integer3")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Inteiro3</b>

Um nó Integer3 gera um vetor inteiro estático de 3 componentes com componentes (X, Y, Z).

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Ícone de tipo Integer4](../../../../assets/fn-constant-integer4.png "Ícone de tipo Integer4")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Inteiro4</b>

Um nó Integer4 gera um vetor inteiro estático de 4 componentes com componentes (X, Y, Z, W).

</td>
</tr>
</table>

## Flutuações

Os valores de Precisão decimal constantes geram números fracionários, ou seja, eles oferecem suporte a valores após o sinal decimal e podem ser ajustados em etapas menores que 1. (Padrão: 0,01)

[As flutuações podem ser convertidas em inteiros](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md), mas serão arredondadas para cima ou para baixo até o inteiro mais próximo, significando que dados e precisão serão perdidos.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Ícone de tipo flutuante](../../../../assets/fn-constant-float.png "Ícone de tipo flutuante")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Flutuante</b>

Uma Precisão decimal tem um único componente e é muito usada para qualquer valor único que exija precisão.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Ícone de tipo Float2](../../../../assets/fn-constant-float2.png "Ícone de tipo Float2")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Flutuante2</b>

Um nó Precisão decimal2 gera um vetor de 2 componentes com componentes (X, Y).

A Precisão decimal 2 é geralmente usada para [coordenadas de amostragem](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md), [transformações de deslocamento](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/transforms.md) e manipulação geral de vetor 2D.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Ícone de tipo Float3](../../../../assets/fn-constant-float3.png "Ícone de tipo Float3")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Flutuante3</b>

Um nó Precisão decimal3 gera um vetor de 3 componentes (X, Y, Z).

O Precisão decimal3 é usado principalmente ao trabalhar com objetos 3D e [coordenadas de escala 3D](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md), como em [nós SDF 3D](../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions), e como uma maneira mais simples de armazenar cores RGB, ou seja, sem Alpha.

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Ícone de tipo Float4](../../../../assets/fn-constant-float4.png "Ícone de tipo Float4")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Flutuante4</b>

Uma Precisão decimal 4 gera um vetor de 4 componentes (X, Y, Z, W).

A Precisão decimal 4 é a maneira preferencial de armazenar e definir informações de cores nas quais os valores XYZW são mapeados para RGBA, como no [nó de Cor uniforme](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md).

</td>
</tr>
</table>

## Não numérico

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Ícone de tipo booliano](../../../../assets/fn-constant-boolean.png "Ícone de tipo booliano")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Booleano</b>

Um booleano é o tipo de dados mais simples que existe, conhecendo apenas dois estados: <code>true</code> ou <code>false</code>.

Esse tipo é bastante comum ao trabalhar com parâmetros de alternância e condições [If/Else](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/control-nodes/control-nodes.md).<br>Booleanos são uma maneira simples e eficiente de controlar o fluxo de uma função ou gráfico, por exemplo, usando um [Nó de Switch](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md).

</td>
</tr>
</table>
