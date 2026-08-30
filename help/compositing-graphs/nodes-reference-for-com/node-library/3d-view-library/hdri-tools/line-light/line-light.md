---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/line-light.html"
breadcrumb-title: ''
description: Use o nó Luz de linha para criar fontes de luz linear em ambientes HDRI para simular iluminação fluorescente e de faixa.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Line Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luz de linha
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '707'
ht-degree: 3%

---


# Luz de linha

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](line-light.resources/panorama-line-light.png){width="200px"}

<b>Entrada:</b> Visualização 3D > Ferramenta HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma forma de linha projetada esfericamente com base nas coordenadas de dois pontos no espaço. Em comparação à [Luz de forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md), ela tem mais opções para orientar formas e aplicar padrões repetidos à forma de luz.

Os modos de posicionamento para este nó são ligeiramente mais complexos do que outros nós de luz HDRI. É recomendável experimentar alguns modos de tamanho diferentes para descobrir qual funciona para o seu cenário.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada de imagem de fundo</b> <i>Entrada de cores</i> | Fundo opcional no qual compor a luz gerada. |
| <b>Entrada de Imagem de Forma</b> <i>Entrada de cores</i> | Imagem opcional para mapear para a luz da linha. Usado somente quando o Modo de cor da forma está definido como Entrada de imagem. |
| <b>Entrada de imagem de padrão</b> <i>Entrada em tons de cinza</i> | Imagem de padrão personalizado, usada quando o parâmetro “Pattern” está definido como “Image Input”. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Modo de Posição</b> <i>Solo/Teto, Distância da origem, Posições Mundiais</i> | Selecione um dos três modos diferentes de inserção. O solo/teto e a Distância da origem suportam a manipulação na visualização 2D, as posições do mundo só podem ser alteradas por meio de propriedades, mas suportam um posicionamento mais exato. |
| <b>Mostrar grade terrestre</b> <i>Falso/Verdadeiro</i> | Função auxiliar para habilitar o desenho de uma grade de aterramento de depuração. Ajuda a estimar a posição das linhas no espaço. |
| <b>Coordenadas de Posição</b> |  |
| <b>Vetor para cima</b> <i>Z Para Cima, Y Para Cima</i> | Somente com o modo Posição mundial, determine a orientação do sistema de coordenadas. |
| <b>Posição UV de ponto 1</b> | Somente com chão / teto e Distância da origem. Define a posição do primeiro ponto no espaço UV. |
| <b>Posição UV de ponto 2</b> | Somente com chão / teto e Distância da origem. Define a segunda posição de ponto no espaço UV. |
| <b>Posição Mundial do Ponto 1</b> <i>-2.0 - 2.0</i> | Somente com o modo Posições Mundiais. Define o primeiro ponto no espaço global. Não há suporte para interação de exibição 2D. |
| <b>Posição Mundial do Ponto 2</b> <i>-2.0 - 2.0</i> | Somente com o modo Posições Mundiais. Define o segundo ponto no espaço global. Não há suporte para interação de exibição 2D. |
| <b>Height Absoluto de Linha</b> <i>0.0 - 1.0</i> | Somente com o modo de posição do solo/teto, define o height absoluto a partir do teto. Use Mostrar grade terrestre para estimar melhor a posição. |
| <b>Distância da origem</b> <i>0.0 - 1.0</i> | Somente com o Modo de posição de Distância da origem. Define a distância a partir do centro do panorama para ambos os pontos. |
| <b>Modo de Cores da Forma</b> <i>RGB, Temperatura (Kelvin), Entrada De Imagem</i> | Escolha o método a ser usado para definir a cor da forma. A Entrada de imagem permite o uso do segundo slot de entrada. |
| <b>Cor</b> <i>(Valor da cor)</i> | Somente com o Modo de cor da forma definido como RGB. Escolhe a cor da forma. |
| Temperatura <b>1</b> <i>800.0 - 20000.0</i> | Somente com o Modo de cor da forma definido como Temperatura. Define o valor de Kelvin para a cor da forma. |
| <b>Modo UV de Imagem de Forma</b> <i>Esticar, Esticar apenas no meio, Repetir + Espaçamento</i> | Somente com o Modo de cor da forma definido como Entrada de imagem. Define como a imagem é aplicada à forma de linha e determina o comportamento de repetição UV. |
| <b>Espaçamento de repetição da imagem da forma</b> <i>0.0 - 1.0</i> | Somente com o Modo de cor da forma definido como Entrada de imagem e com o Modo UV definido como Repetir + Espaçamento. Define a quantidade de espaçamento quando a imagem se repete ao longo da linha. |
| <b>Gama de Imagem da Forma</b> <i>sRGB, Linear</i> | Somente com o Modo de cor da forma definido como Entrada de imagem. Determine como interpretar a entrada de imagem de forma. |
| <b>Exposição (EV)</b> <i>0.0 - 10.0</i> | Defina o valor de exposição para a forma gerada, de forma ideal para o valor de exposição da imagem de plano de fundo. |
| <b>Rotação de Linha</b> <i>0.0 - 1.0</i> | Gira a linha ao longo do eixo de seu comprimento. A linha é tratada como uma placa plana ao girar. |
| <b>Thickness de linha</b> <i>0.0 - 1.0</i> | Define o thickness da placa de linha. |
| <b>Padrão</b> <i>Quadrado Suave, Quadrado Nítido, Cone, Hemisfério, Entrada de Imagem</i> | Selecione a forma de padrão a ser usada. |
| <b>Dureza de padrão</b> <i>0.0 - 1.0</i> | Definir dureza/contraste do padrão. |
| <b>Modo UV de padrão</b> <i>Esticar, Esticar apenas no meio, Repetir + Espaçamento</i> | Definir como usar a máscara de padrão secundária, aplicada sobre a Imagem da Forma. |
| <b>Espaçamento de repetição de padrão</b> <i>0.0 - 1.0</i> | Somente se o Modo UV de padrão estiver definido como Repetição + Espaçamento. Defina a quantidade de espaçamento entre os padrões repetidos. |
| <b>Habilitar recorte terrestre</b> <i>Falso/Verdadeiro</i> | Habilitar corte de desenho de linha. O efeito não é visível ao usar o modo de posicionamento Terra/Teto. |
| <b>Height terrestre</b> <i>-2.0 - 0.0</i> | Define o height relativo do plano frontal, usado para recorte. Afeta a grade do solo desenhada. |
| <b>Habilitar Entrada em Segundo Plano</b> <i>Falso/Verdadeiro</i> | Alterna o uso da imagem de fundo opcional. Os compostos geraram luz na parte superior do plano de fundo. |
| <b>Cor do plano de fundo</b> <i>(Valor da cor)</i> | Se a Entrada do plano de fundo não for usada, defina um valor de plano de fundo de cor sólida aqui. |
| <b>Gama de Plano de Fundo</b> <i>sRGB, Linear</i> | Se a Entrada em segundo plano for usada, defina como interpretar a entrada em segundo plano. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="line-light.resources/line-light-ex.gif" />
        </td>
    </tr>
</table>
