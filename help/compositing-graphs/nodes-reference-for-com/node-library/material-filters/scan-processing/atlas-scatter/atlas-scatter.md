---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-scatter.html"
breadcrumb-title: ''
description: Use o nó Atlas scatter para dispersão texturas em um atlas a fim de criar padrões lado a lado a partir de materiais digitalizados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Scatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas scatter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 7%

---


# Atlas scatter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](atlas-scatter.resources/atlas-scatter-01.png){width="200px"}

<b>Entrada:</b> Filtros Materiais > Processamento de materiais escaneados

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Extraia elementos de um Atlas e dispersão-os em um plano de fundo. As entradas Atlas são materiais completos, constituídos por elementos individuais dispostos e embalados em uma única folha de textura. Este nó os divide (usando um processo interno de [Atlas splitter](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/atlas-splitter/atlas-splitter.md)) e os dispersão, semelhante a [Divisória de Forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md). O atlas scatter requer no mínimo uma entrada do mapa de Opacidade e uma entrada do mapa de Altura para o Atlas funcionar.

</td>
</tr>
</table>

>[!NOTE]
>
> Centenas de [Atlas](https://source.substance3d.com/allassets?assetType=substanceAtlas), prontos para uso no nó do Atlas scatter, estão disponíveis em [Substance Source](https://source.substance3d.com/).

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Resolução da Entrada Atlas</b> <i>Resolução, 1 a 12</i> | Defina manualmente a resolução do atlas de entrada completo para garantir um bom desempenho versus uma taxa de qualidade. |
| <b>Valor X</b> <i>1 - 64</i> | Quantidade de repetições X do padrão. |
| <b>Valor Y</b> <i>1 - 64</i> | Quantidade de repetições Y do padrão. |
| <b>Padrão</b> |  |
| <b>Intervalo de padrões</b> <i>0 - 10</i> | Define o intervalo de padrões a serem dispersos. Se definido como 0, todos os padrões serão usados. |
| <b>Modo de Distribuição de Padrão</b> <i>Aleatório, Índice de Padrão, Índice de Linha, Índice de Coluna</i> | Define a ordem na qual os elementos atlas são usados. |
| <b>Multiplicador de Mapa de Distribuição de Padrões</b> <i>0.0 - 1.0</i> | Selecione o padrão de forma em função do valor de tons de cinza da imagem de entrada. |
| <b>Rotação de padrão</b> <i>0, 90, 180, 270</i> | Aplica uma rotação fixa a cada elemento do atlas, de acordo com a quantidade selecionada de graus. |
| <b>Rotação de padrão aleatória</b> <i>0.0 - 1.0</i> | Aplica uma rotação aleatória à parte definida dos elementos do atlas. |
| <b>Precisão de Detecção de Forma do Atlas</b> <i>Formas simples ou pequenas, Formas complexas ou grandes, Modo sem falha</i> | Define a precisão com que as formas são detectadas. Quanto maior a precisão, maior o impacto no desempenho. |
| <b>Reduzir a Opacidade do Atlas (detecção mais rápida)</b> <i>-4 - 0</i> | Permite controlar a taxa de redução do mapa de opacidade do atlas de entrada, usado para detecção de formas. Uma resolução mais baixa melhora o desempenho às custas da precisão. |
| <b>Ignorar Forma Menor Que</b> <i>0.0 - 1.0</i> | Define o tamanho mínimo que uma forma deve ser detectada, expresso como a proporção da imagem geral |
| <b>Tamanho</b> |  |
| <b>Escala</b> <i>0.0 - 5.0</i> | Define a escala relativa de formas dispersas. |
| <b>Escala aleatória</b> <i>0.0 - 1.0</i> | Define o multiplicador para aplicar o dimensionamento aleatório a cada forma dispersa. |
| <b>Escala sem sobreposição</b> <i>0.0 - 1.0</i> | Reduz a escala da forma para que ela não se sobreponha. |
| <b>Multiplicador de Mapa de Escala</b> <i>0.0 - 1.0</i> | Multiplica a escala da forma em função do valor de tons de cinza da imagem de entrada. |
| <b>Tamanho</b> <i>0.0 - 1.0</i> | Define a escala relativa de formas dispersas por comprimento (X) e largura (Y). |
| <b>Proporção de Tamanho da Inclinação de Erro</b> <i>0.0 - 1.0</i> | Modifica a taxa de tamanho da forma em função da inclinação do height de plano de fundo. |
| <b>Preservar Proporções</b> <i>0.0 - 1.0</i> | Determina por qual intensidade as proporções originais das formas dispersas devem ser preservadas, em vez de usar a proporção de células da grade, por exemplo, a proporção dos valores de Intensidade X e Intensidade Y. |
| <b>Posição</b> |  |
| <b>Posição Aleatória</b> <i>0.0 - 2.0</i> | Um multiplicador para mover cada forma em uma direção aleatória a partir do ponto de partida da grade. |
| <b>Distribuição Aleatória</b> <i>Gaussiano, Uniforme</i> | Alterna de uma distribuição Gaussiana para uma Distribuição Uniforme para a posição aleatória. A distribuição gaussiana produzirá um resultado mais orgânico comparado com a distribuição uniforme. |
| <b>Multiplicador de Mapa Vetorial</b> <i>0.0 - 1.0</i> | Controla a influência da entrada do mapa de vetor para mover as formas na direção do vetor especificado pelos canais vermelho (X) e verde (Y) do mapa. |
| <b>Deslocamento horizontal</b> <i>-2.0 - 2.0</i> | Um multiplicador para deslocamento de posição ao longo do eixo X. |
| <b>Deslocamento vertical</b> <i>-2.0 - 2.0</i> | Um multiplicador para deslocamento de posição ao longo do eixo Y. |
| <b>Opção Fora dos Limites</b> <i>Dimensionar Forma, Restringir Posição</i> | Devido à natureza técnica do respingo, as formas não podem ser desenhadas a mais de 2 células de tamanho de distância de sua posição original. Se uma forma ficar muito grande ou for movida para longe demais, você terá duas opções: - Dimensionar forma reduzirá o tamanho da forma quando ela atingir um limite - Restringir posição moverá a forma de volta à sua posição original |
| <b>Rotação</b> |  |
| <b>Rotação</b> <i>0.0 - 1.0</i> | Permite controlar a rotação local de todas as formas. |
| <b>Rotação aleatória</b> <i>0.0 - 1.0</i> | Um multiplicador para uma quantidade aleatória de rotação aplicada por forma. |
| <b>Rotação da Inclinação de erros</b> <i>0.0 - 1.0</i> | Modifica a rotação da forma em função da inclinação do height de plano de fundo. Normalmente usado em combinação com o parâmetro “Size Ratio from Bg Inclinação” |
| <b>Multiplicador de Mapa de rotação</b> <i>0.0 - 1.0</i> | Multiplica a rotação da forma em função do valor da imagem de entrada em tons de cinza. |
| <b>Multiplicador de Mapa Vetorial</b> <i>0.0 - 1.0</i> | Define a rotação da forma em função da entrada da imagem vetorial. |
| <b>Height</b> |  |
| <b>Ajuste Automático De Escala De Height</b> <i>Falso/Verdadeiro</i> | Ajuste automaticamente o height em função da escala de padrão para manter o height da forma proporcional ao height do plano de fundo. |
| <b>Modo de Mesclagem</b> <i>Combinar de Height, Alpha Teste</i> | Define o método para resolver sobreposições de formas. |
| <b>Deslocamento de Height</b> <i>-1.0 - 1.0</i> | Aplica um deslocamento global ao height de formas |
| <b>Deslocamento de Height Aleatório</b> <i>0.0 - 1.0</i> | Um multiplicador para um deslocamento de height aleatório aplicado por forma |
| <b>Multiplicador de Mapa de Deslocamento de Height</b> <i>0.0 - 1.0</i> | Multiplica o deslocamento do height de forma em função do valor de tons de cinza da imagem de entrada. |
| <b>Escala de Height</b> <i>0.0 - 1.0</i> | Permite controlar a escala de height global das formas dispersas |
| <b>Escala de Height aleatória</b> <i>0.0 - 1.0</i> | Um multiplicador para uma escala de height aleatória aplicada por forma |
| <b>Multiplicador de Mapa de Escala de Height</b> <i>0.0 - 1.0</i> | Multiplica a escala do height de forma em função do valor da imagem de entrada em tons de cinza. |
| <b>Conformidade com o plano de fundo</b> <i>0.0 - 1.0</i> | Em 0, o height da forma permanece intacto; em 1, o height da forma será deformado pelo plano de fundo subjacente do height. |
| <b>Plano de fundo suave</b> <i>0.0 - 2.0</i> | Permite controlar a quantidade de suavização aplicada à deformação do height da forma quando ela está em conformidade com seu plano de fundo. |
| <b>Inclinar da Inclinação de erros</b> <i>0.0 - 1.0</i> | Deforma o height da forma em função da inclinação do height do plano de fundo local: um gradiente linear correspondente à inclinação do plano de fundo é adicionado ao height da forma. |
| <b>Smoothness de Inclinação em segundo plano</b> <i>0.0 - 2.0</i> | Controla a quantidade de suavização aplicada à inclinação de plano de fundo quando a forma é inclinada com base nessa inclinação. |
| <b>Recortar pixels pretos</b> <i>Falso/Verdadeiro</i> | Ignora o valor preto das entradas de padrão. |
| <b>Achatar base de padrão</b> <i>Falso/Verdadeiro</i> | Permite nivelar a height do plano de fundo sob uma forma para que corresponda à height inicial. |
| <b>Mascaramento</b> |  |
| <b>Máscara aleatória</b> <i>0.0 - 1.0</i> | Mascara uma quantidade aleatória de formas, expressa como uma proporção da quantidade total. |
| <b>Multiplicador de Mapa Aleatório de Máscara</b> <i>0.0 - 1.0</i> | Define o mascaramento de forma aleatório em função da entrada da imagem em tons de cinza. |
| <b>Mascarar da Inclinação de erros</b> <i>-1.0 - 1.0</i> | Controla o mascaramento das formas com base na inclinação do plano de fundo em seu local. |
| <b>Cor</b> |  |
| <b>Ajuste de cor</b> <i>-1.0 - 1.0</i> | Permite ajustar as cores dos elementos dispersos globalmente. |
| <b>Cores aleatórias</b> <i>0.0 - 1.0</i> | Um multiplicador para mudar os valores das cores por uma quantidade aleatória por forma. |
| <b>Cor do plano de fundo</b> <i>0.0 - 1.0</i> | Muda as cores da forma para a cor do plano de fundo em seu local. |
| <b>Normal</b> |  |
| <b>Inclinar da Inclinação de erros</b> <i>0.0 - 1.0</i> | Inclinar a forma normal de acordo com a normal de fundo. |
| <b>Aleatório Normal</b> <i>0.0 - 1.0</i> | Um multiplicador para inclinar a forma normal em uma quantidade aleatória por forma. |
| <b>Formato Normal</b> <i>DirectX, OpenGL</i> | Alternar entre Formatos de mapa normais diferentes (inverte o canal verde) |
| <b>Aspereza</b> |  |
| <b>Ajuste de aspereza</b> <i>-1.0 - 1.0</i> | Permite que você desloque a aspereza da forma global. |
| <b>Aspereza de plano de fundo</b> <i>0.0 - 1.0</i> | Move a aspereza da forma para a aspereza do plano de fundo em sua localização. |
| <b>Aspereza aleatória</b> <i>0.0 - 1.0</i> | Um multiplicador para compensar a aspereza por uma quantidade aleatória por forma. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="atlas-scatter.resources/atlas-scatter-02.png" />
        </td>
    </tr>
</table>
