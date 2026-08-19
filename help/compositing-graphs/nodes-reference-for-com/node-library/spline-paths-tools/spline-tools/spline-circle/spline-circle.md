---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-circle.html"
breadcrumb-title: ''
description: Use o nó Círculo de spline para criar splines circulares para gerar padrões e formas redondos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Circle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Círculo com Spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---


# Círculo com Spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](../../../../../../assets/spline-circle-icon.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma única spline na forma de um círculo.

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

<b>Raio do círculo</b> *Flutuante*\
Ajusta o raio do círculo no espaço de textura.

<b>Pré-rotação do Círculo</b> *Flutuante*\
Aplica uma rotação ao círculo base antes que o Tamanho seja aplicado.

<b>Tamanho do Círculo</b> *Flutuante2*\
Ajusta o tamanho horizontal (X) e o tamanho vertical (Y) do círculo.

<b>Pós-rotação do círculo</b> *Flutuante*\
Aplica uma rotação ao círculo base após a aplicação do Tamanho.

<b>Posição do Círculo</b> *Flutuante2*\
Define a posição do centro do círculo no espaço de textura.

<b>Iniciar Thickness</b> *Flutuar* Ajusta o thickness do ponto inicial do círculo.\
Esse thickness é interpolado ao longo da spline até o Thickness final.\
Observação: o Thickness é usado por nós de spline específicos.

<b>Encerrar Thickness</b> *Flutuar* Ajusta o thickness do ponto final do círculo.\
Esse thickness é interpolado ao longo da spline até o Thickness inicial.\
Observação: o Thickness é usado por nós de spline específicos.

<b>Iniciar Height</b> *Flutuante* Ajusta o height do ponto inicial do círculo, onde um valor mais baixo significa um local mais baixo ou mais profundo.\
Esse height é interpolado ao longo da spline até o Height final.

<b>Encerrar Height</b> *Flutuante* Ajusta o height do ponto final do círculo onde um valor mais baixo significa um local mais baixo ou mais profundo.\
Esse height é interpolado ao longo da spline a partir do Height inicial.

<b>Cortar</b> *Flutuante2* Desloca os pontos inicial e final da spline ao longo do círculo.\
Esses valores são normalizados.

<b>Espiral</b> *Flutuante* Desloca o ponto inicial do círculo de seu raio para seu centro.\
A distância do centro é então interpolada ao longo do spline até o final do spline.\
Este valor está normalizado.

<b>Rotações em espiral</b> *Flutuante* Define o número de voltas feitas pela espiral ao redor de seu centro.

<b>Energia em espiral</b> *Flutuante* Aplica uma curva de potência à distância do centro usada para desenhar a espiral.\
Um valor maior do que um significa que uma porção maior da espiral permanece próxima ao centro.

<b>Inverter Direção</b> *Booleano*\
Inverte a direção da spline.

<b>Distribuição Uniforme</b> *Booleano*\
Quando verdadeiro, os pontos da spline ficam com espaçamento uniforme do início ao fim.

<b>Acrescentar Spline de Entrada</b> *Booleano*\
Adiciona a spline gerada ao final da lista de splines conectadas às entradas de <b>spline</b>.

<b>Correção não quadrada </b>*Booleana* Ajuste as posições e o thickness dos pontos para manter a forma de spline em resoluções não quadradas.\
Isso também afeta a distribuição uniforme.

+++Visualização
<b>Mostrar Auxiliar de Direção</b> *Booleano* Exibe um ponto no início da spline e uma ponta de seta no final da saída de Visualização.

<b>Mostrar Envelope de Thickness</b> *Booleano*\
Exibe linhas adicionais nas bordas do thickness da spline.

<b>Valor de Segmentos</b> *Inteiro* Ajusta o número de segmentos usados para desenhar a visualização de spline na saída da Visualização.\
Um valor mais alto resulta em uma linha mais suave.

<b>Thickness (px)</b> *Flutuante* Ajusta o thickness em pixels da visualização de spline na saída da Visualização.

+++

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 1](../../../../../../assets/SplineCircle-Variant1.jpg "Exemplo de nó 1")

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](../../../../../../assets/SplineCircle-Demo.gif "Exemplo de nó 2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo 3](../../../../../../assets/SplineCircle-Variant2.jpg "Exemplo 3")

</td>
<td style="border: 0;" valign="top">

![Exemplo 4](../../../../../../assets/SplineCircle-Variant3.jpg "Exemplo 4")

</td>
</tr>
</table>
