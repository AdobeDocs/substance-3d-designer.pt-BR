---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic.html"
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
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '1147'
ht-degree: 0%

---


# Spline (Poli Quadrático)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](../../../../../../assets/spline-poly-quadratic-icon.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma spline ao longo de vários pontos. A quantidade e os locais desses pontos podem ser arbitrários ou coletados de um nó da [Lista de Pontos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md).

</td>
</tr>
</table>

A trajetória do spline pode ser suavizada a partir de seus pontos intermediários, em que cada ponto intermediário é o ponto de encontro das tangentes “out” e “in” de seus vizinhos.

## Conectores de entrada

<b>Visualizar</b> *Tons de cinza* A visualização das linhas divisórias de entrada como uma imagem em tons de cinza.

<b>Cordas de spline</b> *Cor* As coordenadas dos pontos das splines de entrada codificadas nos canais RGBA de uma imagem colorida:\
<b> R</b> - Posição X\
<b> G</b> - posição Y\
<b> B</b> - Height\
<b> A</b> - Dados empacotados:\
        * Sinal: Spline é fechado (negativo) ou aberto (positivo);\
        * Valor absoluto: Thickness + 1.

<b>Dados de Spline</b> *Cor* Dados adicionais das splines de entrada codificados nos canais RGBA de uma imagem colorida.\
<b> R</b> - Tangentes X\
<b> G</b> - Tangentes Y\
<b> B</b> - Não Usado\
<b> A</b> - Não Usado

<b>Valor da spline</b> *Inteiro* O número de splines de entrada.

<b>Visualização de pontos </b>*Tons de cinza* A visualização dos pontos como uma imagem em tons de cinza.

<b>Lista de Pontos de Entrada</b> *Cor* (disponível quando “Usar lista de pontos de entrada” é Verdadeiro)\
Uma lista de pontos codificados nos canais RGBA de uma imagem colorida:\
    <b>R</b> - Posição X\
    <b>G</b> - posição Y\
    <b>B</b> - Height\
    <b>A</b> - Dados empacotados:\
        * Parte inteira: Smoothness;\
        * Parte fracionária: Thickness.

<b>Número do Ponto</b> *Inteiro* (disponível quando “Usar Lista de Pontos de Entrada” é Verdadeiro)\
O número de pontos.

>[!IMPORTANT]
>
> Os conectores da <b>Lista de Pontos</b> e do <b>Número de Pontos</b> são *incompatíveis* com os conectores da <b>Coluna de Spline</b>, dos <b>Dados de Spline</b> e da <b>Quantidade de Spline</b>, pois eles dependem de dados diferentes.

## Conectores de saída

<b>Visualizar</b> *Tons de cinza* A visualização das linhas divisórias de saída como uma imagem em tons de cinza.

<b>Cordas de spline</b> *Cor* As coordenadas dos pontos das linhas divisórias de saída codificadas nos canais RGBA de uma imagem colorida.\
    <b>R</b> - Posição X\
    <b>G</b> - posição Y\
    <b>B</b> - Height\
    <b>A</b> - Dados empacotados:\
        * Sinal: Spline é fechado (negativo) ou aberto (positivo);\
        * Valor absoluto: Thickness + 1.

<b>Dados de Spline</b> *Cor* Dados adicionais das splines de saída codificados nos canais RGBA de uma imagem colorida.\
    <b>R</b> - Tangentes X\
    <b>G</b> - Tangentes Y\
    <b>B</b> - Não Usado\
    <b>A</b> - Não Usado

<b>Valor da spline</b> *Inteiro* O número de splines de saída.

## Parâmetros

<b>Valor de Pontos</b> *Inteiro* O número arbitrário de pontos usados para criar a spline.

<b>Modo de Conexão de Spline de Entrada</b> *Inteiro* O método usado para conectar os Splines de entrada:\
*- Automático:* O final da última spline de entrada é conectado ao início da spline gerada, e o final da spline gerada é conectado ao início da primeira spline de entrada;\
*- Manual:* Você pode especificar quais das splines de entrada devem ser conectadas às extremidades da spline gerada e onde nas splines de entrada essas conexões devem pousar.

<b>Fechar Spline</b> *Booleano* Controla se o ponto final da spline deve ser conectado ao seu ponto inicial.\
A suavização aplicada à spline nos pontos inicial e final é especificada pelos valores de Smoothness desses pontos.

<b>Inverter Direção</b> *Booleano*\
Inverte a direção da spline.

<b>Usar Lista de Pontos de Entrada</b> *Booleano* Use a lista de pontos fornecida para os conectores de entrada Lista de Pontos de Entrada e Número de Pontos em vez de uma lista arbitrária de pontos.\
A lista de pontos pode ser fornecida por um nó de [Lista de Pontos](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md).

<b>Conectar Início à Spline de Entrada</b> *Booleano* Quando Verdadeiro, o início da spline gerada é conectado ao último ponto da última spline nas splines de entrada.

<b>Iniciar Índice de Spline de Conexão</b> *Inteiro* (Disponível quando “Modo de Conexão Spline de Entrada” está definido como “Manual” e “Conectar Início ao Spline de Entrada” está definido como “Verdadeiro”)O índice do spline de entrada que deve ser conectado ao início do spline gerado.

<b>Iniciar Posição da Conexão</b> *Flutuante* (Disponível quando “Modo de Conexão de Spline de Entrada” estiver definido como “Manual” e “Conectar Início ao Spline de Entrada” estiver definido como “Verdadeiro”)A posição na spline de entrada selecionada onde a conexão com o início da spline gerada deve parar.\
Esse valor é o comprimento normalizado do spline de entrada selecionado.

<b>Conectar Extremidade à Spline de Entrada</b> *Booleano* Quando Verdadeiro, o final da spline gerada é conectado ao primeiro ponto da primeira spline nas splines de entrada.

<b>Encerrar Índice de Spline de Conexão</b> *Inteiro* (Disponível quando “Modo de Conexão Spline de Entrada” estiver definido como “Manual” e “Conectar Fim ao Spline de Entrada” estiver definido como “Verdadeiro”)O índice do spline de entrada que deve ser conectado ao fim do spline gerado.

<b>Encerrar Posição da Conexão</b> *Flutuante* (Disponível quando “Modo de Conexão de Spline de Entrada” estiver definido como “Manual” e “Conectar Extremidade à Spline de Entrada” estiver definido como “Verdadeiro”)A posição na spline de entrada selecionada na qual a conexão com a extremidade da spline gerada deve aterrar.\
Esse valor é o comprimento normalizado do spline de entrada selecionado.

<b>Distribuição Uniforme</b> *Booleano*\
Quando verdadeiro, os pontos da spline ficam com espaçamento uniforme do início ao fim.

<b>Acrescentar Spline de Entrada</b> *Booleano*\
Adiciona a spline gerada ao final da lista de splines conectadas às entradas de <b>spline</b>.

<b>Correção não quadrada </b>*Booleana* Ajuste as posições e o thickness dos pontos para manter a forma de spline em resoluções não quadradas.\
Isso também afeta a distribuição uniforme.

<b>Ajuste de Smoothness Global</b> *Flutuante* Aplica um deslocamento uniforme ao valor de smoothness de todos os pontos.\
O valor do smoothness resultante é fixado no intervalo [0;1].

+++Propriedades de Pontos
<b>p# Propriedades</b> *Flutuante3* Define as propriedades do ponto p#.\
*- Height:* Ajusta o height do ponto onde um valor mais baixo significa um local mais baixo ou mais profundo;\
*- Smoothness:* Desloca o início da suavização da spline em p#, onde um valor de 0 resulta em uma trajetória rígida e 1 em uma totalmente suave;\
*- Thickness:* Ajusta o thickness da spline em p#. O thickness é usado por nós Spline específicos.

+++

+++Coordenadas de pontos
<b>p#</b> *Flutuante2* Define a posição do ponto p# no espaço de textura.

+++

+++Visualização
<b>Mostrar Tangentes</b> *Booleano* Exibe as tangentes dos pontos p1 e p3 para p2 na saída da Visualização.

<b>Mostrar Auxiliar de Direção</b> *Booleano* Exibe um ponto no início da spline e uma ponta de seta no final da saída de Visualização.

<b>Mostrar Envelope de Thickness</b> *Booleano*\
Exibe linhas adicionais nas bordas do thickness da spline.

<b>Mostrar Rótulo de Pontos</b> *Booleano*\
Para cada ponto, exibe o nome do ponto ao lado dele na saída “Visualização”.

<b>Tamanho do Rótulo de Pontos</b> *Flutuante* (Disponível quando &#39;Mostrar Rótulo de Pontos&#39; estiver definido como &#39;Verdadeiro&#39;)\
O tamanho do rótulo para cada ponto no espaço de textura, onde 0,1 é um décimo da largura da textura.

<b>Mostrar pontos</b> *Booleano*\
Exibe os pontos de controle da spline.

<b>Tamanho de pontos</b> *Flutuante* (Disponível quando &#39;Mostrar Pontos&#39; estiver definido como &#39;Verdadeiro&#39;)\
O raio dos pontos no espaço de textura, onde 0,1 é um décimo da largura da textura.

<b>Valor de Segmentos</b> *Inteiro* Ajusta o número de segmentos usados para desenhar a visualização de spline na saída da Visualização.\
Um valor mais alto resulta em uma linha mais suave.

<b>Thickness (px)</b> *Flutuante* Ajusta o thickness da visualização da spline em pixels na saída da Visualização.

+++

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplinePolyQuadratic-Variant1-Before.jpg" alt="SplinePolyQuadratic-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplinePolyQuadratic-Variant1-After.jpg" alt="SplinePolyQuadratic-Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](../../../../../../assets/SplinePolyQuadratic-Demo.gif "Exemplo de nó 2")

</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
