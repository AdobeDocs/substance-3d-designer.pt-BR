---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/plane-light.html"
breadcrumb-title: ''
description: Use o nó Luz de plano para adicionar fontes de luz planar a ambientes HDRI para controle de iluminação direcional.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Plane Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Luz do plano
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 4%

---


# Luz do plano

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](plane-light.resources/plane-light-01.png){width="200px"}

<b>Entrada:</b> Visualização 3D > Ferramenta HDRI

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera uma forma plana projetada esfericamente. O plano pode ser colocado e orientado em 3d usando os parâmetros de entrada.

Ela difere da [Luz de forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md) mais simples, pois tem opções de posicionamento mais avançadas fora da projeção de Distância da origem mais simples e mais padrões e máscaras podem ser aplicados, semelhante à [Luz de linha](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/line-light/line-light.md).

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
| <b>Posição UV do plano</b> | Somente com chão / teto e Distância da origem. Define a posição do plano no espaço UV. |
| <b>Posição Mundial do Plano</b> <i>-2.0 - 2.0</i> | Somente com o modo Posições Mundiais. Define o espaço mundial da posição do plano. Não há suporte para interação com o Visualização 2D. |
| <b>Height Absoluto de Plano</b> <i>0.0 - 1.0</i> | Somente com o modo de posição do solo/teto, define o height absoluto a partir do teto. Use Mostrar grade terrestre para estimar melhor a posição. |
| <b>Distância da origem</b> <i>0.0 - 1.0</i> | Somente com o Modo de posição de Distância da origem. Define a distância a partir do centro do panorama para ambos os pontos. |
| <b>Modo de Cores da Forma</b> <i>RGB, Temperatura (Kelvin), Entrada De Imagem</i> | Escolha o método a ser usado para definir a cor da forma. A Entrada de imagem permite o uso do segundo slot de entrada. |
| <b>Cor</b> <i>(Valor da cor)</i> | Somente com o Modo de cor da forma definido como RGB. Escolhe a cor da forma. |
| Temperatura <b>1</b> <i>800.0 - 20000.0</i> | Somente com o Modo de cor da forma definido como Temperatura. Define o valor de Kelvin para a cor da forma. |
| <b>Modo UV de Imagem de Forma</b> <i>Esticar, Esticar apenas no meio, Repetir + Espaçamento</i> | Somente com o Modo de cor da forma definido como Entrada de imagem. Define como a imagem é aplicada à forma de linha e determina o comportamento de repetição UV. |
| <b>Espaçamento de repetição da imagem da forma</b> <i>0.0 - 1.0</i> | Somente com o Modo de cor da forma definido como Entrada de imagem e com o Modo UV definido como Repetir + Espaçamento. Define a quantidade de espaçamento quando a imagem se repete ao longo da linha. |
| <b>Gama de Imagem da Forma</b> <i>sRGB, Linear</i> | Somente com o Modo de cor da forma definido como Entrada de imagem. Determine como interpretar a entrada de imagem de forma. |
| <b>Exposição (EV)</b> <i>0.0 - 10.0</i> | Defina o valor de exposição para a forma gerada, de forma ideal para o valor de exposição da imagem de plano de fundo. |
| <b>Escala do plano</b> <i>0.0 - 1.0</i> | Defina a escala uniforme da forma Plano. |
| <b>Tamanho do plano</b> <i>0.0 - 1.0</i> | Defina o tamanho não uniforme da forma Plano. |
| <b>Rotação do plano</b> <i>0.0 - 1.0</i> | Girar plano ao longo de seu eixo central. |
| <b>Padrão</b> <i>Quadrado Suave, Quadrado Nítido, Cone, Hemisfério, Entrada de Imagem</i> | Selecione a forma de padrão a ser usada. |
| <b>Dureza de padrão</b> <i>0.0 - 1.0</i> | Definir dureza/contraste do padrão. |
| <b>Modo UV de padrão</b> <i>Esticar, Esticar apenas no meio</i> | Definir como usar a máscara de padrão secundária, aplicada sobre a Imagem da Forma. |
| <b>Habilitar recorte terrestre</b> <i>Falso/Verdadeiro</i> | Habilite se o plano pode ser cortado por um plano terrestre ou ainda é mostrado quando estiver abaixo dele. Use Mostrar grade terrestre para estimar melhor isso. |
| <b>Height terrestre</b> <i>-2.0 - 0.0</i> | Ajuste o height do solo para recorte. |
| <b>Habilitar Entrada em Segundo Plano</b> <i>Falso/Verdadeiro</i> | Alterna o uso da imagem de fundo opcional. Os compostos geraram luz na parte superior do plano de fundo. |
| <b>Cor do plano de fundo</b> <i>(Valor da cor)</i> | Se a Entrada do plano de fundo não for usada, defina um valor de plano de fundo de cor sólida aqui. |
| <b>Gama de Plano de Fundo</b> <i>sRGB, Linear</i> | Se a Entrada em segundo plano for usada, defina como interpretar a entrada em segundo plano. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="plane-light.resources/plane-light-02.gif" />
        </td>
    </tr>
</table>
