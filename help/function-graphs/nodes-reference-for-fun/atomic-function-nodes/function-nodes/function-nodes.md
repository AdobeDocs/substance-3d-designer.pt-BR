---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/function-nodes.html"
breadcrumb-title: ''
description: Acesse nós de função nos gráficos de função do Substance 3D Designer para chamar e executar gráficos de função personalizados.
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Function
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Função
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 5%

---


# Nós de função

Os nós de função transformam o valor de entrada de acordo com a função matemática que representam.

Embora seus conectores de entrada geralmente não sejam tipados, eles não suportam todos os tipos de valor.

## Lista de nós

+++Pot
![Ícone de nó Pow](function-nodes.resources/function-nodes-01.jpg "Ícone de nó Pow")



Retorna a primeira entrada elevada à potência da segunda entrada: <b>X^Y</b>.

+++

+++2Pow
![ícone do nó Pow](function-nodes.resources/function-nodes-02.jpg "ícone do nó Pow")



Retorna 2 à potência do valor de entrada: <b>2^X</b>.

+++

+++Raiz quadrada
![Ícone de nó Raiz Quadrada](function-nodes.resources/function-nodes-03.jpg "ícone de nó Raiz Quadrada")



Retorna a raiz quadrada de seu valor de entrada: <b> √X</b>.

+++

+++Exponencial
![Ícone de nó exponencial](function-nodes.resources/function-nodes-04.jpg "Ícone de nó exponencial")



Retorna o valor exponencial de seu valor de entrada: <b>e^X</b>

<b>e</b> é aproximadamente igual a 2,7182818.

+++

+++Logaritmo
![Ícone de nó de logaritmo](function-nodes.resources/function-nodes-05.jpg "Ícone de nó de logaritmo")



Retorna o logaritmo natural de seu valor de entrada: <b>ln(X)</b>.

+++

+++Logaritmo base 2
![Ícone de nó da Base do Logaritmo 2](function-nodes.resources/function-nodes-06.jpg "Ícone de nó da Base do Logaritmo 2")



Retorna o logaritmo de base 2 de seu valor de entrada: <b>log2(X)</b>.

+++

+++Absoluto
![Ícone de nó absoluto](function-nodes.resources/function-nodes-07.jpg "Ícone de nó absoluto")



Retorna o valor absoluto de sua entrada: <b>abs(X)</b>.

+++

+++Teto
![Ícone de nó Ceil](function-nodes.resources/function-nodes-08.jpg "Ícone de nó Ceil")



Arredonda o valor de entrada para cima. Retorna o menor valor inteiro não menor que X: <b>ceil(X)</b>.

+++

+++Piso
![ícone do nó do Número inteiro](function-nodes.resources/function-nodes-09.jpg "ícone do nó do Número inteiro")



Arredonda o valor de entrada para baixo. Retorna o maior valor inteiro não maior que X: <b>floor(X)</b>.

+++

+++Interpolação linear
![Ícone do nó de Interpolação Linear](function-nodes.resources/function-nodes-10.jpg "ícone do nó de Interpolação Linear")



Retorna a interpolação linear entre dois valores na função de um valor flutuante: <b>(1 - X)\*A + X\*B</b>.

+++

+++Mínimo
![Ícone de nó mínimo](function-nodes.resources/function-nodes-11.jpg "Ícone de nó mínimo")



Retorna o menor dos dois valores de entrada: <b>min(A, B)</b>.

+++

+++Máximo
![Ícone de nó máximo](function-nodes.resources/function-nodes-12.jpg "Ícone de nó máximo")



Retorna o maior dos dois valores de entrada: <b>max(A, B)</b>.

+++

+++Cosseno
![Ícone de nó cosseno](function-nodes.resources/function-nodes-13.jpg "Ícone de nó cosseno")



Retorna o cosseno de seu valor de entrada em radianos: <b>cos(X)</b>.

+++

+++Seno
![Ícone de nó seno](function-nodes.resources/function-nodes-14.jpg "Ícone de nó seno")



Retorna o seno de seu valor de entrada em radianos: <b>sin(X)</b>.

+++

+++Tangente
![Ícone de nó Tangent](function-nodes.resources/function-nodes-15.jpg "ícone de nó Tangent")



Retorna a tangente de seu valor de entrada em radianos: <b>tan(X)</b>.

+++

+++Tangente do arco 2
![Ícone de nó Arc Tangent 2](function-nodes.resources/function-nodes-16.jpg "ícone de nó Arc Tangent 2")



Retorna o ângulo entre o vetor 2D de entrada e a horizontal.

É o recíproco da função <b>Cartesiana</b>.

Não é necessário alternar o componente X e Y do vetor de entrada como na função <b>atan2</b> comum.

+++

+++Cartesiano
![Ícone de nó absoluto](function-nodes.resources/function-nodes-07.jpg "Ícone de nó absoluto")



Converte coordenadas polares em coordenadas cartesianas.

É o recíproco da <b>função Arc tangent 2 </b>: <b>Comprimento \* Float2(cos(Angle), sin(Angle).</b>

Coordenadas polares são uma distância da origem e um ângulo em radianos da horizontal.

+++

+++Aleatória
![Ícone de nó aleatório](function-nodes.resources/function-nodes-17.jpg "Ícone de nó aleatório")



Retorna um valor aleatório entre 0 e o valor de entrada <b>X</b>.

+++
