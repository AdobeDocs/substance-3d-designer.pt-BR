---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic.html"
breadcrumb-title: ''
description: Use o nó Quadrático de polígono de spline para criar splines quadráticas complexas com vários pontos de controle.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Poly Quadratic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline (Poli Quadrático)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4ae20991693573dd44016a411c233b071fa96df6
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---


# Spline (Poli Quadrático)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](spline-poly-quadratic.resources/spline-poly-quadratic-icon.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma spline ao longo de vários pontos. A quantidade e os locais desses pontos podem ser arbitrários ou coletados de um nó da [Lista de Pontos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md).

</td>
</tr>
</table>

A trajetória do spline pode ser suavizada a partir de seus pontos intermediários, em que cada ponto intermediário é o ponto de encontro das tangentes “out” e “in” de seus vizinhos.

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Visualizar</b> <i>Tons de cinza</i> | A visualização das linhas de entrada como uma imagem em tons de cinza. |
| <b>Cordas de spline</b> <i>Cor</i> | As coordenadas dos pontos das linhas divisórias de entrada codificadas nos canais RGBA de uma imagem colorida:<br><b>R</b> - posição X<br><b>G</b> - posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br> - Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br> - Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> <i>Cor</i> | Dados adicionais das splines de entrada codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usadas<br><b>A</b> - Não Usadas |
| <b>Valor da spline</b> <i>Inteiro</i> | O número de splines de entrada. |
| <b>Visualização de pontos</b> <i>Tons de cinza</i> | A visualização dos pontos como uma imagem em tons de cinza. |
| <b>Lista de Pontos de Entrada</b> <i>Cor</i> | (disponível quando a opção “Usar lista de pontos de entrada” for Verdadeira) Uma lista de pontos codificados nos canais RGBA de uma imagem colorida:<br><b>R</b> - Posição X<br><b>G</b> - Posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br> - Parte inteira: Smoothness;<br> - Parte fracionária: Thickness. |
| <b>Número do Ponto</b> <i>Inteiro</i> | (disponível quando a opção “Usar lista de pontos de entrada” for Verdadeira) O número de pontos. |

>[!IMPORTANT]
>
> Os conectores da <b>Lista de Pontos</b> e do <b>Número de Pontos</b> são *incompatíveis* com os conectores da <b>Coluna de Spline</b>, dos <b>Dados de Spline</b> e da <b>Quantidade de Spline</b>, pois eles dependem de dados diferentes.

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Visualizar</b> <i>Tons de cinza</i> | A visualização das linhas de saída como uma imagem em tons de cinza. |
| <b>Cordas de spline</b> <i>Cor</i> | As coordenadas dos pontos das linhas divisórias de saída codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Posição X<br><b>G</b> - Posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br> - Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br> - Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> <i>Cor</i> | Dados adicionais das splines de saída codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usadas<br><b>A</b> - Não Usadas |
| <b>Valor da spline</b> <i>Inteiro</i> | O número de splines de saída. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Valor de Pontos</b> <i>Inteiro</i> | O número arbitrário de pontos usados para criar a spline. |
| <b>Modo de Conexão de Spline de Entrada</b> <i>Inteiro</i> | O método usado para conectar as splines de entrada:<br>- <i>Automático:</i> o final da última spline de entrada é conectado ao início da spline gerada, e o final da spline gerada é conectado ao início da primeira spline de entrada;<br>- <i>Manual:</i> Você pode especificar quais splines de entrada devem ser conectadas às extremidades da spline gerada, e onde nas splines de entrada essas conexões devem aterrar. |
| <b>Fechar Spline</b> <i>Booleano</i> | Controla se o ponto final da spline deve ser conectado ao seu ponto inicial.<br>A suavização aplicada à spline nos pontos inicial e final é especificada pelos valores de Smoothness desses pontos. |
| <b>Inverter Direção</b> <i>Booleano</i> | Inverte a direção da spline. |
| <b>Usar Lista de Pontos de Entrada</b> <i>Booleano</i> | Use a lista de pontos fornecida para os conectores de entrada Lista de pontos de entrada e Número do ponto em vez de uma lista arbitrária de pontos.<br>A lista de pontos pode ser fornecida por um nó de [Lista de Pontos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md). |
| <b>Conectar Início à Spline de Entrada</b> <i>Booleano</i> | Quando Verdadeiro, o início da spline gerada é conectado ao último ponto da última spline nas splines de entrada. |
| <b>Iniciar Índice de Spline de Conexão</b> <i>Inteiro</i> | (Disponível quando “Modo de conexão de spline de entrada” estiver definido como “Manual” e “Conectar início ao spline de entrada” estiver definido como “Verdadeiro”) O índice do spline de entrada que deve ser conectado ao início do spline gerado. |
| <b>Iniciar Posição da Conexão</b> <i>Flutuante</i> | (Disponível quando “Modo de conexão de spline de entrada” estiver definido como “Manual” e “Conectar início ao spline de entrada” estiver definido como “Verdadeiro”) A posição no spline de entrada selecionado onde a conexão com o início do spline gerado deve ser estabelecida.<br>Este valor é o comprimento normalizado da spline de entrada selecionada. |
| <b>Conectar Extremidade à Spline de Entrada</b> <i>Booleano</i> | Quando Verdadeiro, o final da spline gerada é conectado ao primeiro ponto da primeira spline nas splines de entrada. |
| <b>Encerrar Índice de Spline de Conexão</b> <i>Inteiro</i> | (Disponível quando “Modo de conexão de spline de entrada” estiver definido como “Manual” e “Conectar extremidade à spline de entrada” estiver definido como “Verdadeiro”) O índice da spline de entrada que deve ser conectado ao final da spline gerada. |
| <b>Encerrar Posição da Conexão</b> <i>Flutuante</i> | (Disponível quando “Modo de conexão de spline de entrada” estiver definido como “Manual” e “Conectar extremidade à spline de entrada” estiver definido como “Verdadeiro”) A posição na spline de entrada selecionada onde a conexão com a extremidade da spline gerada deve ser estabelecida.<br>Este valor é o comprimento normalizado da spline de entrada selecionada. |
| <b>Distribuição Uniforme</b> <i>Booleano</i> | Quando verdadeiro, os pontos da spline ficam com espaçamento uniforme do início ao fim. |
| <b>Acrescentar Spline de Entrada</b> <i>Booleano</i> | Adiciona a spline gerada ao final da lista de splines conectadas às entradas de <b>spline</b>. |
| <b>Correção Não Quadrada</b> <i>Booleano</i> | Ajuste a posição e o thickness dos pontos para manter a forma de spline em resoluções não quadradas.<br>Isso também afeta a distribuição uniforme. |
| <b>Ajuste de Smoothness Global</b> <i>Flutuante</i> | Aplica um deslocamento uniforme ao valor de smoothness de todos os pontos.<br>O valor do smoothness resultante é fixado ao intervalo [0;1]. |
| <b>Propriedades de Pontos</b> |  |
| <b>p# Propriedades</b> <i>Flutuante3</i> | Define as propriedades do ponto p#.<br>- <i>Height:</i> ajusta o height do ponto onde um valor mais baixo significa um local mais baixo ou mais profundo;<br>- <i>Smoothness:</i> Desloca o início da suavização da spline em p#, onde um valor de 0 resulta em uma trajetória rígida e 1 em uma totalmente suave;<br>- <i>Thickness:</i> ajusta o thickness da spline em p#. O thickness é usado por nós Spline específicos. |
| <b>Coordenadas de pontos</b> |  |
| <b>p#</b> <i>Flutuante2</i> | Define a posição do ponto p# no espaço de textura. |
| <b>Visualizar</b> |  |
| <b>Mostrar Tangentes</b> <i>Booleano</i> | Exibe as tangentes dos pontos p1 e p3 para p2 na saída da Visualização. |
| <b>Mostrar Auxiliar de Direção</b> <i>Booleano</i> | Exibe um ponto no início da spline e uma ponta de seta no final da saída de Visualização. |
| <b>Mostrar Envelope de Thickness</b> <i>Booleano</i> | Exibe linhas adicionais nas bordas do thickness da spline. |
| <b>Mostrar Rótulo de Pontos</b> <i>Booleano</i> | Para cada ponto, exibe o nome do ponto ao lado dele na saída “Visualização”. |
| <b>Tamanho do Rótulo de Pontos</b> <i>Flutuante</i> | (Disponível quando a opção &#39;Mostrar Rótulo de Pontos&#39; estiver definida como &#39;Verdadeiro&#39;) O tamanho do rótulo para cada ponto no espaço de textura, onde 0,1 é um décimo da largura da textura. |
| <b>Mostrar pontos</b> <i>Booleano</i> | Exibe os pontos de controle da spline. |
| <b>Tamanho de pontos</b> <i>Flutuante</i> | (Disponível quando a opção &#39;Mostrar pontos&#39; estiver definida como &#39;Verdadeiro&#39;) O raio dos pontos no espaço de textura, onde 0,1 é um décimo da largura da textura. |
| <b>Valor de Segmentos</b> <i>Inteiro</i> | Ajusta o número de segmentos usados para desenhar a visualização de spline na saída da Visualização.<br>Um valor mais alto resulta em uma linha mais suave. |
| <b>Thickness (px)</b> <i>Flutuante</i> | Ajusta o thickness da visualização da spline em pixels na saída da Visualização. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-poly-quadratic.resources/SplinePolyQuadratic-Variant1-Before.jpg" alt="SplinePolyQuadratic-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-poly-quadratic.resources/SplinePolyQuadratic-Variant1-After.jpg" alt="SplinePolyQuadratic-Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](spline-poly-quadratic.resources/SplinePolyQuadratic-Demo.gif "Exemplo de nó 2")

</td>
</tr>
</table>
