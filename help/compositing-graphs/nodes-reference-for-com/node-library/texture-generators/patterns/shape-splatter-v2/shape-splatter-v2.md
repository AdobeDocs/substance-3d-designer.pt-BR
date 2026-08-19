---
title: respingo de forma v2
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Gerador > Padrão > respingo de forma v2
source-git-commit: f688c618b01d3ca8059e67cf0797268e44e94b17
workflow-type: tm+mt
source-wordcount: '4234'
ht-degree: 0%

---


# respingo de forma v2

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de respingo de forma v2](shape-splatter-v2.resources/shape-splatter-v2.png "respingo de forma v2")

<b>Entrada:</b> Gerador > Padrão

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Dispersão formas em uma superfície de height de plano de fundo com recursos avançados de dispersão em um <b>espaço 3D</b> virtual, com controles para posição, rotação, escala e aleatoriedade.<br><br>O nó oferece formas 3D primitivas básicas e oferece suporte a formas personalizadas fornecidas como uma <b>imagem de padrão</b>, um <b>atlas</b> ou como uma função de <b>campo de distância assinado (SDF)</b> para formas 3D personalizadas complexas.<br><br>Vários <b>métodos de distribuição de formas</b> estão disponíveis, incluindo a criação de uma função personalizada para controle completo.<br><br>As formas podem ser puxadas para áreas específicas usando um <b>mapa de densidade</b> personalizado.<br><br><i>Observação:</i> este nó não deve ser usado com as versões de CPU do mecanismo de Substance, por exemplo, SSE2 (Windows, Linux) e NEON (macOS).

</td>
</tr>
</table>

>[!INFO]
>
> Os dados gerados por este nó podem ser usados com os outros nós na família Shape splatter v2:
> * [Cor do mapeador do respingo de forma v2](../shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.md)
> * [Escala de cinza do mapeador de respingo de forma v2](../shape-splatter-v2-mapper-grayscale/shape-splatter-v2-mapper-grayscale.md)
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

|                                      |                                                                                                                                                                                                                                                                                                                                                                  |
|:-------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>height de fundo</b> *Tons de cinza* | O mapa de height base no qual as formas são dispersas. Os heights de cada um são combinados usando uma “Mesclagem máxima”, onde o mais alto dos dois é usado.<br><br>A contribuição do height de plano de fundo para o height de saída é controlada pelo parâmetro <b>Opacidade de entrada do plano de fundo</b>. |
| <b>Mapa de densidade</b> *Tons de cinza* | Um mapa em tons de cinza que direciona o deslocamento de formas de acordo com sua luminância, no qual as formas se reúnem em suas áreas mais brilhantes.<br><br>A intensidade do deslocamento de formas é controlada pelo parâmetro <b>multiplicador de Mapa de densidade</b>. |
| <b>Deslocamento de Height</b> *Tons de cinza* | Um mapa em tons de cinza cujos valores são adicionados às formas de maneira uniforme, de acordo com o local de tabela dinâmica das formas.<br><br>A contribuição do mapa é controlada pelo parâmetro <b>multiplicador de mapa de deslocamento de Height</b>. |
| <b>Mapa de escala de Height</b> *Tons de cinza* | Um mapa em tons de cinza cujos valores são usados como fator para o height das formas.<br><br>A contribuição do mapa é controlada pelo parâmetro <b>multiplicador de mapa de escala de Height</b>. |
| <b>Mapa de escala da forma</b> *Tons de cinza* | Um mapa em tons de cinza cujos valores são usados como um fator para a escala das formas.<br><br>A contribuição do mapa é controlada pelo parâmetro <b>Multiplicador de mapa de escala</b>. |
| <b>Rotação de forma</b> *Tons de cinza* | Um mapa em tons de cinza com valores adicionados à rotação 3D de formas, ajustado pelos fatores por eixo fornecidos pelo <b>multiplicador de mapa de rotação 3D</b>. |
| <b>Mapa vetorial</b> *Cor* | Um mapa que descreve os vetores de direção que podem ser usados para orientar a rotação e/ou posição das formas, usando os seguintes parâmetros:<br><br>- <b>deslocamento de mapa vetorial</b> ajusta o efeito do mapa para mover as formas.<br>- <b>A entrada de rotação de Inclinação</b> pode ser definida como &#39;Mapa vetorial&#39; para usar este mapa para girar as formas usando os parâmetros relacionados. |
| <b>Mapa de máscaras</b> *Tons de cinza* | A imagem usada para mascarar formas de acordo com o <b>Limite de mapa de máscara</b>.<br><br>Ou seja, as formas localizadas em áreas do mapa onde a luminância está abaixo desse limite serão mascaradas. |
| <b>Entrada de padrão 1</b> *Tons de cinza* | O mapa de heights do padrão #1 que está disperso quando <b>Tipo de padrão</b> está definido como &#39;Entrada de padrão&#39;.<br><br><i>Dica:</i> use uma resolução próxima ao tamanho máximo que o padrão pode ter quando disperso. |
| <b>Entrada de padrão 2</b> *Tons de cinza* | O mapa de heights do padrão #2 que está disperso quando <b>Tipo de padrão</b> está definido como &#39;Entrada de padrão&#39;.<br><br><i>Dica:</i> use uma resolução próxima ao tamanho máximo que o padrão pode ter quando disperso. |
| <b>Entrada de padrão 3</b> *Tons de cinza* | O mapa de heights do padrão #3 que está disperso quando <b>Tipo de padrão</b> está definido como &#39;Entrada de padrão&#39;.<br><br><i>Dica:</i> use uma resolução próxima ao tamanho máximo que o padrão pode ter quando disperso. |
| <b>Entrada de padrão 4</b> *Tons de cinza* | O mapa de heights do padrão #4 que está disperso quando <b>Tipo de padrão</b> está definido como &#39;Entrada de padrão&#39;.<br><br><i>Dica:</i> use uma resolução próxima ao tamanho máximo que o padrão pode ter quando disperso. |
| <b>Entrada de padrão 5</b> *Tons de cinza* | O mapa de heights do padrão #5 que está disperso quando <b>Tipo de padrão</b> está definido como &#39;Entrada de padrão&#39;.<br><br><i>Dica:</i> use uma resolução próxima ao tamanho máximo que o padrão pode ter quando disperso. |
| <b>Entrada de padrão 6</b> *Tons de cinza* | O mapa de heights do padrão #6 que está disperso quando <b>Tipo de padrão</b> está definido como &#39;Entrada de padrão&#39;.<br><br><i>Dica:</i> use uma resolução próxima ao tamanho máximo que o padrão pode ter quando disperso. |
| <b>Entrada de padrão 7</b> *Tons de cinza* | O mapa de heights do padrão #7 que está disperso quando <b>Tipo de padrão</b> está definido como &#39;Entrada de padrão&#39;.<br><br><i>Dica:</i> use uma resolução próxima ao tamanho máximo que o padrão pode ter quando disperso. |
| <b>Entrada de padrão 8</b> *Tons de cinza* | O mapa de heights do padrão #8 que está disperso quando <b>Tipo de padrão</b> está definido como &#39;Entrada de padrão&#39;.<br><br><i>Dica:</i> use uma resolução próxima ao tamanho máximo que o padrão pode ter quando disperso. |
| <b>height DE Grade de atlas</b> *Tons de cinza* | A imagem que descreve o height de padrões empacotados em um atlas.<br><br>Use o parâmetro <b>tamanho da Grade de atlas</b> para especificar o tamanho da grade do atlas. |
| <b>Grade de atlas normal</b> *Cor* | A imagem que descreve os normais de padrões empacotados em um atlas.<br><br>Use o parâmetro <b>tamanho da Grade de atlas</b> para especificar o tamanho da grade do atlas. |

<a name="outputs"></a>

## Saídas

|                        |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Height</b> | O mapa de heights calculado para as formas dispersas, incluindo o height de plano de fundo, se usado e visível. |
| <b>Cor do SDF</b> | As cores da forma produzidas pela <b>Função SDF</b>.<br><br>Use o nó <a href="../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/sdf-functions-material/set-color/set-color.md">Definir cor</a> no gráfico de Função SDF para definir uma cor por componente da forma. |
| <b>Metalidade do SDF</b> | As cores da forma produzidas pela <b>Função SDF</b>.<br><br>Use o nó <a href="../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/sdf-functions-material/set-metalness/set-metalness.md">Definir metalidade</a> no gráfico de Função SDF para definir um valor de metalidade por componente da forma. |
| <b>Aspereza do SDF</b> | As cores da forma produzidas pela <b>Função SDF</b>.<br><br>Use o nó <a href="../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-sdf-functions/sdf-functions-material/set-roughness/set-roughness.md">Definir aspereza</a> no gráfico de Função SDF para definir um valor de aspereza por componente da forma. |
| <b>Normal</b> | Os normais computados para as formas dispersas, mascaradas de acordo com a mesclagem com o height de plano de fundo.<br><br> Se o <b>tipo de forma</b> for &#39;Grade de atlas&#39;, os normais fornecidos para a entrada <b>normal de Grade de atlas</b> serão usados diretamente. |
| <b>Splatter UVW</b> | <b>R</b> - Componente U dos UVs das formas.<br><b>G</b> - Componente V dos UVs das formas.<br><b>B</b> - height das formas. (W)<br><b>A</b> - Dados empacotados:<br> - <i>Parte inteira:</i> O identificador exclusivo das formas. (ID)<br> - <i>Parte fracionária:</i> depende do <b>tipo de forma</b>: ID de material se SDF/primitiva, ID de padrão* se entrada/grade de atlas de padrão.<br><br><b>*:</b> A ID de padrão é o índice da forma na lista/atlas. |
| <b>Dados de respingo 1</b> | <b>R</b> - Componente X da posição na superfície da forma, no espaço de objeto.<br><b>G</b> - Componente Y da posição na superfície da forma, no espaço de objeto.<br><b>B</b> - Componente Z da posição na superfície da forma, no espaço de objeto.<br><b>A</b> - Dados empacotados:<br> - <i>Parte inteira:</i> um componente UV das coordenadas UV para os dados das formas nas saídas Data 2/3.<br> - <i>Parte fracionária:</i> componente V das coordenadas UV para os dados das formas nas saídas de Dados 2/3.<br> - <i>Assinar:</i> máscara binária para a mesclagem de formas com o height do plano de fundo. |
| <b>Dados de respingo 2</b> | <b>R</b> - Componente X da rotação 3D das formas.<br><b>G</b> - Componente Y da rotação 3D das formas.<br><b>B</b> - Componente Z da rotação 3D das formas.<br><b>A</b> - A rotação das formas em torno de sua normal.<br><br>Todas as rotações são definidas em número de rotações. |
| <b>Dados de respingo 3</b> | <b>R</b> - Componente X da posição das formas.<br><b>G</b> - Componente Y da posição das formas.<br><b>B</b> - Deslocamento das formas ao longo de seu normal.<br><b>A</b> - Dados empacotados:<br> - <i>Parte inteira:</i> O identificador exclusivo da forma.<br> - <i>Parte fracionária:</i>O índice do padrão das formas em seu atlas de origem. (Se estiver usando um tipo de padrão de grade de atlas) |
| <b>Dados de respingo 4</b> | <i>Pixel 1</i><br><b>R</b> - Tamanho X das imagens de saída dos Dados 2/3.<br><b>G</b> - Tamanho Y das imagens de saída dos Dados 2/3.<br><b>B</b> - Tamanho X da imagem de saída dos Dados 4.<br><b>A</b> - Tamanho Y da imagem de saída dos Dados 4.<br><br><i>Pixel 2</i><br><b>R</b> - O tipo de forma. (E.g. Cubo, cilindro, ...)<br><b>G</b> - Dados empacotados:<br> - <i>Valor absoluto:</i> O número de entrada do padrão.<br> - <i>Sinal:</i> Formato normal do mapa normal de saída. (Positivo: DirectX / Negativo: OpenGL)<br><b>B</b> - Tamanho X da grade de atlas. (Ou seja, a quantidade de colunas)<br><b>A</b> - Tamanho Y da grade de atlas. (Ou seja, o número de linhas) |

<a name="parameters"></a>

## Parâmetros

|                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Modo de distribuição da posição</b> *Inteiro* | O método de distribuição de formas no espaço:<br><br>- <b>Grade 2D:</b> Uma grade uniforme simples.<br>- <b>Disco Poisson:</b> Uma simulação destinada a deslocar aleatoriamente as células de uma grade para evitar sobreposições, fazendo uso do espaço disponível.<br>- <b>Uniforme:</b> Uma distribuição uniforme de um número especificado de formas. Requer cálculos mais intensivos.<br>- <b>Função personalizada:</b> crie um gráfico de função para definir a distribuição de formas. As variáveis disponíveis são listadas na descrição do nó. |
| <b>Função de posição</b> *Flutuante2* | O gráfico de função usado para definir a distribuição de formas.<br><br>O gráfico gera um valor Float2 para a posição normalizada XY das formas na imagem.<br><br>Variáveis disponíveis:<br> - <code>shape.id</code> (Flutuante) O identificador exclusivo da forma.<br> - <code>shape.amount</code> (Flutuante) A quantidade de formas especificadas pelo parâmetro <b>Quantidade</b>. |
| <b>Valor de X</b> *Inteiro* | A quantidade de colunas na grade de distribuição.<br><br>Ou seja, a quantidade de formas geradas no eixo X. |
| <b>Valor Y</b> *Inteiro* | A quantidade de linhas na grade de distribuição.<br><br>Ou seja, a quantidade de formas geradas no eixo Y. |
| <b>Valor</b> *Inteiro* | A quantidade de formas geradas. |
| <b>Formato normal de saída</b> *Inteiro* | O formato do mapa normal de saída.<br><br>Inverte efetivamente o canal verde.<br><br>- <b>DirectX:</b> o eixo Y aponta para cima.<br>- <b>OpenGL:</b> O eixo Y aponta para baixo. |
| <b>Expansão não quadrada</b> *Booleano* | Em imagens não quadradas, preserva a taxa de formas e expande sua geração para os limites da imagem. |
| <b>Tipo de forma</b> *Inteiro* | Há vários tipos de formas disponíveis para serem dispersas, cada uma oferecendo características específicas.<br><br>A <b>Função SDF</b> é um gráfico de função que gera um campo de distância assinado (SDF) que descreve a superfície de uma forma 3D. Isso permite a dispersão 3D de formas processuais complexas que podem variar dinamicamente.<br><br><b>Formas primitivas</b>, computadas usando funções simples de interseção de raio/superfície, estão prontas para uso: cubo, esfera, cilindro, plano, disco<br><br><b>Os padrões de entrada</b> são imagens fornecidas pelo gráfico. Eles são mapeados para planos e podem ser <i>extrusados</i> em formas 3D:<br> - Entrada de imagem: o(s) padrão(ões) conectado(s) aos pinos de entrada <b>Entrada de padrão #</b>.<br> - Grade de atlas: os padrões empacotados em uma imagem atlas conectada às entradas de <b>Grade de atlas</b>. |
| <b>Tamanho da Grade de atlas</b> *Inteiro2* | A quantidade de linhas e colunas do atlas fornecido para as entradas da imagem de <b>Grade de atlas</b>.<br><br><i>Observação:</i> células vazias no atlas resultarão em lacunas na distribuição da forma. |
| <b>Recalcular grade de atlas normal</b> *Booleano* | Quando <i>Verdadeiro</i>, o mapa normal fornecido para a entrada de imagem <b>normal de Grade de atlas</b> é ignorado e os normais para os padrões fornecidos para o <b>height de Grade de atlas</b> são computados do zero.<br><br>Quando <i>Falso</i>, o mapa normal fornecido para a <b>Grade de atlas normal</b> é usado como está.<br><br><i>Observação:</i> a intensidade dos normais é ajustada de acordo com o <b>height de extrusão de forma</b>. |
| <b>Grade de atlas formato normal</b> *Inteiro* | O formato do mapa normal fornecido para a entrada de imagem <b>normal de Grade de atlas</b>.<br><br>Inverte efetivamente o canal verde.<br><br>- <b>DirectX:</b> o eixo Y aponta para cima.<br>- <b>OpenGL:</b> O eixo Y aponta para baixo. |
| <b>Número de entrada padrão</b> *Inteiro* | A quantidade de padrões fornecidos como imagens de entrada.<br><br>Adiciona quantos pinos de entrada de <b>Padrão #</b> ao nó. |
| <b>Habilitar extrusão de forma</b> *Booleano* | Alterna a extrusão de padrões de entrada, interpretando-os como mapas de height, o que resulta em formas 3D de procedimento complexas. |
| <b>Simetria de extrusão de forma</b> *Booleano* | Permite a extrusão simétrica para frente/para trás dos padrões de entrada.<br><br>O eixo de simetria é o <i>ponto intermediário</i> da extrusão, o que significa que sua localização pode mudar de acordo com a posição de pivô das formas. |
| <b>height de extrusão de forma</b> *Flutuante* | A distância máxima de extrusão no espaço da imagem, onde 1 é o lado mais longo da imagem.<br><br>Esta distância é dimensionada em relação ao valor de <b>escala da forma</b>. |
| <b>Amostras de extrusão de forma</b> *Inteiro* | A quantidade de amostras executadas para desenhar a extrusão dos padrões de entrada.<br><br>Uma quantidade maior resulta em extrusões mais suaves e mais definidas, o que prejudica algum desempenho. |
| <b>Função de padrão</b> *Flutuante* | O gráfico de função Substance criado usado para calcular o padrão mapeado para um SDF de plano 3D.<br><br>Esses padrões também podem ser extrusados usando <b>Habilitar extrusão de forma</b>. |
| <b>Função SDF de padrões</b> *Flutuante* | O gráfico de função Substance que cria o campo de distância assinada (SDF) que descreve a superfície de um objeto 3D no espaço.<br><br>Procure a coleção interna de [Funções SDF](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions) na Biblioteca para criar um objeto complexo combinando várias <i>primitivas</i> de SDF usando os <i>operadores</i> e as <i>transformações</i> disponíveis.<br><br>Uma forma SDF é inteiramente processual e pode ser ajustada dinamicamente, o que pode permitir que cada forma dispersa seja <i>única</i>.<br><br>Use o nó [visualizador 3D](../../../filters/effects/3d-viewer/3d-viewer.md) para visualizar o resultado de uma Função SDF.<br><br><i>Observação:</i> para aplicar aleatoriedade no Função SDF, use os nós [Hash](../../../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#random) em vez de &#39;Aleatório&#39;. |
| <b>Tamanho de quadro delimitador do SDF</b> *Flutuante3* | Define o tamanho máximo da caixa delimitadora (Bbox) da forma SDF, que por sua vez é usada para calcular sua Caixa 2D.<br><br>As formas são desenhadas somente dentro dos limites de sua Caixa 2D e o restante é aparado. |
| <b>Habilitar recorte de arestas</b> *Booleano* | Alterna a aparagem de padrões, o que ignora todos os valores abaixo do <b>Limite de recorte</b>. Isso garante que apenas a silhueta desejada dos padrões seja usada. |
| <b>Limite de recorte</b> *Flutuante* | O valor de tons de cinza abaixo do qual os valores nos padrões são aparados. Ou seja, o valor usado como borda da silhueta para os padrões. |
| <b>Fluxo de trabalho normalizado</b> *Booleano* | Quando ativado, habilita o ajuste automático do height das formas para que elas <i>preservem suas proporções originais</i> conforme são dimensionadas para cima ou para baixo.<br><br>Quando desativado, o height das formas é expresso na faixa de heights completa da imagem, independentemente de suas proporções originais.<br><br>O height das formas ainda pode ser ajustado manualmente usando os parâmetros de <b>escala de Height</b>. |
| <b>A escala da forma afeta a escala do height</b> *Booleano* | Quando <i>Verdadeiro</i>, a escala de height de uma forma é ajustada à medida que sua escala muda para preservar suas proporções.<br><br>Quando <i>Falso</i>, a escala do height é independente da escala da forma, o que resulta em deformação. |
| <b>Escala de Height</b> *Flutuante* | Um multiplicador para o height da forma, onde 1 é o height completo da forma expresso no intervalo de heights completo da imagem do intervalo de heights normalizado da forma. (Consulte <b>Fluxo de trabalho normalizado</b>) |
| <b>Escala aleatória do Height</b> *Flutuante* | Reduz aleatoriamente o height de cada forma até a proporção especificada, onde 1 significa que o height de uma forma pode ser totalmente reduzido a 0. |
| <b>Multiplicador de mapa de escala de Height</b> *Flutuante* | A intensidade do <b>mapa de escala de Height</b> fornecido, onde 1 significa que o valor do mapa completo é multiplicado em relação ao height da forma. |
| <b>Opacidade da entrada do plano de fundo</b> *Flutuante* | A intensidade da entrada fornecida do <b>height de Plano de Fundo</b> no mapa de height final.<br><br>Os heights das formas e do plano de fundo são combinados usando uma “Mesclagem máxima”, em que o mais alto dos dois é usado. |
| <b>Deslocamento de Height do plano de fundo</b> *Flutuante* | A proporção do height de plano de fundo que deve ser adicionado ao height das formas, onde 1 significa que o height de plano de fundo completo foi adicionado.<br><br>Isso pode ser usado para fazer com que as formas “descansem” no height de plano de fundo. |
| <b>Conformidade com o plano de fundo</b> *Flutuante* | A intensidade da deformação aplicada ao height das formas para corresponder ao height do plano de fundo por pixel, onde 1 significa uma correspondência exata.<br><br><i>Observação:</i> este parâmetro não tem efeito quando o <b>deslocamento do Height do plano de fundo</b> = 0. |
| <b>Suavizar inclinação do plano de fundo</b> *Flutuante* | A intensidade da suavização aplicada ao height de plano de fundo usado para os ajustes de <b>Deslocamento do Height do plano de fundo</b> e <b>Conformidade com o plano de fundo</b>.<br><br>Isso suaviza as frequências de deformação e deslocamento de height, que podem ser mais duras do que o desejado. |
| <b>Deslocamento de Height</b> *Flutuante* | Um valor adicionado ao height das formas, resultando em um deslocamento reto.<br><br>O valor é expresso no intervalo de height completo da imagem. |
| <b>Deslocamento aleatório do Height</b> *Flutuante* | Aplica um deslocamento aleatório ao height das formas, até o valor especificado.<br><br>O valor é expresso no intervalo de height completo da imagem. |
| <b>Deslocamento de Height da ID</b> *Flutuante* | O deslocamento aplicado ao height das formas de acordo com seu índice na distribuição, onde o deslocamento aumenta linearmente de uma forma para a seguinte até o valor especificado.<br><br>O valor pode ser definido manualmente além de <code>[0, 1]</code> intervalo. |
| <b>Multiplicador de mapa de deslocamento de Height</b> *Flutuante* | Ajusta a intensidade do deslocamento aplicado pelo <b>mapa de deslocamento de Height</b> usando o fator especificado, onde 1 significa que os valores de intensidade do mapa são aplicados como estão.<br><br>O height inteiro da forma é deslocado pela adição do valor no mapa de deslocamento em seu local de tabela dinâmica XY.<br><br>O valor do multiplicador pode ser definido manualmente além de <code>[0, 1]</code> intervalo. |
| <b>Modo de tamanho</b> *Inteiro* | O método de definição do tamanho das formas dispersas:<br><br>- <b>Automático:</b> o tamanho é expresso como um fator do tamanho da célula da forma.<br>- <b>Absoluto (espaço de textura):</b> o tamanho é expresso como um fator do lado mais longo da imagem. |
| <b>Manter proporção de tamanho</b> *Booleano* | Ajusta o tamanho das formas para preservar suas proporções originais em grades e tamanhos de imagem não quadrados. |
| <b>Escala da forma</b> *Flutuante* | O tamanho da forma como um fator definido pelo <b>Modo de tamanho</b>.<br><br><i>Observação:</i> ao usar a distribuição do <b>Disco Poisson</b>, ajustar o tamanho das formas resulta em sua movimentação para aproveitar o espaço disponível. Use o parâmetro <b>Poisson</b> da escala de forma para dimensionar as formas no local. |
| <b>Escala aleatória da forma</b> *Flutuante* | Reduz as formas aleatoriamente até o valor especificado, em que 1 pode resultar na redução completa de algumas formas até o tamanho zero. |
| <b>Multiplicador de mapa de escala</b> *Flutuante* | A intensidade da multiplicação dos valores no <b>mapa de escala de forma</b> pelo tamanho das formas. |
| <b>Poisson da postagem da escala de forma</b> *Flutuante* | Um fator de dimensionamento aplicado após a simulação do disco Poisson. |
| <b>Tamanho da forma</b> *Flutuante3* | Separe os fatores de escala por eixo para ajustar o tamanho das formas. |
| <b>Tamanho aleatório da forma</b> *Flutuante3* | Reduz as formas aleatoriamente a um fator de <i>por eixo</i> até o valor especificado, onde 1 pode resultar na redução de algumas formas até o tamanho zero. |
| <b>Raio do cilindro</b> *Flutuante* | Raio dos FDS do cilindro espalhado. O raio é expresso como um fator definido pelo <b>Modo de tamanho</b>. |
| <b>Tamanho da forma</b> *Flutuante2* | Separe os fatores de escala por eixo para ajustar o tamanho das formas. |
| <b>Tamanho aleatório da forma</b> *Flutuante2* | Reduz as formas aleatoriamente a um fator de <i>por eixo</i> até o valor especificado, onde 1 pode resultar na redução de algumas formas até o tamanho zero. |
| <b>Posição aleatória</b> *Flutuante* | Aplica um deslocamento aleatório nos eixos XY até o valor especificado, onde 1 é o comprimento do lado mais longo da imagem. |
| <b>Posicionar multiplicador aleatório</b> *Flutuante2* | Fatores separados por eixo para o deslocamento aleatório aplicado às formas nos eixos XY. |
| <b>Sequência de distribuição de posição</b> *Inteiro* | O algoritmo usado para distribuir as formas uniformemente no espaço. <br><br>- <b>R2</b>: com base na proporção áurea. É rápido e oferece distribuições mais uniformes e aparentemente aleatórias, independentemente da quantidade de formas.<br>- <b>Halton</b>: baseado em números primos. Ele fornece ótimos resultados para distribuições esparsas, mas fica mais lento e pode resultar em linhas visíveis à medida que a quantidade de formas aumenta.<br><br>Esses algoritmos são conhecidos como <i>quasirandom</i> e <i>baixa discrepância</i>, pois seguem uma sequência determinística (quasirandom) destinada a cobrir um espaço uniformemente (baixa discrepância). |
| <b>Multiplicador de Mapa de densidade</b> *Flutuante* | Um fator para o deslocamento aplicado às formas para que elas sejam reunidas nas áreas mais claras do <b>Mapa de densidade</b>. |
| <b>Deslocamento ao longo do normal</b> *Flutuante* | Desloca as formas ao longo do eixo Z normal, ou seja, no local. |
| <b>Deslocamento ao longo do aleatório normal</b> *Flutuante* | Adiciona uma quantidade aleatória de deslocamento às formas ao longo de sua normal.<br><br>O valor aleatório pode ser positivo ou negativo até o valor especificado ou até seu negativo. |
| <b>deslocamento de mapa vetorial</b> *Flutuante* | Um fator para o deslocamento aplicado às formas ao adicionar os valores de RGB no <b>Mapa vetorial</b> às coordenadas XYZ da forma, respectivamente.<br><br>O deslocamento é expresso como um fator do lado mais longo da imagem.<br>Por exemplo. um valor de RGB (0,5, 0,5, 0) desloca as formas pela metade de seu tamanho ao longo dos eixos X e Y.<br><br>Um valor de parâmetro de 1,0 significa que o valor completo foi adicionado. |
| <b>Multiplicador de deslocamento vetorial</b> *Flutuante3* | Ajusta o <b>deslocamento de mapa vetorial</b> por um fator separado por eixo, onde 0,0 significa que nenhum deslocamento é aplicado nesse eixo. |
| <b>Deslocamento global</b> *Flutuante2* | Um deslocamento aplicado à posição de cada forma <i>depois</i> de aplicar qualquer deslocamento de height, deslocamentos aleatórios e outros deslocamentos.<br><br>Isso significa que mover as formas usando este parâmetro não modificará sua posição, orientação e escala. |
| <b>Deslocamento da posição da linha</b> *Flutuante* | Um deslocamento aplicado às linhas de formas na grade de acordo com o <b>modo de deslocamento de posição de linha.</b> |
| <b>Modo de deslocamento da posição da linha</b> *Inteiro* | O método de aplicar o <b>Deslocamento da posição da linha</b> às formas.<br><br>Os métodos <b>Todos</b> aplicam o deslocamento como um fator do lado mais longo da imagem (isto é, no espaço de textura).<br>- <b>Todos - Horizontal:</b> adiciona gradualmente o valor de deslocamento horizontalmente linha por linha, por um fator do índice de linha.<br>- <b>Todos - Vertical:</b> adiciona gradualmente o valor de deslocamento verticalmente coluna por coluna, por um fator do índice de coluna.<br><br>Os métodos <b>Quincunx</b> aplicam o deslocamento como um fator do tamanho de célula das formas.<br>- <b>Quincunx - Horizontal:</b> Adiciona o valor de deslocamento uniformemente em todas as outras linhas.<br>- <b>Quincunx - Vertical:</b> Adiciona o valor de deslocamento uniformemente em todas as outras colunas. |
| <b>Posição de pivô (local)</b> *Flutuante3* | Ajusta a posição da tabela dinâmica no espaço local da forma, o que afeta a origem das transformações. (Por exemplo, deslocamento de posição, rotação e dimensionamento)<br><br>Por exemplo, ajuste a posição de pivô Z para que as formas girem em torno de sua base. |
| <b>Rotação 3D</b> *Flutuante3* | Aplica uma rotação por eixo uniformemente a todas as formas, em número de voltas. |
| <b>Rotação 3D aleatória</b> *Flutuante* | Um fator de rotação aleatória aplicado às formas até o valor especificado, no sentido horário ou anti-horário, em número de voltas. |
| <b>Multiplicador aleatório de rotação 3D</b> *Flutuante3* | Ajusta a quantidade de rotação aleatória aplicada pela <b>rotação 3D aleatória</b> por um fator separado por eixo. |
| <b>Multiplicador de mapa de rotação 3D</b> *Flutuante3* | A intensidade com que os valores no mapa de <b>Rotação de forma</b> são adicionados à rotação por eixo de cada forma, onde 1 significa que a quantidade total de rotação é adicionada. |
| <b>Rotação em torno do normal</b> *Flutuante* | A quantidade de rotação aplicada uniformemente a todas as formas ao redor de seu eixo Z local em número de voltas. |
| <b>Rotação ao redor do aleatório normal</b> *Flutuante* | Aplica uma rotação aleatória em cada forma ao redor de sua forma normal, ou seja, seu eixo Z local, no sentido horário ou anti-horário, até uma volta completa. |
| <b>Rotação de Inclinação</b> *Flutuante* | Gira as formas para corresponder à inclinação do plano de fundo em seu local.<br>Ou seja, aplica uma rotação igual à do vetor Z-up global ao normal do height de plano de fundo.<br><br>Este parâmetro é um fator para esta rotação, onde 1 significa que a rotação completa é aplicada.<br><br>Esta rotação é adicionada a outras rotações que podem ser aplicadas às formas. |
| <b>Entrada de rotação de Inclinação</b> *Inteiro* | A origem da inclinação usada para orientar a <b>rotação da Inclinação</b>.<br><br>- <b>Fundo:</b> a textura do height de Plano de Fundo é usada, o normal calculado fora desse mapa de height é a direção de destino da rotação.<br>- <b>Mapa de vetor:</b> Os vetores especificados pela textura do mapa de Vetor são usados como estão para a direção de destino da rotação.</b> |
| <b>Multiplicador de mapa vetorial</b> *Flutuante* | Gira as formas ao redor do eixo especificado pelo <b>Eixo de rotação do mapa vetorial</b> para corresponder à direção dos vetores descritos pela textura do <b>Mapa vetorial</b>.<br>Ou seja, aplica uma rotação igual à do vetor X-right global aos vetores na textura.<br><br>Este parâmetro é um fator para esta rotação, onde 1 significa que a rotação completa é aplicada.<br><br>Esta rotação é adicionada a outras rotações que podem ser aplicadas às formas. |
| <b>Eixo de rotação do mapa vetorial</b> *Inteiro* | O eixo ao redor do qual a rotação especificada pelo <b>Mapa de vetor</b> deve ser executada.<br><br>- <b>Normal:</b> Gira as formas ao redor de seu normal, de forma semelhante ao uso do parâmetro &#39;Rotação ao redor do normal&#39;.<br>- <b>Eixo Z:</b> Gira as formas ao redor do eixo Z global, de forma semelhante ao uso do componente Z do parâmetro &#39;Rotação 3D&#39;. |
| <b>Máscara aleatória</b> *Flutuante* | Oculta a proporção especificada da quantidade total de formas em uma sequência aleatória, onde 1 significa que todas as formas estão ocultas.<br><br>Este parâmetro é combinado com o Mapa de máscaras. (Se usado) |
| <b>Limite do mapa de máscaras</b> *Flutuante* | O valor em tons de cinza no <b>Mapa de máscaras</b> abaixo do qual as formas estão ocultas.<br><br>O mapa é combinado com o parâmetro <b>Máscara aleatória</b>. |
| <b>Escala UV</b> *Flutuante2* | Um multiplicador por eixo para os UVs das formas, em que a divisão em blocos gráficos aumenta com os valores. |
| <b>Escala UV de arremate</b> *Flutuante2* | Um multiplicador por eixo para os UVs das tampas do cilindro, onde a divisão em blocos gráficos aumenta com os valores. |
| <b>Modo Cap UV</b> *Inteiro* | O método de calcular os UVs para as tampas do cilindro.<br><br>- <b>Polar:</b> Use coordenadas polares onde U aumenta ao redor do eixo Z do cilindro e V aumenta à medida que ele se afasta dele.<br>- <b>Planar:</b> Use uma projeção planar onde os UVs são mapeados usando a caixa delimitadora das tampas (isto é, um retângulo ajustado para o tamanho das tampas) |
| <b>Mostrar caixa 2D de forma</b> *Booleano* | Sobrepõe uma visualização do retângulo delimitador da forma na imagem. Esta é a área na qual as formas são desenhadas. |
| <b>Mostrar caixa 3D de formas</b> *Booleano* | Sobrepõe uma visualização do volume delimitador da forma no espaço 3D. Essa é a área na qual as formas SDF e os planos de extrusão são desenhados.<br><br>Para formas SDF, esta área corresponde ao <b>tamanho de quadro delimitador SDF</b>.<br><br>Esta visualização ajuda a avaliar a extensão e a orientação da forma. |
| <b>Mostrar tabela dinâmica da forma</b> *Booleano* | Sobrepõe a visualização da tabela dinâmica de formas, como uma combinação dos vetores locais do eixo XYZ.<br><br>Esta visualização ajuda a avaliar a orientação da forma, bem como a origem de suas transformações. (Ou seja, deslocamento, rotação, escala) |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-3d-distribution-poisson.gif" /><br><i>Distribuição Poisson</i>
        </td>
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-3d-distribution-uniform.gif" /><br><i>Distribuição uniforme</i>
        </td>
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-density-map.gif" /><br><i>Mapa de densidade</i>
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-3d-rotation.gif" /><br><i>Rotação 3D aleatória</i>
        </td>
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-background-slope.gif" /><br><i>Rotação de Inclinação</i>
        </td>
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-shape-extrusion.gif" /><br><i>Extrusão de forma</i>
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="./shape-splatter-v2.resources/shape-splatter-v2-sdf.jpg" /><br><i>Formas 3D SDF</i>
        </td>
        <td style="border: 0; background: transparent">
        </td>
        <td style="border: 0; background: transparent">
        </td>
    </tr>
</table>

