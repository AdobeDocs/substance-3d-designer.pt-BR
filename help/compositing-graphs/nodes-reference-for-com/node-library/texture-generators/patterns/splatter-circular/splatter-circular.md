---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter-circular.html"
breadcrumb-title: ''
description: Use o nó Divisória circular para dispersão formas circulares nas texturas a fim de criar padrões orgânicos e aleatórios.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter Circular
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Espalhar Circular
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '850'
ht-degree: 8%

---


# Espalhar Circular

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](splatter-circular.resources/splatter-circular.png){width="128px"}

![](splatter-circular.resources/splatter-circular-color.png){width="128px"}

<b>Em:</b> Geradores De Textura > Padrões

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Splatter Circular gera um padrão baseado em anel com vários controles. Ele pode usar formas predefinidas ou entradas personalizadas. É semelhante a [Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md), mas com um posicionamento circular em vez de uma grade.

Isso é útil quando você deseja inserir formas de uma forma circular com várias opções de aleatoriedade.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

Ambas as entradas são opcionais.

|  |  |
|:---|:---|
| <b>Entrada de imagem de padrão 1-6</b> <i>Entrada em tons de cinza (entrada Colorida)</i> | Somente Splatter Circular: imagem de padrão personalizada, usada quando o parâmetro “Pattern” está definido como “Image Input”. |
| <b>Fundo</b> <i>Entrada em tons de cinza (entrada Colorida)</i> |  |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Valor do Padrão</b> <i>1 - 64</i> | Quantidade de blocos gráficos de padrão para colocar em um anel. |
| <b>Valor Aleatório do Padrão</b> <i>0.0 - 1.0</i> | Aleatoriedade da quantidade de padrões a serem colocados. Melhor usado com uma quantidade de anel maior que 1. |
| <b>Quantidade de padrão aleatória mínima</b> <i>1 - 10</i> | Define a quantidade mínima de padrões para aleatoriedade. |
| <b>Valor do Toque</b> <i>1 - 10</i> | Define o número de toques a preencher. Os anéis são sempre colocados dentro do externo, e o espaço é igual. |
| <b>Expansão não quadrada</b> <i>Falso/Verdadeiro</i> | Permite a compensação de esmagamento e alongamento com proporções não quadradas. |
| <b>Padrão</b> |  |
| <b>Padrão</b> <i>Entrada De Imagem, Quadrado, Disco, Parabolóide, Sino, Gaussiano, Espinho, Pirâmide, Tijolo, Gradação, Ondas, Meio sino, Sino Ondulado, Crescente, Cápsula, Cone</i> | Seleciona a forma de padrão a ser usada. |
| <b>Número de Entrada de Padrão</b> <i>1 - 6</i> | Define o número de entradas de Imagem diferentes a serem usadas. Disponível somente quando a <i>Entrada de imagem</i> está selecionada acima. |
| <b>Distribuição de Entrada de Padrão</b> <i>Aleatório, Por Número De Padrão, Por Número De Toque</i> | Define como várias Entradas de Padrão são escolhidas. Aleatório significa que um número aleatório foi escolhido, Número de padrão significa que eles foram colocados em uma sequência em loop. Por números de anel significa que cada anel tem um diferente na sequência. |
| <b>Filtragem de Entrada de Imagens</b> <i>Bilinear + Mipmaps, Bilinear, Mais Próximo</i> |  |
| <b>Específico de Padrão</b> <i>0.0 - 1.0</i> | Permite que você altere a forma do padrão selecionado. O efeito depende do padrão selecionado. |
| <b>Simetria aleatoriamente</b> <i>0.0 - 1.0</i> | Define o número de ladrilhos que devem ser invertidos/espelhados aleatoriamente, de acordo com o comportamento abaixo. |
| <b>Modo Aleatório de Simetria</b> <i>Horizontal + Vertical, Horizontal, Vertical</i> | Determina o comportamento de espelhamento da simetria. |
| <b>Posição</b> |  |
| <b>Raio</b> <i>0.0 - 1.0</i> | Define o raio a partir do centro no qual os padrões são colocados. |
| <b>Raio aleatório</b> <i>0.0 - 1.0</i> | Dispõe aleatoriamente o raio de cada bloco gráfico de padrão. |
| <b>Multiplicador de Raio de Anel</b> <i>0.0 - 1.0</i> | Afeta o espaçamento de vários anéis. |
| <b>Ângulo Aleatório</b> <i>0.0 - 1.0</i> | Aleatório o ângulo de cada padrão. Um montante mais elevado significa mais rotação. |
| <b>Fator de Espiral</b> <i>0.0 - 1.0</i> | Transforma os anéis em Espirais, onde cada ladrilho é colocado em um raio levemente crescente. |
| <b>Propagação</b> <i>0.0 - 2.0</i> | Define a quantidade de voltas que um anel faz. Isto pode ser aumentado além de seus limites. |
| <b>Deslocamento ao longo da direção</b> <i>0.0 - 1.0</i> | Move todos os padrões para fora do centro ao longo de seu ângulo. O efeito depende muito do Ângulo aleatório ou se parece apenas com um multiplicador do Raio. |
| <b>Deslocamento global</b> <i>0.0 - 1.0</i> | Converte toda a forma. |
| <b>Tamanho</b> |  |
| <b>Padrões de Conexão</b> <i>Falso/Verdadeiro</i> | Torna o comprimento dos blocos gráficos de padrão dependente do raio, o que significa que cada forma deve tocar na anterior e na próxima. |
| <b>Tamanho (Conectado)</b> <i>0.0 - 1.0</i> | Altera globalmente o tamanho de cada padrão. Quando conectado, é relativo ao raio total. |
| <b>Tamanho aleatório</b> <i>0.0 - 1.0</i> | Aleatório o tamanho de cada padrão individualmente. |
| <b>Escala</b> <i>0.0 - 2.0</i> | Dimensiona uniformemente cada padrão. |
| <b>Escala aleatória</b> <i>0.0 - 1.0</i> | Dispõe aleatoriamente o dimensionamento uniforme. |
| <b>Dimensionar por Número de Padrão</b> <i>0.0 - 1.0</i> | Torna a escala de padrão dependente da posição ao longo do anel. |
| <b>Inverter Número de Padrão</b> <i>Falso/Verdadeiro</i> | Usado com a opção anterior, pode inverter o dimensionamento de pequeno para grande e vice-versa. |
| <b>Dimensionar por Número de Toque</b> <i>0.0 - 1.0</i> | Torna a escala dependente do número do anel. |
| <b>Inverter Número de Toque</b> <i>Falso/Verdadeiro</i> | Usado com a opção anterior, pode inverter o dimensionamento de pequeno para grande e vice-versa. |
| <b>Rotação</b> |  |
| <b>Rotação de padrão</b> <i>0.0 - 1.0</i> | Gira todos os padrões uniformemente. |
| <b>Rotação de padrão aleatória</b> <i>0.0 - 1.0</i> | Dispõe aleatoriamente a rotação do padrão. |
| <b>Tabela Dinâmica de Rotação de Padrão</b> <i>Centro, Mín. X, Máx. X, Mín. Y, Máx. Y</i> | Define a posição do ponto de giro em torno da qual cada padrão será girado individualmente. |
| <b>Orientação Central</b> <i>Falso/Verdadeiro</i> | Gira todos os padrões para que fiquem voltados para o centro do anel. Desativá-la fornece a todos a mesma orientação, o que pode produzir efeitos indesejados com Deslocamento ao longo da direção. |
| <b>Rotação de Toque</b> <i>0.0 - 1.0</i> | Gira todo o anel ao redor do centro. |
| <b>Rotação Aleatória de Toque</b> <i>0.0 - 1.0</i> | Dispõe aleatoriamente a rotação por anel. |
| <b>Deslocamento da Rotação de Toque</b> <i>0.0 - 1.0</i> | Desloca a rotação por anel. |
| <b>Cor</b> |  |
| <b>Cor</b> <i>(Valor em tons de cinza)</i> | Cor para multiplicar com o padrão selecionado. |
| <b>Luminância aleatória</b> <i>0.0 - 1.0</i> | Dispõe aleatoriamente a cor ou a Luminância de cada bloco gráfico de padrão. |
| <b>Luminância por escala</b> <i>0.0 - 1.0</i> | Torna a luminância dependente da escala de padrão individual. |
| <b>Luminância por Número de Padrão</b> <i>0.0 - 1.0</i> | Torna a luminância dependente da sequência de padrão. Pode, por exemplo, ser usado com espirais. |
| <b>Inverter Número de Padrão</b> <i>Falso/Verdadeiro</i> | Inverte a opção anterior. |
| <b>Luminância por Número de Toque</b> <i>0.0 - 1.0</i> | Torna a luminância dependente da sequência de anéis. |
| <b>Inverter Número de Toque</b> <i>Falso/Verdadeiro</i> | Inverte a opção anterior. |
| <b>Máscara aleatória</b> <i>0.0 - 1.0</i> | Oculta padrões aleatoriamente. |
| <b>Cor do plano de fundo</b> <i>(Valor em tons de cinza)</i> | Altera a cor sólida do plano de fundo. |
| <b>Modo de Mesclagem</b> <i>Adicionar, Máx., Adicionar Sub</i> | Define como mesclar padrões sobrepostos. |
| <b>Opacidade Global</b> <i>0.0 - 1.0</i> | Define a opacidade global de todo o resultado. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="splatter-circular.resources/circularsplatter-ex.png" />
        </td>
    </tr>
</table>
