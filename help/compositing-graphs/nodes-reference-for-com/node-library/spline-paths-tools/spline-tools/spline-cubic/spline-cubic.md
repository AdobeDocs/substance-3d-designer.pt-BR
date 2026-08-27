---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-cubic.html"
breadcrumb-title: ''
description: Use o nó Cúbico de spline para criar splines cúbicas suaves com quatro pontos de controle para caminhos curvos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Cubic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Spline (cúbico)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---


# Spline (cúbico)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](../../../../../../assets/spline-cubic-icon.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma única spline entre dois pontos <b>p1 </b>e <b>p2</b> em locais arbitrários.

A trajetória da spline é controlada pela tangente “out” de <b>p1</b> e pela tangente “in” de <b>p2</b>.

</td>
</tr>
</table>

## Conectores de entrada

<b>Visualizar</b> *Tons de cinza* A visualização das linhas divisórias de entrada como uma imagem em tons de cinza.

<b>Cordas de spline</b> *Cor* As coordenadas dos pontos das splines de entrada codificadas nos canais RGBA de uma imagem colorida:\
<b> R</b> - Posição X\
<b> G</b> - posição Y\
<b> B</b> - Height\
<b>A</b> - Dados empacotados:\
* Sinal: Spline é fechado (negativo) ou aberto (positivo);\
* Valor absoluto: Thickness + 1.

<b>Dados de Spline</b> *Cor* Dados adicionais das splines de entrada codificados nos canais RGBA de uma imagem colorida.\
<b> R</b> - Tangentes X\
<b> G</b> - Tangentes Y\
<b> B</b> - Não Usado\
<b> A</b> - Não Usado

<b>Valor da spline</b> *Inteiro* O número de splines de entrada.

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

<b>Inverter Direção</b> *Booleano*\
Inverte a direção da spline.

<b>Acrescentar Spline de Entrada</b> *Booleano*\
Adiciona a spline gerada ao final da lista de splines conectadas às entradas de <b>spline</b>.

<b>Correção não quadrada </b>*Booleana* Ajuste as posições e o thickness dos pontos para manter a forma de spline em resoluções não quadradas.\
Isso também afeta a distribuição uniforme.

+++Altura
<b>Iniciar Height</b> *Flutuante* Ajusta o height do ponto p1 onde um valor mais baixo significa um local mais baixo ou mais profundo.\
Isso afeta o height da spline em p1.

<b>Encerrar Height</b> *Flutuante* Ajusta o height do ponto p2 onde um valor mais baixo significa um local mais baixo ou mais profundo.\
Isso afeta o thickness da spline em p2.

<b>Height Tangente Automático</b> *Booleano* Define automaticamente o height das tangentes da spline para interpolar linearmente do Height inicial ao Height final.

<b>Height de Tangente p1</b> *Flutuante* (disponível quando ‘Auto Tangent Height’ é True)\
Ajusta o height da tangente p1 point “out”, em que um valor mais baixo significa um local mais baixo ou mais profundo.\
Isso afeta o height ao longo da spline à medida que se afasta do p1.

<b>Height de Tangente p2</b> *Flutuante* (disponível quando ‘Auto Tangent Height’ é True)\
Ajusta o height da tangente “in” do ponto p2, em que um valor mais baixo significa um local mais baixo ou mais profundo.\
Isso afeta o height ao longo da spline à medida que se afasta do p2.

+++

+++Espessura
<b>Iniciar Thickness</b> *Flutuante* Ajusta o thickness do ponto p1.\
Isso afeta o thickness da spline em p1.\
Observação: o Thickness é usado por nós de spline específicos.

<b>Encerrar Thickness</b> *Flutuar* Ajusta o thickness do ponto p2.\
Isso afeta o thickness da spline em p2.\
Observação: o Thickness é usado por nós de spline específicos.

<b>Thickness Tangente Automático</b> *Booleano* Define automaticamente o thickness das tangentes da spline para interpolar linearmente do Thickness inicial ao Thickness final.\
Observação: o Thickness é usado por nós de spline específicos.

<b>Thickness de Tangente p1</b> *Flutuante* (disponível quando ‘Auto Tangent Thickness’ é True)\
Ajusta o thickness da tangente p1 point “out”.\
Isso afeta o thickness ao longo da spline à medida que se afasta do p1.\
Observação: o Thickness é usado por nós de spline específicos.

<b>Thickness de Tangente p2</b> *Flutuante* (disponível quando ‘Auto Tangent Thickness’ é True)\
Ajusta o thickness da tangente “in” do ponto p2.\
Isso afeta o thickness ao longo da spline à medida que se afasta do p2.\
Observação: o Thickness é usado por nós de spline específicos.

+++

+++Coordenadas de pontos
<b>p1</b> *Flutuante2* Define a posição do ponto p1 no espaço de textura.

<b>p1 Tangente</b> *Flutuante2* Define a posição da alça tangente p1 point &#39;out&#39; no espaço de textura.

<b>p2</b> *Flutuante2* Define a posição do ponto p2 no espaço de textura.

<b>Tangente p2</b> *Flutuante2* Define a posição da alça tangente “in” do ponto p2 no espaço de textura.

+++

+++Visualização
<b>Mostrar Tangentes</b> *Booleano* Exibe a tangente p1 point &#39;out&#39; e a tangente p2 point &#39;in&#39; na saída da Visualização.

<b>Mostrar Auxiliar de Direção</b> *Booleano* Exibe um ponto no início da spline e uma ponta de seta no final da saída de Visualização.

<b>Valor de Segmentos</b> *Inteiro* Ajusta o número de segmentos usados para desenhar a visualização de spline na saída da Visualização.\
Um valor mais alto resulta em uma linha mais suave.

<b>Thickness (px)</b> *Flutuante* Ajusta o thickness em pixels da visualização de spline na saída da Visualização.

+++

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 1](../../../../../../assets/SplineCubic-Variant1.jpg "Exemplo de nó 1")

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](../../../../../../assets/SplineCubic-Variant2.jpg "Exemplo de nó 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 3](../../../../../../assets/SplineCubic-Demo.gif "Exemplo de nó 3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
