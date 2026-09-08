---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/constant-nodes.html"
breadcrumb-title: ''
description: Acesse nós constantes nos gráficos de função do Substance 3D Designer para definir valores e parâmetros constantes.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Constant
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Constante
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 0%

---


# Constante

Nós constantes são uma maneira de criar um valor estático para uso dentro de gráficos de função Substance. Diferentemente de [variáveis](../../../../function-graphs/variables/variables.md), elas não podem ser modificadas externamente.

Além disso, esta página fornece algumas informações adicionais para cada tipo de dados e casos de uso comuns.

## Inteiros

Inteiros constantes geram números inteiros e têm uma etapa de 1.

[Eles podem ser convertidos em Precisão decimal](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md), o que é recomendado ao executar qualquer operação mais complexa do que adições, subtrações e comparações simples.

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

Inteiro2 não é comum, mas é usado, por exemplo, para definir X e Y 2D lado a lado em um [Tile Generator](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md).

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

O inteiro 3 não é comum e provavelmente não será encontrado muito.<b>\
</b>

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

O inteiro 4 não é comum e provavelmente não será encontrado muito.<b>\
</b>

</td>
</tr>
</table>

## Flutuações

Flutuações Constantes geram números fracionários, não números inteiros, o que significa que eles sempre terão valores após o sinal decimal, e podem aumentar ou diminuir em etapas menores que 1 (padrão 0,01).

[As flutuações podem ser convertidas em inteiros](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md), mas serão arredondadas para cima ou para baixo até o inteiro mais próximo, significando que dados e precisão serão perdidos.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Ícone de tipo flutuante](../../../../assets/fn-constant-float.png "Ícone de tipo flutuante")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Flutuante</b>

Um Float, tem um único componente, o (1) é omitido do nome para abreviação. Float é muito comum e é usado para qualquer valor que exija controle preciso na forma de um controle deslizante ou Ângulo. Você pode encontrá-lo em quase todos os parâmetros do Nó. É também o tipo de dados preferencial para um valor em tons de cinza!<b></b>

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

Um nó Float2 gera um vetor flutuante estático de 2 componentes. Os componentes são denominados X, Y. Float2 é bastante comum e é usado para [coordenadas de amostragem](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md) e para [Deslocamentos de transformação](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/transforms.md)

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

Um nó Float3 gera um vetor flutuante estático de 3 componentes. Os componentes são denominados X, Y, Z. Float3 é incomum, é usado principalmente para representar [coordenadas de escala 3D](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md) e como uma maneira mais simples de armazenar cores sem dados de Alpha.<b>\
</b>

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

Um Float4 gera um vetor flutuante estático de 4 componentes. Os componentes são denominados X, Y, Z, W. O Float4 é muito comum, pois é a maneira preferencial de armazenar e definir informações de [Cores, onde os dados XYZW representam valores RGBA.](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md)<b>\
</b>

</td>
</tr>
</table>

## Outros

Existem dois tipos de dados adicionais dentro dos gráficos de função Substance: booleanos e strings. Cadeias de caracteres foram introduzidas junto com o nó [Texto](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md) no Designer versão 6.

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Ícone de tipo booliano](../../../../assets/fn-constant-boolean.png "Ícone de tipo booliano")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Booleano</b>

Um booleano é o tipo de dados mais simples que existe, conhecendo apenas dois estados: Verdadeiro ou Falso, 1 ou 0. É representado pela cor branca. Não é possível fazer intercâmbio entre Boolean e Integer sem [Projeção](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md) ou usando [Nós Lógicos.](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) Um booleano é bastante comum e é uma excelente maneira de controlar o fluxo de uma função ou gráfico. Um uso típico seria para um [Nó de Switch.](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md)<b></b>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Ícone de tipo de cadeia de caracteres](../../../../assets/fn-constant-string.png "Ícone de tipo de cadeia de caracteres")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Cadeia de Caracteres</b>

Um nó String gera uma String estática, um pedaço de texto. É o tipo mais exótico de Dados disponível em Funções, e geralmente não pode ser usado muito em conjunto com outros nós de Função. Seu objetivo principal é funcionar como uma saída final para o [Nó de texto.](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)

</td>
</tr>
</table>
