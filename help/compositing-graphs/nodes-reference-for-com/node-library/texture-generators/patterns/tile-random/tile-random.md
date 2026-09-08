---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random.html"
breadcrumb-title: ''
description: Use o nó Aleatório de blocos para criar padrões de blocos aleatórios com variação processual para efeitos de textura orgânicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Lado a lado aleatório
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 7%

---


# Lado a lado aleatório

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/tile-random.png){width="128px"}

<b>Em:</b> Geradores > Padrões

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O Bloco Aleatório gera um padrão de bloco processual que tem um pouco mais de caos nas formas do bloco do que seu correspondente, [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md). Ele faz isso dividindo aleatoriamente certos ladrilhos em ladrilhos menores. Sugerimos que você primeiro encontre o seu caminho em torno do Tile Generator antes de abordar o Telha Aleatória, como muitos conceitos são semelhantes.

O Bloco Aleatório é usado em vez de [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md) quando a meta é um padrão mais antigo e menos organizado. No entanto, ele tem suas limitações. Portanto, considere o [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) para atender a quaisquer outras necessidades avançadas.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada de padrão</b> <i>Entrada em Tons de Cinza (Entrada de Cores)</i> | Imagem de padrão personalizado, usada quando o parâmetro “Pattern” está definido como “Image Input”. |
| <b>Entrada em segundo plano</b> <i>Entrada em tons de cinza (entrada Colorida)</i> |  |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Valor X</b> <i>1 - 64</i> | Quantidade de repetições X do padrão. |
| <b>Valor Y</b> <i>1 - 64</i> | Quantidade de repetições Y do padrão. |
| <b>Expansão não quadrada</b> <i>Falso/Verdadeiro</i> | Permite a compensação de esmagamento e alongamento com proporções não quadradas. |
| <b>Padrão</b> |  |
| <b>Padrão</b> <i>Entrada de Padrão, Quadrado, Disco, Parabolóide, Sino, Gaussiano, Espinho, Pirâmide, Tijolo, Gradação, Ondas, Meio sino, Sino Ondulado, Crescente, Cápsula, Cone</i> | Seleciona a forma de padrão a ser usada. |
| <b>Filtragem de Entrada de Imagem (Mecanismo > v4)</b> <i>Bilinear + Mipmaps, Bilinear, Mais Próximo</i> |  |
| <b>Específico de Padrão</b> <i>0.0 - 1.0</i> | Permite que você altere a forma do padrão selecionado. O efeito depende do padrão selecionado. |
| <b>Aleatório Específico de Padrão</b> <i>0.0 - 1.0</i> | O efeito de aleatorização depende do padrão selecionado. |
| <b>Rotação</b> <i>0, 90, 180, 270, aleatório horizontal, aleatório vertical</i> | Define a rotação em etapas de 90 graus, com aleatorização opcional. |
| <b>Rotação aleatória</b> <i>0.0 - 1.0</i> | Adiciona rotação livre aleatória. |
| <b>Simetria aleatoriamente</b> <i>0.0 - 1.0</i> | Espelha aleatoriamente certos padrões pelo modo aleatório de Simetria selecionado. Quanto maior for esse valor, mais padrões serão espelhados. |
| <b>Modo Aleatório de Simetria</b> <i>Horizontal + Vertical, Horizontal, Vertical</i> | Determina o comportamento de espelhamento quando a Simetria aleatória é maior que 0. |
| <b>Dividir</b> |  |
| <b>Modo</b> <i>nenhum, automático, horizontal automático, vertical automático, h+v aleatório</i> | Define a regra de divisão de blocos. |
| <b>Limite</b> <i>0.0 - 1.0</i> | Limite de tamanho para quando dividir um bloco. |
| <b>Multiplicador</b> <i>0 - 10</i> | Dividindo multiplicador. Quanto maior esse valor, mais divisões. |
| <b>Tamanho</b> |  |
| <b>X Aleatório</b> <i>0.0 - 1.0</i> | Dispõe aleatoriamente um dimensionamento não uniforme sobre o eixo X. |
| <b>Y Aleatório</b> <i>0.0 - 1.0</i> | Dispõe aleatoriamente um dimensionamento não uniforme sobre o eixo Y. |
| <b>Interstício</b> |  |
| <b>Modo</b> <i>Em relação ao menor tijolo, em relação ao maior tijolo</i> | Define a que tamanho de tijolo o interstício está relativo. |
| <b>Valor</b> <i>0.0 - 1.0</i> | Define o tamanho do espaço entre os tijolos. |
| <b>Forma</b> |  |
| <b>Escala</b> <i>0.0 - 1.0</i> | Dimensiona globalmente todos os ladrilhos. |
| <b>Escala aleatória</b> <i>0.0 - 1.0</i> | Escala aleatória por bloco. |
| <b>Rotação</b> <i>0.0 - 1.0</i> | Rotação global para cada ladrilho. |
| <b>Rotação aleatória</b> <i>0.0 - 1.0</i> | Gira aleatoriamente por ladrilho. |
| <b>Restrição de Rotação</b> <i>Falso/Verdadeiro</i> | Restringe a escala para que os blocos gráficos girados nunca se sobreponham. |
| <b>Posição</b> |  |
| <b>Deslocamento</b> <i>0.0 - 1.0</i> | Move ou traduz os ladrilhos globalmente, desliza somente no eixo X |
| <b>Deslocamento Aleatório</b> <i>0.0 - 1.0</i> | Deslocamento aleatório por bloco, slides somente sobre o eixo X |
| <b>Aleatório</b> <i>0.0 - 1.0</i> | Dispõe aleatoriamente a posição, os blocos se movem nos eixos X e Y. |
| <b>Restrições Aleatórias</b> <i>Falso/Verdadeiro</i> | Restringe a escala para que os blocos toquem, mas não se sobreponham. Reduz significativamente o efeito Posição aleatória. |
| <b>Cor</b> |  |
| <b>Cor</b> <i>(Valor em tons de cinza) / (Valor da cor)</i> | Define cores sólidas para todos os ladrilhos. |
| <b>Cores aleatórias</b> <i>0.0 - 1.0</i> | Dispõe as cores de maneira aleatória, lado a lado. |
| <b>Parametrização de Cor</b> <i>nenhuma, área, tamanho x, tamanho y</i> | Torna a variação de cor dependente de uma dessas configurações. |
| <b>Intensidade de parametrização de cor</b> <i>0.0 - 1.0</i> | Multiplicador do efeito Parametrização acima. |
| <b>Efeito de Parametrização de Cor (somente para Cor)</b> <i>RGB+Alpha, somente RGB, somente Alpha</i> | Determina o efeito de parametrização somente de cor. |
| <b>Cor do plano de fundo</b> <i>(Valor em tons de cinza) / (Valor da cor)</i> | Define a cor sólida do plano de fundo. |
| <b>Modo de Mesclagem</b> <i>Adicionar/Sub, Máximo/Adicionar/Sub, Combinar de Alpha (Cor)</i> | Define o modo de mesclagem para ladrilhos no plano de fundo. |
| <b>Máscara</b> |  |
| <b>Aleatório</b> <i>0.0 - 1.0</i> | Inicia aleatoriamente o mascaramento dos blocos. Quanto maior o valor, mais blocos desaparecem. |
| <b>Inverter</b> <i>Falso/Verdadeiro</i> | Inverte o resultado da máscara. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/tile-random-1.png" />
        </td>
    </tr>
</table>
