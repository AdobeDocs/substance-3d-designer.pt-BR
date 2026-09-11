---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random-2.html"
breadcrumb-title: ''
description: Use o nó Aleatório de bloco 2 para criar padrões de bloco aleatórios com controles avançados de variação no Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random 2
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mosaico aleatório 2
user-guide-description: ''
user-guide-title: ''
source-git-commit: b63bc7a45aa6eadef1b72eb05d4a6aded05866a8
workflow-type: tm+mt
source-wordcount: '1308'
ht-degree: 0%

---


# Mosaico aleatório 2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tile-random-2.resources/tilerandom2.jpg){width="200px"}

<b>Em:</b> Geradores De Textura > Padrões

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O nó **Bloco Aleatório 2** gera blocos adjacentes de tamanhos aleatórios e proporções de height para largura.

A grade pode ser ajustada ao *inclinar* aleatoriamente os lados das formas para quebrar os ângulos.

As formas podem ser ajustadas com opções de *dimensionamento*, *chanfro*, *arredondamento dos cantos*, bem como *rotação distorcida*.

Esses ajustes podem ser controlados por *mapas de entrada*.

Uma saída dedicada permite que você insira os **UVs** da forma em **Flood Fill para (...)** nós para aplicar a variação adicional.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Mapa de Tamanho Aleatório</b> <i>Tons de cinza</i> | A imagem de entrada em tons de cinza que controla a escala aleatória das formas.<br><br>Seu impacto é controlado pelo parâmetro <b>Multiplicador de Mapa de Entrada de Tamanho Aleatório</b>. |
| <b>Mapa de Inclinação Aleatório</b> <i>Tons de cinza</i> | A imagem de entrada em tons de cinza que controla a inclinação aleatória das formas.<br><br>Seu impacto é controlado pelo parâmetro <b>Multiplicador de Mapa de Entrada Inclinada Aleatória</b>. |
| <b>Mapa do Raio dos Cantos Arredondados</b> <i>Tons de cinza</i> | A imagem de entrada em tons de cinza que controla o raio dos cantos arredondados das formas.<br><br>Seu impacto é controlado pelo <b>Módulo de Mapa de Entrada do Raio dos Cantos Arredondados.</b> parâmetro. |
| <b>Mapa de distância de chanfro</b> <i>Tons de cinza</i> | A imagem de entrada em tons de cinza que controla o chanfro das formas.<br><br>Seu impacto é controlado pelo <b>Módulo de Mapa de Entrada de Distância de Chanfro.</b> parâmetro. |
| <b>Mapa de máscaras</b> <i>Tons de cinza</i> | A imagem de entrada em tons de cinza que controla o mascaramento das formas.<br><br>Seu impacto é controlado pelos parâmetros <b>Início da entrada do mapa de máscaras</b> e <b>Fim da entrada do mapa de máscaras</b>. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Valor X</b> <i>Inteiro</i> | O número de células no eixo <b>X</b>. |
| <b>Valor Y</b> <i>Inteiro</i> | O número de células no eixo <b>Y</b>. |
| <b>Tamanho</b> |  |
| <b>Multiplicador de Tamanho Aleatório</b> <i>Flutuante</i> | Aplica um ajuste <i>global</i> à intensidade do dimensionamento aleatório. |
| <b>Multiplicador de Mapa de Entrada de Tamanho Aleatório</b> <i>Flutuante</i> | Ajusta a intensidade do dimensionamento aleatório usando os valores <i>amostrados</i> da entrada <b>Mapa de Tamanho Aleatório</b>. |
| <b>Tamanho Aleatório X</b> <i>Flutuante</i> | Ajusta a intensidade do dimensionamento aleatório no eixo <b>X</b> <i>somente</i>. |
| <b>Tamanho aleatório Y</b> <i>Flutuante</i> | Ajusta a intensidade do dimensionamento aleatório no eixo <b>Y</b> <i>somente</i>. |
| <b>Distribuição de Tamanho Aleatório</b> <i>Inteiro</i> | Controla o método de distribuição de valores de escala aleatória:<br><br>- <i>Uniforme</i>: a escala aleatória é aplicada da <i>mesma forma</i> em todas as células<br>- <i>Ruído azul</i>: a escala aleatória é <i>ajustada</i> usando um padrão de ruído azul |
| <b>Proporção da forma - Transformar</b> |  |
| <b>Thickness Interstice</b> <i>Flutuante</i> | Ajusta o thickness do espaço entre as formas. É <i>igual para todas as formas</i>. |
| <b>Multiplicador de Posição Aleatória</b> <i>Flutuante</i> | Aplica um deslocamento de posição aleatório à forma até ela <i>atingindo a borda da célula</i>. |
| <b>Raio dos cantos arredondados</b> <i>Flutuante</i> | Ajusta o <i>raio</i> dos cantos arredondados das formas. Um valor de <b>0</b> significa que nenhum arredondamento foi aplicado.<br><br><i>Observação</i>: esse efeito não pode ser aplicado quando o parâmetro <b>Habilitar por Controle de Chanfro de Eixo</b> está definido como <i>Verdadeiro</i>. |
| <b>Mapa De Entrada Do Raio Dos Cantos Arredondados Mult.</b> <i>Flutuante</i> | Ajusta a intensidade com que o mapa de entrada <b>Mapa do Raio dos Cantos Arredondados</b> afeta o raio dos cantos arredondados.<br><br>O mapa atua como um multiplicador <i>por pixel</i> para o parâmetro <b>Raio dos cantos arredondados</b>.<br><br><i>Observação</i>: esse efeito não pode ser aplicado quando o parâmetro <b>Habilitar controle de chanfro por eixo</b> está definido como <i>Verdadeiro</i>. |
| <b>Multiplicador de Escala</b> <i>Flutuante</i> | Ajusta o tamanho de cada forma, como uma proporção da <i>área de sua célula</i>. |
| <b>Escala aleatória</b> <i>Flutuante</i> | Ajusta a intensidade com que uma escala aleatória é aplicada a <i>cada</i> forma. |
| <b>Rotação</b> <i>Flutuante</i> | Gira formas em suas células movendo cada <i>canto</i> para seu <i>vizinho</i> ao longo da borda da célula.<br><br>Este método resulta na aplicação de uma quantidade de <i>distorção</i> e <i>dimensionamento</i> à forma em seus giros. |
| <b>Rotação aleatória</b> <i>Flutuante</i> | Ajusta a intensidade com que uma quantidade aleatória de rotação é aplicada a cada forma.<br><br>O método de rotação está descrito no parâmetro <b>Rotação</b>. |
| <b>Posição dos cantos aleatória</b> <i>Flutuante</i> | Distorce as formas aplicando um valor aleatório de <i>deslocamento</i> em cada um dos <i>cantos</i> ao longo da borda da célula. |
| <b>Inclinar</b> |  |
| <b>Multiplicador de inclinação aleatória</b> <i>Flutuante</i> | Aplica um ajuste <i>global</i> à intensidade da inclinação aleatória. |
| <b>Multiplicador de Mapa de Entrada Inclinado Aleatório</b> <i>Flutuante</i> | Ajusta a intensidade da inclinação aleatória usando os valores <i>amostrados</i> da entrada <b>Mapa de inclinação aleatória</b>. |
| <b>Inclinação Aleatória X</b> <i>Flutuante</i> | Ajusta a intensidade da inclinação aleatória no eixo <b>X</b> <i>somente</i>. |
| <b>Inclinação aleatória Y</b> <i>Flutuante</i> | Ajusta a intensidade da inclinação aleatória no eixo <b>Y</b> <i>somente</i>. |
| <b>Distribuição de Inclinação Aleatória</b> <i>Inteiro</i> | Controla o método de distribuição de valores de inclinação aleatória:<br><br>- <i>Uniforme</i>: a inclinação aleatória é aplicada da <i>mesma forma</i> em todas as células<br>- <i>Ruído azul</i>: a inclinação aleatória é <i>ajustada</i> usando um padrão de ruído azul |
| <b>Chanfro</b> |  |
| <b>Modo de distância de chanfro</b> <i>Inteiro</i> | Define o método de <i>aquisição da distância</i> pela qual as formas devem ser chanfradas:<br><br>- <i>Em relação ao tamanho da grade</i>: as formas são chanfradas pela <i>proporção especificada de seu tamanho de grade</i><br>- <i>Em relação ao tamanho da forma</i>: as formas são chanfradas pela <i>proporção especificada de seu tamanho</i><br>- <i>Em relação ao tamanho da imagem</i>: as formas são chanfradas pela <i>proporção especificada da imagem</i> |
| <b>Multiplicador de distância de chanfro</b> <i>Flutuante</i> | Aplica um ajuste <i>global</i> à distância do chanfro. |
| <b>Mapa de Entrada de Distância de Chanfro Mult.</b> <i>Flutuante</i> | Ajusta a distância do chanfro usando o mapa de entrada <b>Mapa de distância de chanfro</b> como um multiplicador de <i>por pixel</i>. |
| <b>Curva arredondada chanfrada</b> <i>Flutuante</i> | Ajusta a intensidade do arredondamento aplicado ao ângulo de chanfro para torná-lo mais <i>convexo</i>. |
| <b>Habilitar Controle de Chanfro por Eixo</b> <i>Booleano</i> | Quando <i>Verdadeiro</i>, o chanfro pode ser aplicado e ajustado <i>separadamente</i> nos eixos <b>X</b> e <b>Y</b>.<br><br><i>Observação</i>: este <i>cancela</i> o efeito <b>Cantos arredondados</b>. |
| <b>Distância X Do Chanfro</b> <i>Flutuante</i> | Ajusta a distância do chanfro no eixo <b>X</b> <i>somente</i>. Essa distância depende do valor do parâmetro <b>Modo de distância de chanfro</b>.<br><br><i>Observação</i>: esse parâmetro só está disponível quando o parâmetro <b>Habilitar por controle de chanfro de eixo</b> está definido como <i>True</i>. |
| <b>Distância Y do chanfro</b> <i>Flutuante</i> | Ajusta a distância do chanfro no eixo <b>Y</b> <i>somente</i>. Essa distância depende do valor do parâmetro <b>Modo de distância de chanfro</b>.<br><br><i>Observação</i>: esse parâmetro só está disponível quando o parâmetro <b>Habilitar por controle de chanfro de eixo</b> está definido como <i>True</i>. |
| <b>Máscara</b> |  |
| <b>Inversão aleatória da máscara</b> <i>Booleano</i> | Inverte a máscara aleatória de formas. |
| <b>Início aleatório da máscara</b> <i>Flutuante</i> | Para uma determinada <b>Distribuição aleatória</b>, o mascaramento pseudoaleatório é aplicado seguindo uma <i>ordem específica</i> de uma forma inicial para uma forma final. Este parâmetro permite <i>deslocar o índice</i> da forma <i>inicial</i>.<br><br><i>Observação</i>: isso determina um limite de um <i>intervalo de valores</i> para mascaramento. Portanto, o valor pode ser <i>maior</i> do que o valor de <b>Fim aleatório da máscara</b>. |
| <b>Fim aleatório da máscara</b> <i>Flutuante</i> | Para uma determinada <b>Distribuição aleatória</b>, o mascaramento pseudoaleatório é aplicado seguindo uma <i>ordem específica</i> de uma forma inicial para uma forma final. Este parâmetro permite <i>deslocar o índice</i> da forma <i>fim</i>.<br><br><i>Observação</i>: isso determina um limite de um <i>intervalo de valores</i> para mascaramento. Portanto, o valor pode ser <i>maior</i> do que o valor de <b>Início aleatório da máscara</b>. |
| <b>Inverter máscara por área da célula</b> <i>Booleano</i> | Inverte o mascaramento de formas pela área de suas células. |
| <b>Início da Máscara por Área de Célula</b> <i>Flutuante</i> | Ajusta o <i>limite mínimo</i> da área da célula para mascaramento de formas.<br><br><i>Observação</i>: isso determina um limite de um <i>intervalo de valores</i> para mascaramento. Portanto, o valor pode ser <i>maior</i> do que o valor <b>Fim da Máscara por Área de Célula</b>. |
| <b>Fim da Máscara por Área de Célula</b> <i>Flutuante</i> | Ajusta o <i>limite máximo</i> da área da célula para mascaramento de formas.<br><br><i>Observação</i>: isso determina um limite de um <i>intervalo de valores</i> para mascaramento. Portanto, o valor pode ser <i>menor</i> do que o valor <b>Início da Máscara por Área de Célula</b>. |
| <b>Inversão de entrada de mapa de máscara</b> <i>Booleano</i> | Inverte o mascaramento de formas pelo mapa de entrada <b>Mapa de máscaras</b>. |
| <b>Início da Entrada do Mapa de Máscaras</b> <i>Flutuante</i> | Ajusta o <i>limite mínimo de valor em tons de cinza</i> no mapa de entrada <b>Mapa de Máscaras</b> para mascarar formas.<br><br><i>Observação</i>: isso determina um limite de <i>intervalo de valores</i> para mascaramento. Portanto, o valor pode ser <i>maior</i> do que o valor <b>Fim de entrada do mapa de máscaras</b>. |
| <b>Fim da Entrada do Mapa de Máscaras</b> <i>Flutuante</i> | Ajusta o <i>limite máximo de valor em tons de cinza</i> no mapa de entrada do <b>Mapa de máscaras</b> para formas de mascaramento.<br><br><i>Observação</i>: isso determina um limite de <i>intervalo de valores</i> para mascaramento. Portanto, o valor pode ser <i>menor</i> do que o valor de <b>Início da Entrada do Mapa de Máscaras</b>. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-inputs.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-demo.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-demo2.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-random-2.resources/tilerandom2-node.png" />
        </td>
    </tr>
</table>
