---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-sampler.html"
breadcrumb-title: ''
description: Use o nó Sampler lado a lado para obter amostras e organizar blocos de texturas de entrada para criar padrões lado a lado no Substance 3D Designer.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Sampler
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bloco Sampler
user-guide-description: ''
user-guide-title: ''
source-git-commit: b63bc7a45aa6eadef1b72eb05d4a6aded05866a8
workflow-type: tm+mt
source-wordcount: '1060'
ht-degree: 6%

---


# Bloco Sampler

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tile-sampler.resources/tile-sampler.png){width="128px"}

<b>Em:</b> Geradores De Textura > Padrões

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Tile Sampler é o último nó de geração de padrão de ladrilho. É uma versão evoluída e mais complexa do [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). A partir do 2017 2.1, as diferenças são muito menores entre o Tile Sampler e o [Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). As principais diferenças estão agora apenas nos sete diferentes slots de mapa que estão disponíveis para dirigir a Escala, Posição, Rotação, Tamanho, Cor e Mascaramento. Seu efeito pode ser mesclado separadamente.

O Tile Sampler é útil para criar padrões de procedimentos feitos pelo homem, com controle adicional sobre determinados parâmetros orientados por mapas de entrada externos.

Certifique-se de estar familiarizado com o [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) antes de passar para o Tile Sampler. Na maioria dos casos, você encontrará [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) o suficiente e não precisará da complexidade adicional de Tile Sampler.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada de padrão 1-6</b> <i>Entrada em tons de cinza/Entrada de cores</i> | Imagem de padrão personalizado, usada quando o parâmetro “Pattern” está definido como “Image Input”.<br><br>A quantidade de entradas disponíveis é determinada pelo parâmetro <b>Número de Entrada de Padrão</b>. |
| <b>Entrada de Mapa de Escala</b> <i>Entrada em tons de cinza</i> | Mapa em tons de cinza para dimensionar o ladrilho. |
| <b>Entrada do Mapa de Deslocamentos</b> <i>Entrada em tons de cinza</i> | Mapa em tons de cinza para o deslocamento de peças de unidade. |
| <b>Entrada de Mapa de rotação</b> <i>Entrada em tons de cinza</i> | Mapa em tons de cinza para girar o ladrilho. |
| <b>Entrada do Mapa Vetorial</b> <i>Entrada de cores</i> | Mapa de vetor de cores para direcionar um dimensionamento não uniforme. |
| <b>Entrada do Mapa de Cores</b> <i>Entrada em tons de cinza/Entrada de cores</i> | Mapa para orientar o matiz por ladrilho. |
| <b>Entrada do mapa de máscaras</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para ocultar certos blocos. |
| <b>Entrada do Mapa de Distribuição de Padrões</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para direcionar várias entradas de padrão personalizadas. |
| <b>Entrada em segundo plano</b> <i>Entrada em tons de cinza/Entrada de cores</i> | Imagem de fundo opcional. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Valor X</b> <i>0 - 64</i> | Quantidade de repetições X do padrão. |
| <b>Valor Y</b> <i>0 - 64</i> | Quantidade de repetições Y do padrão. |
| <b>Expansão não quadrada</b> <i>Falso/Verdadeiro</i> | Permite a compensação de esmagamento e alongamento com proporções não quadradas. |
| <b>Padrão</b> |  |
| <b>Padrão</b> <i>Entrada de padrão, Quadrado, Disco, Parabolóide, Sino, Gaussiano, Espinho, Pirâmide, Tijolo, Gradação, Ondas, Meio sino, Sino ondulado, Crescente, Cápsula, Cone</i> | Seleciona a forma de padrão a ser usada. |
| <b>Número de Entrada de Padrão</b> <i>1 - 6</i> | Quantidade de padrões personalizados para escolher aleatoriamente. |
| <b>Distribuição de Entrada de Padrão</b> <i>Aleatório, Número de Padrão, Mapa de Distribuição</i> | Define como várias Entradas de Padrão são escolhidas. Aleatório significa que um aleatório foi escolhido, Número de padrão significa que eles foram colocados em uma sequência em loop. O mapa de distribuição usa uma entrada de mapa em tons de cinza para o posicionamento da unidade. |
| <b>Filtragem de Entrada de Padrão (Mecanismo > v4)</b> <i>Bilinear + Mipmaps, Bilinear, Mais Próximo</i> |  |
| <b>Específico de Padrão</b> <i>0.0 - 1.0</i> | Permite que você altere a forma do padrão selecionado. O efeito depende do padrão selecionado. |
| <b>Aleatório Específico de Padrão</b> <i>0.0 - 1.0</i> | O efeito de aleatorização depende do padrão selecionado. |
| <b>Rotação</b> <i>0, 90, 180, 270</i> | Rotação controlada (90 graus). |
| <b>Rotação aleatória</b> <i>0.0 - 1.0</i> | Rotação livre aleatória por bloco. |
| <b>Simetria aleatoriamente</b> <i>0.0 - 1.0</i> | Define o número de ladrilhos que devem ser invertidos/espelhados aleatoriamente, de acordo com o comportamento abaixo. |
| <b>Modo Aleatório de Simetria</b> <i>Horizontal + Vertical, Horizontal, Vertical</i> | Determina o comportamento de espelhamento da simetria. |
| <b>Tamanho</b> |  |
| <b>Modo de Tamanho</b> <i>Normal, Manter Proporção, Absoluto, Pixel</i> | Define o comportamento geral do tamanho do padrão.<br><br>Normal permite definir o tamanho dos elementos do padrão. É afetada pelo valor X e Y.<br><br>Manter proporção permite definir um tamanho afetado pela quantidade X e Y, mas a proporção X e Y entre os dois permanece intacta.<br><br>Absoluto permite definir um tamanho absoluto que não é afetado pela quantidade X e Y.<br><br>Pixel permite definir um tamanho absoluto em pixels, não afetado pela quantidade de X e Y. Alterar a resolução afetará o tamanho dos elementos. |
| <b>Tamanho (Absoluto/Pixel)</b> <i>0.0 - 1.0</i> | Altera proporções não uniformes para ladrilhos. O comportamento exato depende do Modo de Tamanho. |
| <b>Tamanho aleatório</b> <i>0.0 - 1.0</i> | Dispõe aleatoriamente as proporções por bloco. |
| <b>Escala</b> <i>0.0 - 10.0</i> | Define a escala do ladrilho global. |
| <b>Escala aleatória</b> <i>0.0 - 1.0</i> | Dispõe aleatoriamente a escala por ladrilho. |
| <b>Multiplicador de Mapa de Escala</b> <i>0.0 - 1.0</i> | Combinar no efeito do Mapa de escala. |
| <b>Multiplicador de Mapa Vetorial de Escala</b> <i>0.0 - 1.0</i> | Combinar no efeito do mapa vetorial de escala para orientar o dimensionamento não uniforme. |
| <b>Efeito de Parametrização de Escala</b> <i>X e Y, X, Y</i> | Define quais eixos a parametrização de escala afeta. Pode ser usado para fazer com que o Mapa de escala afete apenas os elementos X ou Y. |
| <b>Posição</b> |  |
| <b>Posição Aleatória</b> <i>0.0 - 10.0</i> | Dispõe aleatoriamente a posição do ladrilho sobre os dois eixos. |
| <b>Deslocamento</b> <i>0.0 - 1.0</i> | Desloca os blocos de acordo com o Tipo de deslocamento. |
| <b>Tipo de Deslocamento</b> <i>quincux horizontal, quincux vertical, global horizontal, global vertical</i> | Altera em qual direção o Deslocamento opera. |
| <b>Deslocamento global</b> <i>0.0 - 1.0</i> | Desloca globalmente todos os ladrilhos nos eixos X ou Y. |
| <b>Intensidade do Mapa de Deslocamentos</b> <i>0.0 - 1.0</i> | Combinar na intensidade do mapa de Deslocamento no deslocamento. |
| <b>Ângulo do Deslocamento</b> <i>0.0 - 1.0</i> | Define o ângulo em que a mesclagem será feita. |
| <b>Deslocamento de Mapas Vetoriais</b> <i>0.0 - 1.0</i> | Usa o mapa de vetor para orientar o deslocamento e o ângulo. |
| <b>Rotação</b> |  |
| <b>Rotação</b> <i>0.0 - 1.0</i> | Gira globalmente todos os blocos gráficos. |
| <b>Rotação aleatória</b> <i>0.0 - 1.0</i> | Gira aleatoriamente por bloco. |
| <b>Multiplicador de Mapa de rotação</b> <i>0.0 - 1.0</i> | Combinar no efeito de Mapa de rotação na rotação por bloco. |
| <b>Multiplicador de Mapa Vetorial</b> <i>0.0 - 1.0</i> | Usa o Mapa de vetores para orientar a rotação por ladrilho. |
| <b>Cor</b> |  |
| <b>Limite de mapa de máscaras</b> <i>0.0 - 1.0</i> | Limite do mapa de máscaras quando iniciar a ocultação de ladrilhos. |
| <b>Inversão de mapa de máscara</b> <i>Falso/Verdadeiro</i> | Inverte o efeito de mapa de máscara. |
| <b>Técnica de amostragem de mapa de máscara</b> <i>Centro do Padrão, Caixa Delimitadora do Padrão (mais lento)</i> | Se a ocultação deve ser determinada por um único ponto ou por uma caixa delimitadora. Evita pixels isolados, causando efeitos estranhos. |
| <b>Máscara aleatória</b> <i>0.0 - 1.0</i> | O mascaramento aleatório funciona em paralelo com o mapa de máscara. |
| <b>Inverter máscara</b> <i>Falso/Verdadeiro</i> | Inverte a máscara aleatória. |
| <b>Modo de Mesclagem</b> <i>Adicionar/Sub, Máximo (Tile Sampler)/Adicionar/Sub, Combinar de Alpha (Tile Sampler Color)</i> | modo Combinar para ladrilhos no plano de fundo e entre si. |
| <b>Cor</b> <i>(Valor em tons de cinza) / (Valor da cor)</i> | Cor de ladrilho sólida e global. |
| <b>Cor/Luminância Aleatória</b> <i>0.0 - 1.0</i> | Aleatoriedade de cor por bloco. |
| <b>Modo de Parametrização de Cores</b> <i>Entrada de Cores, Escala, Índice de Linhas, Índice de Linhas, Índice de Padrões (Sampler Ladrilho)/Mapa de Cores, Escala, Índice de Linhas, Índice de Linhas, Índice de Padrões, Posição Central do Padrão, Posição Central do Padrão (RG), Tamanho da esfera (B) (Cor Sampler Ladrilho)</i> | Define como exatamente a aleatoriedade de cores é parametrizada. |
| <b>Multiplicador de Parametrização de Cores</b> <i>0.0 - 1.0</i> | Combinar no efeito Parametrização acima. |
| <b>Efeito de Parametrização de Cor (somente Cor)</b> <i>RGB+Alpha, somente RGB, somente Alpha</i> | Define como a Parametrização afeta a cor. |
| <b>Opacidade global (somente tons de cinza)</b> <i>0.0 - 1.0</i> | Define a opacidade global do ladrilho. |
| <b>Cor do plano de fundo</b> <i>(Valor em tons de cinza) / (Valor da cor)</i> | Define a cor sólida do plano de fundo. |
| <b>Inverter ordem de renderização</b> <i>Falso/Verdadeiro</i> | Inverte a ordem de renderização para ir de trás para frente. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="tile-sampler.resources/tilesampler-ex2.png" /><br><i>O exemplo mostra como os parâmetros são orientados por mapas de entrada (Distribuição de Padrões, Escala, Rotação).</i>
        </td>
    </tr>
</table>
