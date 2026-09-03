---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/function-graphs/the-function-graph.html"
breadcrumb-title: ''
description: Saiba mais sobre os gráficos de função Substance no Designer para criar funções personalizadas e redes de nós reutilizáveis.
helpx_creative_field: ""
helpx_description: Designer > Substance function graphs > The Substance function graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: O gráfico da função Substance
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---


# Semelhanças com um gráfico de Substance

À primeira vista, o gráfico de função Substance é realmente semelhante a um gráfico de Substance e o fluxo de trabalho é quase o mesmo.

![gráfico de função de Substance](the-function-graph.resources/the-function-graph-01.png "gráfico de função de Substance")

## A navegação é semelhante

No gráfico de função Substance, você pode criar e organizar seus nós da mesma forma que faria em um gráfico de Substance.

você pode acessar os nós da mesma maneira:

* Da biblioteca
* pressionando a barra de espaço ou a tecla Tab
* clicando com o botão direito do mouse e usando o menu Adicionar nó

### O fluxo de trabalho é semelhante

Como no gráfico de Substance, você criará sua função encadeando séries de nós, cada um deles usando o resultado gerado pelo(s) anterior(es).

A saída definirá o valor de um parâmetro ou a saída do nó de processador de pixels.

## Diferenças com um gráfico de Substance

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### Os nós

Os nós disponíveis no gráfico de função Substance são completamente diferentes daqueles que você encontraria em um gráfico de Substance.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![lista de nós de gráfico de função de Substance](the-function-graph.resources/the-function-graph-02.png "lista de nós de gráfico de função de Substance")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### A saída

Ao contrário dos gráficos de Substance, uma função pode ter apenas uma saída.

Outro ponto a ser observado é que não há um nó de saída específico no qual você conecta o resultado final. Em vez disso, você pode sinalizar diretamente como saída, o nó que gera o resultado esperado:

</td>
<td style="border: 0;" valign="top">

![nó de saída do gráfico de função Substance](the-function-graph.resources/the-function-graph-03.png "nó de saída do gráfico de função Substance")

</td>
</tr>
</table>

#### Como definir o nó de saída?

Para definir a saída, basta clicar com o botão direito do mouse no nó que gera a saída esperada e clicar em *Definir como nó de Saída:*

![Definindo o nó de saída](the-function-graph.resources/the-function-graph-04.gif "Definindo o nó de saída")

>[!WARNING]
>
> <b>Verificar o tipo de resultado gerado</b>
> 
> Se você observar que *Definir como Nó de Saída* está acinzentado, isso significa que o valor gerado pelo nó é diferente do valor esperado pelo parâmetro ou pelo processador de pixels.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Quanto aos gráficos de Substance, você pode importar funções feitas em outro gráfico. É possível abrir o gráfico de referência clicando nele com o botão direito do mouse e selecionando “Abrir referência”:

</td>
<td style="border: 0;" valign="top">

![Abrir gráfico de função de Substance referenciado](the-function-graph.resources/the-function-graph-05.png "Abrir gráfico de função de Substance referenciado")

</td>
</tr>
</table>

Se você tiver um sbs contendo várias funções, poderá arrastá-lo e soltá-lo diretamente em um gráfico de função do Substance e escolher a função que deseja importar na lista exibida:

![Descartar gráfico de função de Substance do pacote](the-function-graph.resources/the-function-graph-06.gif "Descartar gráfico de função de Substance do pacote")
