---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/control-nodes.html"
breadcrumb-title: ''
description: Acessar nós de controle em gráficos de função do Substance 3D Designer para controlar o fluxo e a lógica de execução.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Control
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Controle
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 1%

---


# Nós de controle

Esta página descreve nós de [Gráficos de função](../../../../function-graphs/the-function-graph/the-function-graph.md) cuja finalidade é controlar o *fluxo de execução*.

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó If...Else](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/IfElse_Node.jpg "Nó If...Else")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## If...Else

Semelhante às linguagens de programação, o If... Nó Else introduz a possibilidade de filtrar o resultado de acordo com condições predefinidas.

</td>
</tr>
</table>

Você usará este nó em conjunto com os [Nós lógicos](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) e os [Nós de comparação](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/comparison-nodes/comparison-nodes.md) que o ajudarão a criar a condição a ser verificada.

+++Conectores de entrada
<b>Condição</b> *Booleano*\
A condição que controla a saída do nó.

<b>Se</b> *Tipo de variável* A saída de valor do nó se a <b>Condição</b> for *Verdadeira*.

<b>Caso contrário</b> *Tipo de variável* A saída de valor do nó se a <b>Condição</b> for *Falso*.

+++

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó de sequência](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/Sequence_Node.jpg "Nó de sequência")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Sequência

Garante que uma parte do gráfico seja calculada antes de outra.

</td>
</tr>
</table>

Isso é essencial para controlar o estado das variáveis quando são criadas, lidas e atualizadas.

Você pode aprender mais sobre o nó Sequência na página [Usando os nós Definir/Sequência](../../../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md) desta documentação.

+++Conectores de entrada
<b>Entrada</b> *Tipo de variável*\
A parte do gráfico que deve ser calculada primeiro

<b>Último</b> *Tipo de variável*\
A parte do gráfico que deve ser calculada por último

+++

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó de Loop Inteiro](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/WhileLoop-Node.jpg "Nó de loop inteiro")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Loop Momento

Executa a ramificação <b>Init</b> uma vez e itera sobre o <b>Cond. de Saída</b> e o <b>Corpo do Loop</b> ramifica até o <b>Cond. de Saída</b> branch retorna *True*.

Depois que o loop é concluído, o nó gera o resultado da última iteração do <b>Corpo do Loop</b>.

</td>
</tr>
</table>

Os loops têm um número máximo implícito de iterações que pode ser desabilitado definindo-o como -1.

As variáveis retêm seu valor no iteração e podem ser acessadas na condição de saída (Cond. saída).\
Isso significa que você pode adicionar a um valor de índice a cada iteração e verificar seu valor na condição de saída para controlar o número de loops necessários.

>[!IMPORTANT]
>
> Nós conectados ao <b>Cond. de Saída</b> e as ramificações do <b>Corpo do Loop</b> não podem ser conectadas a outras ramificações do gráfico.

+++Conectores de entrada
<b>Inicializar.</b> *Tipo de variável*\
A parte do gráfico que é calculada antes da primeira iteração, ou seja, o início do loop.

<b>Sair do Cond.</b> *Booleano*\
A condição que precisa ser verdadeira para que o loop pare. Ele é recalculado em cada iteração.\
*Observação:* o número máximo de iterações ainda está limitado ao parâmetro <b>Máximo de iterações</b>.

<b>Corpo do Loop</b> *Tipo de variável*\
O gráfico que se beneficia do loop. É recalculado em cada iteração.

+++

+++Parâmetros
<b>Máx. iteração</b> *Inteiro*\
O número máximo de iterações executadas pelo nó.\
O nó para de iterar quando qualquer um dos seguintes critérios é atendido primeiro: esse número máximo é atingido ou a condição de saída se torna verdadeira.\
Esse máximo pode ser desabilitado definindo o valor como *-1*. Nesse ponto, somente a condição de saída pode interromper as iterações.

Definindo &#39;Máx. o iteração to -1 melhora o desempenho em pequenos loops, pois há um contador a menos para manter o controle e a atualização.

No entanto, lembre-se de como o nó está configurado, pois é possível produzir um <b>loop infinito</b> que pode resultar no Designer não responder.

+++

Confira este tutorial sobre o nó Loop While:
