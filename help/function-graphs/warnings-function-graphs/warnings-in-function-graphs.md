---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/warnings-in-function-graphs.html"
breadcrumb-title: ''
description: Entenda os avisos nos gráficos de funções do Substance 3D Designer e saiba como resolver problemas comuns.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Warnings in function graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Avisos em gráficos de função
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---


# Avisos em gráficos de função

Esta página lista mensagens de avisos e erros que podem ser disparadas por [gráficos de função](../../function-graphs/function-graphs.md) no Substance 3D Designer e oferece etapas comuns de solução de problemas para cada uma.

Os avisos são exibidos na dica de ferramenta do ícone de aviso para o recurso de gráfico no painel [Explorador](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html), bem como no canto inferior esquerdo da [Exibição de gráfico](../../interface/the-graph-view/the-graph-view.md) se o gráfico estiver carregado.\
Se a função for *aplicada a um parâmetro* em [gráficos de Substance](../../compositing-graphs/substance-compositing-graphs.md), qualquer aviso resultará no aviso “*A função do parâmetro [x] tem alguns erros*” sendo acionada para esse parâmetro.

## ![(erro)](../../assets/error.svg) Nenhum nó de saída definido

A função não tem um nó de saída definido.

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(tick)](../../assets/check.svg) Solução**

Selecione qualquer nó no gráfico que gera um valor cujo tipo corresponda ao tipo esperado para esta função, se houver, clique em RMB e selecione a opção **Definir como Nó de Saída** no menu contextual.\
O nó de saída de um gráfico de função é colorido com *laranja*.

>[!NOTE]
>
> Se uma função tiver um tipo de valor de saída esperado, uma observação no canto inferior esquerdo da [Exibição de gráfico](../../interface/the-graph-view/the-graph-view.md) permitirá que você conheça esse tipo.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/warnings-func-output.gif)

</td>
</tr>
</table>

### ![(erro)](../../assets/error.svg) O nó de saída atual retorna um valor do tipo *x*

O nó de saída da função retorna um valor cujo tipo não corresponde ao tipo de valor de saída esperado para essa função.

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(tick)](../../assets/check.svg) Solução**

Selecione qualquer nó no gráfico que gera um valor cujo tipo corresponde ao tipo esperado para esta função, clique em RMB e selecione a opção **Definir como Nó de Saída** no menu contextual.\
O nó de saída de um gráfico de função é colorido com *laranja*.

>[!NOTE]
>
> Se uma função tiver um tipo de valor de saída esperado, uma observação no canto inferior esquerdo da [Exibição de gráfico](../../interface/the-graph-view/the-graph-view.md) permitirá que você conheça esse tipo.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/warnings-func-output-type.gif)

</td>
</tr>
</table>

### ![(erro)](../../assets/error.svg) Alguns nós Get não têm um nome de variável

Um ou mais nós [Get](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md) têm sua propriedade <b>Get...</b> deixada em branco; portanto, não se refere a nenhuma variável.

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(tick)](../../assets/check.svg) Solução**

Insira uma cadeia de caracteres que corresponda ao nome de uma variável *disponível no escopo da função* na propriedade **Get...** dos nós Get que geram este aviso.

>[!NOTE]
>
> A cadeia de caracteres de entrada é *exibida no nó*, o que facilita a localização de nós com valores em branco.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/warnings-func-empty-get.gif)

</td>
</tr>
</table>

### ![(erro)](../../assets/error.svg) Alguns nós Set não têm um nome de variável

Um ou mais nós [Set](../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md) têm sua propriedade **Set** deixada em branco; portanto, não se refere a nenhuma variável.

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(tick)](../../assets/check.svg) Solução**

Insira qualquer cadeia de caracteres na propriedade **Set** de nós Set que gere este aviso.

>[!NOTE]
>
> A cadeia de caracteres de entrada é *exibida no nó*, o que facilita a localização de nós com valores em branco.

>[!NOTE]
>
> Se a cadeia de caracteres *não* corresponder a qualquer variável disponível no escopo da função, uma *nova variável será criada* dentro desse escopo e nomeada com base na cadeia de caracteres.

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/warnings-func-empty-set.gif)

</td>
</tr>
</table>
