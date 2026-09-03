---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-generator.html"
breadcrumb-title: ''
description: Use o nó Tile Generator para criar padrões de ladrilhos de procedimento com controles personalizáveis de tamanho, deslocamento e variação.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Gerador de blocos
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 6%

---


# Gerador de blocos

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tile-generator.resources/tile-generator-01.png){width="128px"}

<b>Em:</b> Geradores De Textura > Padrões

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O Tile Generator é um dos nós mais avançados da biblioteca. Se aprender a dominá-lo, você pode criar qualquer tipo de padrão (dentro de algumas limitações). A partir da versão 2017 2.1, houve algumas grandes atualizações, tornando esse nó mais alinhado com o que o [Tile Sampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md) pode fazer.

Este nó é altamente útil para uma variedade de cenários, mas tenha em mente que a simples leitura de parâmetros não ensinará totalmente como usá-los. Sugerimos que você experimente também!

Em 99% dos casos, a versão colorida NÃO é necessária.

Algumas dicas de uso geral:

* Você pode começar com uma forma básica, mas se tiver uma entrada personalizada (Defina **Tipo de Padrão** para *Entrada de Imagem*), crie-a primeiro! Determina muito o visual.
* Comece definindo corretamente os valores X e Y.
* Encontre o modo **Tamanho** correto: modos relativos, como **Interstício**, se comportam de maneira bem diferente dos modos **Absolutos**.
* Ajuste a **Escala** global e o **Tamanho** não uniforme em seguida.
* Por fim, ajuste qualquer parâmetro de **”Variação”** até que ele atenda às suas necessidades. Sutileza é a chave com variação!

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Entrada de padrão 1-6</b> <i>Entrada em tons de cinza</i> | Imagem de padrão personalizado, usada quando o parâmetro “Pattern” está definido como “Image Input”. |
| <b>Fundo</b> <i>Entrada em tons de cinza</i> | Plano de fundo a ser usado em vez da cor sólida. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Valor X</b> <i>1 - 64</i> | Quantidade de repetições X do padrão. |
| <b>Valor Y</b> <i>1 - 64</i> | Quantidade de repetições Y do padrão. |
| <b>Expansão não quadrada</b> <i>Falso/Verdadeiro</i> | Permite a compensação de esmagamento e alongamento com proporções não quadradas. |
| <b>Padrão</b> |  |
| <b>Padrão</b> <i>Entrada De Imagem, Quadrado, Disco, Parabolóide, Sino, Gaussiano, Espinho, Pirâmide, Tijolo, Gradação, Ondas, Meio sino, Sino Ondulado, Crescente, Cápsula, Cone</i> | Seleciona a forma de padrão a ser usada. |
| <b>Número de Entrada de Padrão</b> <i>1 - 6</i> | Número de entradas de Imagem diferentes a serem usadas. Disponível somente quando a <i>Entrada de imagem</i> está selecionada acima. |
| <b>Distribuição de Entrada de Padrão</b> <i>Aleatório, Por Número De Padrão</i> | Como escolher entre as diferentes entradas de imagem, se mais de 1 estiver selecionado. |
| <b>Específico de Padrão</b> <i>0.0 - 1.0</i> | Permite que você altere a forma do padrão selecionado. O efeito depende do padrão selecionado. |
| <b>Filtragem de Entrada de Imagem (Mecanismo >v4 apenas)</b> <i>Bilinear + Mipmaps, Bilinear, Mais Próximo</i> |  |
| <b>Rotação</b> <i>0, 90, 180, 270</i> | Gira todos os ladrilhos globalmente de acordo com um ângulo definido em etapas de 90 graus. |
| <b>Rotação aleatória</b> <i>0.0 - 1.0</i> | Girar aleatoriamente um ladrilho em uma de quatro etapas de 90 graus. |
| <b>Inversão de Quincunx</b> <i>Falso/Verdadeiro</i> | Gira todos os outros ladrilhos em 90 graus. |
| <b>Simetria aleatoriamente</b> <i>0.0 - 1.0</i> | Espelha aleatoriamente certos padrões pelo modo aleatório de Simetria selecionado. Quanto maior for esse valor, mais padrões serão espelhados. |
| <b>Modo Aleatório de Simetria</b> <i>Horizontal + Vertical, Horizontal, Vertical</i> | Determina o comportamento de espelhamento quando a Simetria aleatória é maior que 0. |
| <b>Tamanho</b> |  |
| <b>Modo de Tamanho</b> <i>Normal - Interstício, Normal - Tamanho, Manter Proporção, Absoluto, Pixel</i> | Define o comportamento geral do tamanho do padrão.<br><br>Normal - O Interstice permite definir a lacuna entre os elementos do padrão. É afetada pelo valor X e Y.<br><br>Normal - Tamanho permite que você defina o tamanho dos elementos do padrão, independentemente do espaço. É afetada pelo valor X e Y.<br><br>Manter proporção permite definir um tamanho afetado pela quantidade X e Y, mas a proporção X e Y entre os dois permanece intacta.<br><br>Absoluto permite definir um tamanho absoluto que não é afetado pela quantidade X e Y.<br><br>Pixel permite definir um tamanho absoluto em pixels, não afetado pela quantidade de X e Y. Alterar a resolução afetará o tamanho dos elementos. |
| <b>Tamanho Médio</b> <i>0.0 - 1.0</i> | Altera o tamanho em uma base de coluna e linha alternada. |
| <b>Interstício X/Y</b> <i>0.0 - 1.0</i> | Disponível somente no modo Normal - Tamanho intersticial. Altera o intervalo de interstício. Afeta a junção entre as formas. Permite um controle não uniforme, diferentemente da <b>Escala</b>. |
| <b>Tamanho (Absoluto/Pixel)</b> <i>0.0 - 1.0</i> | Disponível apenas fora de Normal - Modo de tamanho interstício. Define o tamanho não uniforme, diferentemente da <b>Escala</b>. |
| <b>Escala</b> <i>0.0 - 2.0</i> | Define a escala global. |
| <b>Escala aleatória</b> <i>0.0 - 1.0</i> | Define a variação da escala global por ladrilho. |
| <b>Dimensionar Distribuição Aleatória</b> <i>0 - 1000</i> | Desloca a semente de variação da escala. |
| <b>Posição</b> |  |
| <b>Deslocamento</b> <i>0.0 - 1.0</i> | Desloca o padrão inteiro incrementalmente em cada linha ou coluna consecutiva (o comportamento depende do parâmetro Deslocamento vertical). |
| <b>Deslocamento Aleatório</b> <i>0.0 - 1.0</i> | Dispõe aleatoriamente o deslocamento da linha. |
| <b>Deslocar Distribuição Aleatória</b> <i>0 - 1000</i> | Altera a velocidade relativa do efeito de deslocamento aleatório. |
| <b>Deslocamento vertical</b> <i>Falso/Verdadeiro</i> | Define se o efeito Deslocamento ocorre em linhas ou linhas; Horizontal ou Vertical. |
| <b>Posição Aleatória</b> <i>0.0 - 1.0</i> | Dispõe a posição de maneira não uniforme, com controle separado para X e Y. |
| <b>Deslocamento global</b> <i>0.0 - 1.0</i> | Desloca todo o resultado sobre os eixos X e Y. |
| <b>Rotação</b> |  |
| <b>Rotação</b> <i>0.0 - 1.0</i> | Faz uma Rotação livre uniforme de todos os ladrilhos padrão. |
| <b>Rotação aleatória</b> <i>0.0 - 1.0</i> | Dispõe aleatoriamente a rotação livre de todos os ladrilhos. Quanto maior o valor, mais blocos podem ser girados. |
| <b>Cor</b> |  |
| <b>Cor</b> <i>(Valor em tons de cinza)</i> | Define a cor sólida dos ladrilhos. |
| <b>Luminância/Cor Aleatória</b> <i>0.0 - 1.0</i> | Introduz a variação de Cor ou Luminância por ladrilho. |
| <b>Luminância por Número</b> <i>Falso/Verdadeiro</i> | Atenua a Luminância em todo o padrão. |
| <b>Luminância por escala</b> <i>Falso/Verdadeiro</i> | Torna a variação da Luminância dependente da escala do ladrilho. |
| <b>Máscara do verificador</b> <i>Falso/Verdadeiro</i> | Oculta todos os outros ladrilhos. |
| <b>Máscara horizontal</b> <i>Falso/Verdadeiro</i> | Oculta todas as outras colunas. |
| <b>Máscara vertical</b> <i>Falso/Verdadeiro</i> | Oculta todas as outras linhas. |
| <b>Máscara aleatória</b> <i>0.0 - 1.0</i> | Oculta ladrilhos aleatoriamente. Quanto maior esse valor, mais blocos desaparecerão. |
| <b>Inverter máscara</b> <i>Falso/Verdadeiro</i> | Inverte o resultado de quaisquer efeitos de mascaramento desta seção. |
| <b>Modo de Mesclagem</b> <i>Adicionar, Máx., Adicionar Sub</i> | Define o modo de mesclagem a ser usado. |
| <b>Cor do plano de fundo</b> <i>(Valor em tons de cinza)</i> | Define a cor sólida do plano de fundo. |
| <b>Opacidade Global</b> <i>0.0 - 1.0</i> | Define a opacidade de blocos globais. |
| <b>Inverter ordem de renderização</b> <i>Falso/Verdadeiro</i> | Renderiza os blocos de volta para a frente ou vice-versa. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="tile-generator.resources/tile-generator-02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-generator.resources/tile-generator-03.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-generator.resources/tile-generator-04.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="tile-generator.resources/tile-generator-05.png" />
        </td>
    </tr>
</table>
