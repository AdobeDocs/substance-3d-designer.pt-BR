---
title: Cor do mapeador do respingo de forma v2
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Gerador > Padrão > Cor do mapeador Shape splatter v2
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1948'
ht-degree: 0%

---


# Cor do mapeador do respingo de forma v2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de cor do mapeador de respingo de forma v2](shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color.png "Cor do mapeador de respingo de forma v2")

<b>Entrada:</b> Gerador > Padrão

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Mapeia imagens coloridas em formas geradas e dispersas usando o nó [respingo de forma v2](../shape-splatter-v2/shape-splatter-v2.md), usando os dados adicionais fornecidos pelo nó.<br><br>As imagens são fornecidas como entradas de padrão separadas ou embaladas em uma grade de atlas e podem ser aplicadas às formas usando mapeamento UV, projeção triplanar ou mapeamento personalizado.<br><br>As formas podem ser coloridas e suas cores ajustadas de maneira uniforme ou aleatória por forma.

Consulte também [Escala de cinza do mapeador de respingo de forma v2](../shape-splatter-v2-mapper-grayscale/shape-splatter-v2-mapper-grayscale.md).

</td>
</tr>
</table>

>[!INFO]
>
> Este nó requer dados de entrada gerados pelo nó [respingo de forma v2](../shape-splatter-v2/shape-splatter-v2.md).
> 
> Outros nós na família Shape splatter v2:
> * [respingo de forma v2 para máscara](../shape-splatter-v2-to-mask/shape-splatter-v2-to-mask.md)
>
> Os nós [Cor de Grade de atlas](../grid-atlas-color/grid-atlas-color.md) permitem compactar imagens em um atlas de tamanho personalizado, com até 16 padrões em 4*4 células.

>[!TIP]
> 
> A [**&#39;Rusty bolts&#39;** amostra de material](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md#material-sample) está disponível para começar com os nós Shape splatter v2.
> 
> Para saber mais sobre conceitos e fluxos de trabalho que envolvem Funções SDF, acesse a página dedicada: [Trabalhando com Funções SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/working-with-sdf-functions.md)

<a name="inputs"></a>

## Entradas

|                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:--------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Entrada de Grade de atlas</b> *Cor* | Uma imagem colorida de padrões compactados em um layout de grade.<br><br>O tamanho da grade deve corresponder ao usado pelo nó do [respingo de forma v2](../shape-splatter-v2/shape-splatter-v2.md).<br><br>Use o nó [Cor de Grade de atlas](../grid-atlas-color/grid-atlas-color.md) para empacotar padrões separados em uma grade de atlas. |
| <b>Entrada de padrão 1</b> *Cor* | A imagem colorida do padrão #1 que é mapeada para as formas.<br><br><i>Dica:</i> use uma resolução que esteja próxima do tamanho máximo que o padrão pode ter quando disperso. |
| <b>Entrada de padrão 2</b> *Cor* | A imagem colorida do padrão #2 que é mapeada para as formas.<br><br><i>Dica:</i> use uma resolução que esteja próxima do tamanho máximo que o padrão pode ter quando disperso. |
| <b>Entrada de padrão 3</b> *Cor* | A imagem colorida do padrão #3 que é mapeada para as formas.<br><br><i>Dica:</i> use uma resolução que esteja próxima do tamanho máximo que o padrão pode ter quando disperso. |
| <b>Entrada de padrão 4</b> *Cor* | A imagem colorida do padrão #4 que é mapeada para as formas.<br><br><i>Dica:</i> use uma resolução que esteja próxima do tamanho máximo que o padrão pode ter quando disperso. |
| <b>Entrada de padrão 5</b> *Cor* | A imagem colorida do padrão #5 que é mapeada para as formas.<br><br><i>Dica:</i> use uma resolução que esteja próxima do tamanho máximo que o padrão pode ter quando disperso. |
| <b>Entrada de padrão 6</b> *Cor* | A imagem colorida do padrão #6 que é mapeada para as formas.<br><br><i>Dica:</i> use uma resolução que esteja próxima do tamanho máximo que o padrão pode ter quando disperso. |
| <b>Entrada de padrão 7</b> *Cor* | A imagem colorida do padrão #7 que é mapeada para as formas.<br><br><i>Dica:</i> use uma resolução que esteja próxima do tamanho máximo que o padrão pode ter quando disperso. |
| <b>Entrada de padrão 8</b> *Cor* | A imagem colorida do padrão #8 que é mapeada para as formas.<br><br><i>Dica:</i> use uma resolução que esteja próxima do tamanho máximo que o padrão pode ter quando disperso. |
| <b>Entrada em segundo plano</b> *Cor* | A imagem colorida usada como plano de fundo para as formas mapeadas. |
| <b>Entrada de cores</b> *Cor* | A imagem colorida usada para colorir as formas mapeadas de acordo com sua posição de pivô.<br><br>Use o parâmetro <b>Opacidade de entrada de cor</b> para ajustar a intensidade da contribuição dessas cores para a cor das formas. |
| <b>Normal</b> *Cor* | Os normais computados para as formas dispersas, mascaradas de acordo com a mesclagem com o height de plano de fundo.<br><br> Se o <b>tipo de forma</b> for &#39;Grade de atlas&#39;, os normais fornecidos para a entrada <b>normal de Grade de atlas</b> serão usados diretamente. |
| <b>Splatter UVW</b> *Cor* | <b>R</b> - Componente U dos UVs das formas.<br><b>G</b> - Componente V dos UVs das formas.<br><b>B</b> - height das formas. (W)<br><b>A</b> - Dados empacotados:<br> - <i>Parte inteira:</i> O identificador exclusivo das formas. (ID)<br> - <i>Parte fracionária:</i> depende do <b>tipo de forma</b>: ID de material se SDF/primitiva, ID de padrão* se entrada/grade de atlas de padrão.<br><br><b>*:</b> A ID de padrão é o índice da forma na lista/atlas. |
| <b>Dados de respingo 1</b> *Cor* | <b>R</b> - Componente X da posição na superfície da forma, no espaço de objeto.<br><b>G</b> - Componente Y da posição na superfície da forma, no espaço de objeto.<br><b>B</b> - Componente Z da posição na superfície da forma, no espaço de objeto.<br><b>A</b> - Dados empacotados:<br> - <i>Parte inteira:</i> um componente UV das coordenadas UV para os dados das formas nas saídas Data 2/3.<br> - <i>Parte fracionária:</i> componente V das coordenadas UV para os dados das formas nas saídas de Dados 2/3.<br> - <i>Assinar:</i> máscara binária para a mesclagem de formas com o height do plano de fundo. |
| <b>Dados de respingo 2</b> *Cor* | <b>R</b> - Componente X da rotação 3D das formas.<br><b>G</b> - Componente Y da rotação 3D das formas.<br><b>B</b> - Componente Z da rotação 3D das formas.<br><b>A</b> - A rotação das formas em torno de sua normal.<br><br>Todas as rotações são definidas em número de rotações. |
| <b>Dados de respingo 3</b> *Cor* | <b>R</b> - Componente X da posição das formas.<br><b>G</b> - Componente Y da posição das formas.<br><b>B</b> - Deslocamento das formas ao longo de seu normal.<br><b>A</b> - Dados empacotados:<br> - <i>Parte inteira:</i> ID da forma.<br> - <i>Parte fracionária:</i>O índice do padrão das formas em seu atlas de origem. (Se estiver usando um tipo de padrão de grade de atlas) |
| <b>Dados de respingo 4</b> *Cor* | <i>Pixel 1</i><br><b>R</b> - Tamanho X das imagens de saída dos Dados 2/3.<br><b>G</b> - Tamanho Y das imagens de saída dos Dados 2/3.<br><b>B</b> - Tamanho X da imagem de saída dos Dados 4.<br><b>A</b> - Tamanho Y da imagem de saída dos Dados 4.<br><br><i>Pixel 2</i><br><b>R</b> - O tipo de forma. (E.g. Cubo, cilindro, ...)<br><b>G</b> - Dados empacotados:<br> - <i>Valor absoluto:</i> O número de entrada do padrão.<br> - <i>Sinal:</i> Formato normal do mapa normal de saída. (Positivo: DirectX / Negativo: OpenGL)<br><b>B</b> - Tamanho X da grade de atlas. (Ou seja, a quantidade de colunas)<br><b>A</b> - Tamanho Y da grade de atlas. (Ou seja, o número de linhas) |

<a name="outputs"></a>

## Saídas

|               |                     |
|:--------------|:--------------------|
| <b>Saída</b> | As formas coloridas. |

<a name="parameters"></a>

## Parâmetros

|                                            |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:-------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Modo de projeção</b> *Inteiro* | O método de projetar as imagens de entrada nas formas:<br><br>- <b>De UVs de respingo:</b> use os UVs fornecidos pelo nó &#39;Shape splatter v2&#39;.<br>- <b>Triplanar:</b> use a projeção triplanar para mapear as imagens nos eixos XYZ locais das formas.<br>- <b>Função personalizada:</b> crie um gráfico de função para definir o mapeamento das imagens nas formas. |
| <b>Função personalizada</b> *Flutuante4* | Especifica a cor RGBA por pixel das formas como uma Precisão decimal 4.<br><br>As seguintes variáveis estão disponíveis:<br>- <code>shape.position.os</code> (Precisão decimal 3) A posição da superfície da forma no espaço de objeto.<br>- <code>shape.position.ws</code> (Precisão decimal 3) A posição da superfície da forma no espaço mundial*.<br>- <code>shape.normal.os</code> (Precisão decimal 3) Os normais da superfície da forma no espaço de objeto.<br> - <code>shape.normal.ws</code> (Precisão decimal 3) Os normais da superfície da forma no espaço mundial*.<br>- <code>shape.id</code> (Precisão decimal) O identificador exclusivo da forma.<br>- <code>material.id</code> (Precisão decimal) A ID de material da superfície da forma, definida pelo nó “Shape splatter v2”.<br><br>*: O espaço de mundo da forma está centralizado em sua tabela dinâmica e não leva em conta o height da forma. Isso significa que a única diferença com o espaço do objeto é a orientação.<br><br>Se a amostragem das entradas do nó &#39;Shape splatter v2 mapper color&#39; for necessária, estes <b>slots de entrada do nó </b> de cor de amostra podem ser usados:<br>- 0: Grade de atlas<br>- 1-8: Entrada de padrão 1-8 |
| <b>É mapa normal</b> *Booleano* | Especifica se as imagens fornecidas para a <b>entrada de Grade de atlas</b> ou a <b>entrada de padrão #</b> são mapas normais.<br><br>Isso é necessário para habilitar o processamento necessário para manipular corretamente os vetores normais e aplicá-los nas formas. |
| <b>Formato normal de entrada</b> *Inteiro* | O formato dos mapas normais fornecidos para a <b>entrada de Grade de atlas</b> ou a <b>entrada de padrão #</b>.<br><br>Inverte efetivamente o canal verde.<br><br>- <b>DirectX:</b> o eixo Y aponta para cima.<br>- <b>OpenGL:</b> O eixo Y aponta para baixo. |
| <b>Contraste de mesclagem</b> *Flutuante* | A nitidez das transições entre projeções planas, em que 1 significa que não há gradiente de fade. |
| <b>Projeção de imagem</b> *Inteiro* | A quantidade de imagens de entrada de <b>Padrão #</b> distribuídas pelas projeções planas que contribuem para o mapeamento triplanar.<br><br>Para cobrir todos os lados de uma forma, uma projeção planar frontal (+) e posterior (-) é executada em cada eixo, totalizando 6 projeções.<br><br>- <b>1 imagem:</b> A entrada Pattern 1 é usada para todas as projeções planares.<br>- <b>3 imagens:</b> Uma entrada Pattern separada é usada para a projeção +/- de cada eixo.<br>- <b>6 imagens:</b> Cada projeção usa uma entrada Pattern separada.<br>- <b>1 imagem por material ID:</b> Use uma entrada Pattern separada por ID de material, onde cada imagem é usada para todas as projeções planares. |
| <b>Centro de projeção</b> *Flutuante3* | Desloca a projeção triplanar por eixo, no espaço do objeto.<br><br>O deslocamento é aplicado a <i>todo o espaço de projeção</i>, portanto, um deslocamento em um eixo afetará o posicionamento das texturas projetadas nos <i>outros dois</i> eixos. |
| <b>Escala de projeção</b> *Flutuante* | Ajusta a escala das texturas projetadas em <i>todos os eixos</i>, de acordo com o fator especificado. |
| <b>Modo de seleção de entrada</b> *Inteiro* | O método de selecionar quais imagens de entrada devem ser mapeadas para as formas.<br><br>O <b>tipo de forma</b> selecionado no nó &#39;Shape splatter v2&#39; de origem altera a maneira de atribuir imagens a formas:<br><br>- <b>Grade de atlas</b> significa que as imagens são buscadas na &#39;entrada de Grade de atlas&#39; por índices de grade correspondentes (ambos os atlas devem usar o mesmo tamanho de grade)<br>- <b>Entrada de padrão</b> significa que as imagens são buscadas nas entradas &#39;Entrada de padrão #&#39; por índices correspondentes.<br>- <b>Outros tipos de forma:</b> imagens são atribuídas por meio da correspondência dos índices com os índices IDs de material da forma.<br><br>Os métodos disponíveis de seleção dos índices são:<br>- <b>Dos dados de respingo:</b> Corresponda os índices das imagens &#39;Entrada de padrão #&#39; ou &#39;Entrada de Grade de atlas&#39; aos índices das formas atribuídas pelo nó &#39;Espingo de forma v2&#39;.<br>- <b>Manual:</b> Use o índice especificado pelo parâmetro &#39;Índice de imagem&#39;.<br>- <b>Aleatório:</b> Use um índice aleatório intervalo especificado pelo parâmetro &#39;Random range&#39;. |
| <b>Número de entrada padrão</b> *Inteiro* | A quantidade de imagens de entrada <b>Padrão #</b> que devem ser mapeadas nas formas. |
| <b>Índice de imagem</b> *Inteiro* | O índice do padrão de entrada da <b>Entrada de padrão #</b> ou da <b>Entrada de Grade de atlas</b> que deve ser mapeada nas formas. |
| <b>Intervalo aleatório</b> *Inteiro2* | O intervalo de índices da <b>Entrada de padrão #</b> ou da <b>entrada de Grade de atlas</b> em que o padrão deve ser selecionado aleatoriamente para ser mapeado nas formas. |
| <b>Ajuste de HSL</b> *Precisão decimal 3* | Um deslocamento aplicado uniformemente à matiz, à saturação e à luminância (HSL) de todas as formas. |
| <b>HSL aleatório</b> *Precisão decimal 3* | Um deslocamento aleatório positivo ou negativo aplicado à matiz, saturação e luminância (HSL) das formas, até os valores especificados. |
| <b>Opacidade da entrada de cores</b> *Precisão decimal* | A intensidade da contribuição da <b>entrada de cores</b> para as cores das formas, de acordo com o <b>modo de mesclagem de entrada de cores</b> selecionado. |
| <b>Modo de mesclagem de entrada de cores</b> *Inteiro* | A operação de mesclagem de cores usada para combinar as imagens de primeiro plano e plano de fundo.<br><br>Essas operações são idênticas às suas contrapartes no nó <b>Combinar</b>.<br><br>Modos disponíveis:<br>- <b>Copiar</b><br>- <b>Adicionar (subexposição linear)</b><br>- <b>Subtrair</b><br>- <b>Multiplicar</b><br>- <b>Sobreposição</b> |
| <b>Ângulo normal aleatório</b> *Precisão decimal* | Um vetor de direção é gerado a partir da origem do vetor normal para um ponto aleatório na base de um cone em torno do vetor normal, em seguida, o vetor normal é misturado com esse vetor de direção aleatório.<br><br>Este parâmetro ajusta o <i>ângulo do cone</i>, onde 1 é um hemisfério e 0 significa que o vetor de direção é igual ao vetor normal. |
| <b>Modo lado a lado</b> *Inteiro* | Os eixos ao longo dos quais a textura deve ser repetida:<br> - <b>Sem divisão em blocos gráficos</b><br> - <b>Lado a lado horizontal</b><br> - <b>Lado a lado vertical</b><br> - <b>Lado a lado H e V</b>: divisão em blocos gráficos horizontal e vertical combinada. |
| <b>divisão em blocos gráficos UV</b> *Precisão decimal* | Ajusta a divisão em blocos gráficos global das imagens mapeadas nas formas<br><br>Valores mais altos resultam em mais repetições. |
| <b>Escala UV</b> *Precisão decimal 2* | Ajusta a divisão em blocos gráficos das imagens mapeadas nas formas pelo fator especificado, com controles separados para escala em U e V. Valores mais altos resultam em mais repetições. |
| <b>Deslocamento UV</b> *Precisão decimal 2* | Aplica um deslocamento ao mapeamento de imagens entre as formas, o que permite um ajuste fino do posicionamento das imagens nas formas.<br><br>Este deslocamento é adicionado ao <b>Deslocamento aleatório</b>, se houver. |
| <b>Deslocamento aleatório</b> *Precisão decimal* | Aplica uma quantidade aleatória de deslocamento positivo ou negativo <i>por forma</i> ao mapeamento de imagens pelas formas até o valor especificado.<br><br>Este deslocamento é adicionado ao <b>Deslocamento UV</b>, se houver. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px; border: none">
    <tr style="border: 0; background: transparent">
        <td style="width: 33%; border: 0; background: transparent">
            <img src="./shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color-triplanar-02.gif" /><br><i>Mapeamento triplanar</i>
        </td>
        <td style="width: 33%; border: 0; background: transparent">
            <img src="./shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color-normal.gif" /><br><i>Mapeamento normal</i>
        </td>
        <td style="width: 33%; border: 0; background: transparent">
            <img src="./shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color-matID-02.jpg" /><br><i>Mapeamento por ID de material de formas SDF</i>
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="width: 33%; border: 0; background: transparent">
            <img src="./shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color-tiling.gif" /><br><i>Ajuste de divisão em blocos com mapeamento triplanar</i>
        </td>
        <td style="width: 33%; border: 0; background: transparent">
            <img src="./shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color-matID-01.jpg" /><br><i>Mapeamento por ID de material da forma do cilindro</i>
        </td>
        <td style="width: 33%; border: 0; background: transparent">
            <img src="./shape-splatter-v2-mapper-color.resources/shape-splatter-v2-mapper-color-graph.png" /><br><i>Nó no contexto de um gráfico</i>” /&gt;
        </td>
    </tr>
</table>

