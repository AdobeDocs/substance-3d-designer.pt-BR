---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes.html"
breadcrumb-title: ''
description: Saiba mais sobre os nós de função atômica, as menores unidades de nó nos gráficos de função Substance para a construção de funções personalizadas.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Atomic function nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nós de função atômica
user-guide-description: ''
user-guide-title: ''
source-git-commit: 953b99bc5f48c431e7ace47a23b0b451cceaa0db
workflow-type: tm+mt
source-wordcount: '1108'
ht-degree: 16%

---


# Nós de função atômica

Da mesma forma que os [nós atômicos em gráficos de Substance](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md), os nós atômicos em gráficos de função de Substance são as menores unidades de nós nesse tipo de gráfico.

Eles podem ser classificados em várias categorias de acordo com sua finalidade:

| Categoria | Nó | Tipo(s) de entrada | Tipo de saída | Descrição |
|:---------------------------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------|:------------------|:---------------------------------------------------------------------------------------------------|
| [Constante](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) | Float | - | Float | Define um valor flutuante constante, por exemplo, 0,1 |
|                                                                                                                                        | Float2 | - | Float2 | Define um vetor constante de 2 valores flutuantes, p. ex. (0,1, 0,2) |
|                                                                                                                                        | Float3 | - | Float3 | Define um vetor constante de 3 valores flutuantes, p. ex. (0,1, 0,2, 0,3) |
|                                                                                                                                        | Float4 | - | Float4 | Define um vetor constante de 4 valores de flutuação, por exemplo (0,1, 0,2, 0,3, 0,4) |
|                                                                                                                                        | Integer | - | Integer | Define um valor inteiro constante, como 1 |
|                                                                                                                                        | Integer2 | - | Integer2 | Define um vetor constante de 2 valores inteiros, por exemplo (1, 2) |
|                                                                                                                                        | Integer3 | - | Integer3 | Define um vetor constante de 3 valores inteiros, por exemplo (1, 2, 3) |
|                                                                                                                                        | Integer4 | - | Integer4 | Define um vetor constante de 4 valores inteiros, por exemplo (1, 2, 3, 4) |
|                                                                                                                                        | Boolean | - | Boolean | Define um valor booleano constante, como Verdadeiro ou Falso |
|                                                                                                                                        | String | - | String | Define um valor de string constante, por exemplo “Substance” |
| [Vetor](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md) | Vetor Float2 | PRECISÃO DECIMAL 1 | PRECISÃO DECIMAL 2 | Converte 2 valores flutuantes em um vetor com 2 coordenadas |
|                                                                                                                                        | Vetor Float3 | Precisão decimal1/Precisão decimal2 | PRECISÃO DECIMAL 3 | Converte 2 valores flutuantes em um vetor com 3 coordenadas |
|                                                                                                                                        | Vetor Float4 | Precisão decimal 1/2/3 | PRECISÃO DECIMAL 4 | Converte 2 valores flutuantes em um vetor com 4 coordenadas |
|                                                                                                                                        | Swizzle Float1 | Flutuação de vetor | Flutuante1 | Extrai uma coordenada flutuante de um vetor |
|                                                                                                                                        | Swizzle Float2 | Flutuação de vetor | Float2 | Extrai 2 coordenadas flutuantes de um vetor |
|                                                                                                                                        | Swizzle Float3 | Flutuação de vetor | Float3 | Extrai 3 coordenadas flutuantes de um vetor |
|                                                                                                                                        | Swizzle Float4 | Flutuação de vetor | Float4 | Extrai 4 coordenadas flutuantes de um vetor |
|                                                                                                                                        | Vector Integer2 | Integer2 | Vector Integer2 | Converte 2 valores inteiros em um vetor com 2 coordenadas |
|                                                                                                                                        | Vector Integer3 | Integer3 | Integer3 | Converte 2 valores inteiros em um vetor com 3 coordenadas |
|                                                                                                                                        | Vector Integer4 | Integer4 | Integer4 | Converte 2 valores inteiros em um vetor com 4 coordenadas |
|                                                                                                                                        | Swizzle Integer1 | Inteiro vetorial | Inteiro1 | Extrai uma coordenada inteira de um vetor |
|                                                                                                                                        | Swizzle Integer2 | Inteiro vetorial | Integer2 | Extrai coordenadas inteiras 2 de um vetor |
|                                                                                                                                        | Swizzle Integer3 | Inteiro vetorial | Integer3 | Extrai coordenadas inteiras 3 de um vetor |
|                                                                                                                                        | Swizzle Integer4 | Inteiro vetorial | Integer4 | Extrai 4 coordenadas inteiras de um vetor |
| [Variáveis](../../../function-graphs/variables/variables.md) | Definir | qualquer | tipo de entrada | Define uma variável |
|                                                                                                                                        | Obter Inteiro1 | - | Inteiro1 | Obter uma entrada de valor de Inteiro de função ou gráfico |
|                                                                                                                                        | Obter Integer2 | - | Integer2 | Obter uma entrada de valor Integer2 de função ou gráfico |
|                                                                                                                                        | Obter Integer3 | - | Integer3 | Obter uma entrada de valor Integer3 de função ou gráfico |
|                                                                                                                                        | Obter Integer4 | - | Integer4 | Obter uma entrada de valor Integer4 de função ou gráfico |
|                                                                                                                                        | Obter Precisão decimal 1 | - | Flutuante1 | Obter uma entrada de valor flutuante de função ou gráfico |
|                                                                                                                                        | Obter Float2 | - | Float2 | Obter uma entrada de valor de função ou gráfico Precisão decimal2 |
|                                                                                                                                        | Obter Float3 | - | Float3 | Obter uma entrada de valor de função ou gráfico Precisão decimal3 |
|                                                                                                                                        | Obter Float4 | - | Float4 | Obter uma entrada de valor de função ou gráfico Precisão decimal 4 |
|                                                                                                                                        | Obter booleano | - | Boolean | Obter uma função ou uma entrada de valor booleano de gráfico |
| Amostragem | Cinza da amostra | Vetor Float2 | Float4 | Retorna o valor em tons de cinza de uma imagem de entrada nas coordenadas UV fornecidas (float2) |
|                                                                                                                                        | Cor da amostra | Vetor Float2 | Float4 | Retorna o valor de cor de uma imagem de entrada nas coordenadas UV fornecidas (float2) |
| Converter | Para Float | Inteiro1 | Flutuante1 | Converte um inteiro em um flutuante |
|                                                                                                                                        | To Float2 | Integer2 | Float2 | Converte um Inteiro2 em uma Precisão decimal 2 |
|                                                                                                                                        | To Float3 | Integer3 | Float3 | Converte um Inteiro3 em uma Precisão decimal 3 |
|                                                                                                                                        | To Float4 | Integer4 | Float4 | Converte um Inteiro4 em uma Precisão decimal 4 |
|                                                                                                                                        | Para Integer | Flutuante1 | Inteiro1 | Converte um Float em um Inteiro |
|                                                                                                                                        | To Integer2 | Float2 | Integer2 | Converte uma Precisão decimal 2 em um Inteiro2 |
|                                                                                                                                        | To Integer3 | Float3 | Integer3 | Converte uma Precisão decimal 3 em um Inteiro3 |
|                                                                                                                                        | To Integer4 | Float4 | Integer4 | Converte um Float4 em um Inteiro4 |
| [Operador](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/operator-nodes/operator-nodes.md) | Adição | Vetor flutuante / Inteiro | Tipo de a &amp; b | Adiciona 2 valores do mesmo tipo: a + b |
|                                                                                                                                        | Subtração | Vetor flutuante / Inteiro | Tipo de a &amp; b | Subtrai 2 valores do mesmo tipo: a - b |
|                                                                                                                                        | Multiplicação | Vetor flutuante / Inteiro | Tipo de a &amp; b | Multiplica 2 valores do mesmo tipo: a \* b |
|                                                                                                                                        | Multiplicação escalar | Flutuação de vetor | Tipo de um | Multiplica um valor por um valor flutuante: um \* escalar |
|                                                                                                                                        | Divisão | Precisão decimal 1 / Inteiro1 | Tipo de a &amp; b | Divide 2 valores do mesmo tipo: a / b |
|                                                                                                                                        | Negação | Precisão decimal 1 / Inteiro1 | Tipo de um | Retorna o valor de negação: -a |
|                                                                                                                                        | Módulo | Precisão decimal 1 / Inteiro1 | Tipo de um | Retorna o valor do módulo: mod(a, divisor) |
|                                                                                                                                        | Produto Ponto | Flutuação de vetor | Tipo de a &amp; b | Retorna o produto de ponto de 2 valores do mesmo tipo: dot(a, b) |
| [Lógico](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) | E | Boolean | Boolean | Retorna verdadeiro se as duas entradas booleanas forem verdadeiras. Retorna false se a entrada for false. |
|                                                                                                                                        | Ou | Boolean | Boolean | Retorna verdadeiro se 1 das entradas booleanas for verdadeiro. Retorna false se ambos forem false. |
|                                                                                                                                        | Não | Boolean | Boolean | Retorna o booleano de negação da entrada: !a |
| [Comparação](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/comparison-nodes/comparison-nodes.md) | Igual | Precisão decimal 1 / Inteiro1 | Boolean | Retorna verdadeiro se a = b |
|                                                                                                                                        | Não igual | Precisão decimal 1 / Inteiro1 | Boolean | Retorna verdadeiro se a != b |
|                                                                                                                                        | Maior | Precisão decimal 1 / Inteiro1 | Boolean | Retorna verdadeiro se a > b |
|                                                                                                                                        | Maior ou igual | Precisão decimal 1 / Inteiro1 | Boolean | Retorna verdadeiro se a >= b |
|                                                                                                                                        | Menor | Precisão decimal 1 / Inteiro1 | Boolean | Retorna verdadeiro se a &lt; b |
|                                                                                                                                        | Menor ou igual | Precisão decimal 1 / Inteiro1 | Boolean | Retorna verdadeiro se a &lt;= b |
| Função | Absoluto | Precisão decimal 1 / Inteiro1 | Flutuante1 | Retorna o valor absoluto de a: abs(a) |
|                                                                                                                                        | Piso | Precisão decimal 1 / Inteiro1 | Flutuante1 | Retorna o valor mais alto menor ou igual a a: floor(a) |
|                                                                                                                                        | Teto | Precisão decimal 1 / Inteiro1 | Flutuante1 | Retorna o menor valor superior ou igual a a: ceil(a) |
|                                                                                                                                        | Cosseno | Precisão decimal 1 / Inteiro1 | Flutuante1 | Retorna o valor de cosseno de a: cos(a) |
|                                                                                                                                        | Seno | Precisão decimal 1 / Inteiro1 | Flutuante1 | Retorna o valor seno de a: sin(a) |
|                                                                                                                                        | Tangente | Precisão decimal 1 / Inteiro1 | Flutuante1 | Retorna o valor tangente de a: tan(a) |
|                                                                                                                                        | Tangente do arco 2 | Vetor Float2 | Flutuante1 | Retorna o valor arc tan 2 de uma entrada vetor2: arctan2(xa, ya) |
|                                                                                                                                        | Cartesiano | Flutuante1 | Float2 | Converte 2 coordenadas polares em coordenadas cartesianas: carth(rho, theta) |
|                                                                                                                                        | Raiz quadrada | Precisão decimal 1 / Inteiro1 | Flutuante1 | Retorna o valor raiz quadrada de um |
|                                                                                                                                        | Logarítmico | Precisão decimal 1 / Inteiro1 | Flutuante1 | Retorna o valor logarítmico de a: log(a) |
|                                                                                                                                        | Exponencial | Precisão decimal 1 / Inteiro1 | Flutuante1 | Retorna o valor exponencial de a: exp(a) |
|                                                                                                                                        | Pow 2 | Precisão decimal 1 / Inteiro1 | Flutuante1 | Retorna a potência de 2 valores de um |
|                                                                                                                                        | Interpolação linear | Precisão decimal 1 / Inteiro1 | Flutuante1 | Retorna a interpolação linear entre 2 valores, dependendo de um valor flutuante: (1-x)a + x \* b |
|                                                                                                                                        | Mínimo | Precisão decimal 1 / Inteiro1 | Tipo de a &amp; b | Retorna o valor mínimo entre a e b |
|                                                                                                                                        | Máximo | Precisão decimal 1 / Inteiro1 | Tipo de a &amp; b | Retorna o valor máximo entre a e b |
| Aleatória |                       | Flutuante1 | Flutuante1 | Gera um valor flutuante entre 0 e um |
| [Controle](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/control-nodes/control-nodes.md) | Sequência | qualquer | Tipo de entrada | Permite escolher qual valor será calculado primeiro entre 2 valores. |
|                                                                                                                                        | If...Else | Booleano / a &amp; b | Tipo de a &amp; b | Retorna verdadeiro se a condição em If for verdadeira. Retorna falso se for falso. |
