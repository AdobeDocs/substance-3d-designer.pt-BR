---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/scatter-on-spline-grayscale.html"
breadcrumb-title: ''
description: Use o nó Dispersão na spline de tons de cinza para distribuir elementos de tons de cinza nos caminhos da spline para obter padrões processuais.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Scatter on Spline Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dispersão em Tons de Cinza Spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '2853'
ht-degree: 0%

---


# Dispersão em Tons de Cinza Spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](scatter-on-spline-grayscale.resources/scatter-on-spline-grayscale-icon.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Desenha o(s) padrão(ões) especificado(s) ao longo das linhas de entrada sobre o plano de fundo de entrada.

</td>
</tr>
</table>

O nó oferece profundas opções de personalização para controlar como os padrões são dispersos.

Alguns aspectos da dispersão podem ser controlados usando imagens de outros nós no gráfico para promover o aspecto dinâmico do resultado.

>[!NOTE]
>
> Consulte também [Dispersão na cor da spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-on-spline-color/scatter-on-spline-color.md).

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Fundo</b> <i>Tons de cinza</i> (Primário) | A imagem em tons de cinza sobre a qual as splines devem ser desenhadas. |
| <b>Cordas de spline</b> <i>Cor</i> | As coordenadas dos pontos das linhas divisórias de entrada codificadas nos canais RGBA de uma imagem colorida:<br><b>R</b> - Posição X<br><b>G</b> - Posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br>- Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> <i>Cor</i> | Dados adicionais das splines de entrada codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usadas<br><b>A</b> - Não Usadas |
| <b>Valor da spline</b> <i>Inteiro</i> | O número de splines de entrada. |
| <b>Entrada de padrão #</b> <i>Tons de cinza</i> | O(s) padrão(ões) que devem ser espalhados ao longo dos splines. |
| <b>Mapa de Escala</b> <i>Tons de cinza</i> | O mapa que controla a escala dos padrões dispersos. O efeito desse mapa é controlado pelo parâmetro &#39;Multiplicador de Entrada de Mapa de Escala&#39; e é combinado com outros parâmetros no grupo &#39;Tamanho&#39;. |
| <b>Mapa de Heights</b> <i>Tons de cinza</i> | O mapa que controla o height dos padrões dispersos. O efeito desse mapa é controlado pelo parâmetro &#39;Multiplicador de entrada de Height&#39; e é combinado com outros parâmetros &#39;Cor&#39; no grupo &#39;Cor&#39;. |
| <b>Mapa de máscaras</b> <i>Tons de cinza</i> | O mapa que controla o mascaramento dos padrões dispersos. O efeito desse mapa é controlado pelo parâmetro &#39;Limite de mapa de máscara&#39; e é combinado com outros parâmetros &#39;Máscara&#39; no grupo &#39;Cor&#39;. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Saída</b> <i>Tons de cinza</i> | A imagem que representa o(s) padrão(ões) espalhado(s) ao longo da(s) spline(s) de entrada sobre o plano de fundo de entrada. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Entrada de spline</b> <i>Inteiro</i> | O método de selecionar quais splines devem ser usados para padrões de dispersão:<br><br>- <i>Todas as splines</i>: use todas as splines na lista de entrada;<br>- <i>Única Spline</i>: use somente a spline especificada na lista de entrada;<br>- <i>Intervalo de Spline</i>: use somente as splines no intervalo especificado da lista de entrada. |
| <b>Índice de Spline</b> <i>Inteiro</i> (Disponível quando &#39;Entrada Spline&#39; está definido como &#39;Spline Simples&#39;) | O índice de lista da spline que deve ser usado para padrões de dispersão. |
| <b>Intervalo de spline</b> <i>Inteiro2</i> (Disponível quando &#39;Entrada Spline&#39; estiver definido como &#39;Intervalo Spline&#39;) | O intervalo de índices de lista, incluindo as splines, que deve ser usado para padrões de dispersão. |
| <b>Modo de Dispersão</b> <i>Inteiro</i> | O método de dispersão dos padrões nas linhas divisórias, que afeta a quantidade de padrões em cada linha divisória:<br><br>- Quantidade de forma: a quantidade especificada de padrões com espaçamento uniforme é dispersa;<br>- Espaçamento entre formas: o número de padrões é ajustado automaticamente para se ajustar ao espaçamento uniforme especificado.<br><br>Em ambos os casos, o primeiro e o último padrões caem exatamente no início e no final de cada spline, respectivamente. |
| <b>Quantidade de forma</b> <i>Inteiro</i> (Disponível quando o &#39;Modo de Dispersão&#39; estiver definido como &#39;Quantidade de forma&#39;) | A quantidade de padrões com espaçamento uniforme espalhados ao longo de cada spline. |
| <b>Distribuição De Formas Ao Longo Da Spline</b> <i>Inteiro</i> (Disponível quando o &#39;Modo de Dispersão&#39; estiver definido como &#39;Quantidade de forma&#39;) | O método de distribuição dos padrões ao longo de uma spline:<br><br>- <i>Da Origem</i>: o espaçamento dos padrões é influenciado pelas tangentes do ponto de spline, onde as formas estão mais distantes perto de pontos com tangentes longas;<br>- <i>Uniformes</i>: os padrões são espaçados uniformemente ao longo da spline, independentemente de suas tangentes e trajetória. |
| <b>Espaçamento entre formas</b> <i>Precisão decimal</i> (Disponível quando o &#39;Modo de Dispersão&#39; estiver definido como &#39;Espaçamento de forma&#39;) | A distância mínima ao longo de uma spline pela qual os padrões devem ser espaçados, enquanto ainda aterrissam o primeiro e o último padrão no início e no final de cada spline, respectivamente. |
| <b>Iniciar</b> <i>Flutuante</i> | <span id="_Hlk135680521"></span>Desloca o ponto do início de uma spline onde a dispersão começa. O valor é o comprimento normalizado de cada spline. |
| <b>Fim</b> <i>Flutuante</i> | Desloca o ponto a partir do início de uma spline onde a dispersão termina. O valor é o comprimento normalizado de cada spline. |
| <b>Tabela Dinâmica de Formas</b> <i>Flutuante2</i> | Desloca a tabela dinâmica do padrão X e Y no espaço tangente da spline.<br>Considerando que a tabela dinâmica é o que é colocado na spline, isso desloca efetivamente os padrões ao longo ou perpendicularmente à spline.<br>Observação: as posições das tabelas dinâmicas afetam o efeito dos parâmetros &#39;Escala&#39; e &#39;Rotação (Tabela Dinâmica)&#39;. |
| <b>Padrão</b> |  |
| <b>Padrão</b> <i>Inteiro</i> | O padrão que deve ser espalhado ao longo das splines:<br><br>- <i>Entrada de Padrão</i>: Use os padrões fornecidos para as entradas &#39;Entrada de Padrão #&#39;;<br>- Quadrado;<br>- Disco;<br>- Parabolóide;<br>- Sino;<br>- Gaussiano;<br>- Espinho;<br>- Pirâmide;<br>- Tijolo;<br>- Gradação;<br>- Ondas;<br>- Meio sino;<br>- Cúpulo Sino;<br>- Crescente;<br>- Cápsula;<br>- Cone;<br>- Gradação w. offset;<br>- Hemisfério. |
| <b>Número de Entrada de Padrão</b> <i>Inteiro</i> (Disponível quando &#39;Padrão&#39; está definido como &#39;Entrada de Padrão&#39;) | Seleciona o índice do padrão de entrada que deve ser disperso. |
| <b>Distribuição de Entrada de Padrão</b> <i>Inteiro</i> (Disponível quando &#39;Padrão&#39; está definido como &#39;Entrada de Padrão&#39;) | O método usado para selecionar quais dos padrões de entrada devem ser espalhados em uma determinada spline:<br><br>- <i>Aleatório</i>: um padrão é selecionado aleatoriamente;<br>- <i>Ao longo da spline</i>: o índice de padrão aumenta gradualmente ao longo da spline;<br>- <i>Índice de padrão</i>: repete o índice de padrões de entrada ao longo de cada spline;<br>- <i>Índice de Spline</i>: repete o índice de padrões de entrada de uma spline para a próxima na lista de splines de entrada. |
| <b>Tremulação de Distribuição</b> <i>Precisão decimal</i> (Disponível quando &#39;Distribuição de Entrada de Padrão&#39; estiver definido como &#39;Na Curva&#39;) | Aumenta ou diminui aleatoriamente o índice selecionado de padrões na spline. |
| <b>Substituir o primeiro padrão</b> <i>Booleano</i> | Selecione manualmente o índice do padrão que deve ser colocado no início de cada spline. |
| <b>Primeiro Índice de Entrada de Padrão</b> <i>Inteiro</i> (Disponível quando &#39;Substituir primeiro padrão&#39; estiver definido como &#39;Verdadeiro&#39;) | O índice do padrão que deve ser colocado no início de cada spline. |
| <b>Substituir último padrão</b> <i>Booleano</i> | Selecione manualmente o índice do padrão que deve ser colocado no final de cada spline. |
| <b>Último Índice de Entrada de Padrão</b> <i>Inteiro</i> (Disponível quando &#39;Substituir último padrão&#39; estiver definido como &#39;Verdadeiro&#39;) | O índice do padrão que deve ser colocado no final de cada spline. |
| <b>Duplicatas</b> |  |
| <b>Modo de Distribuição</b> <i>Inteiro</i> | O método usado para colocar os padrões duplicados:<br><br>- <i>Linear</i>: duplicatas são espaçadas uniformemente ao longo do normal da spline a partir do local original do padrão;<br>- <i>Circular</i>: duplicadas são organizadas ao longo de um círculo virtual centralizado na spline no local original do padrão. |
| <b>Valor Duplicado</b> <i>Inteiro</i> | O número de padrões duplicados. |
| <b>Deslocamento</b> <i>Precisão decimal 2</i> (Disponível quando o &#39;Modo de Distribuição&#39; está definido como &#39;Linear&#39;) | Aplica um deslocamento às posições das duplicatas ao longo da tangente (paralela) e do normal (perpendicular) da spline.<br>As duplicatas em lados opostos da spline são movidas em direções opostas. |
| <b>Centro de Deslocamento</b> <i>Precisão decimal 2</i> (Disponível quando o &#39;Modo de Distribuição&#39; está definido como &#39;Linear&#39;) | Aplica um deslocamento às duplicatas ao longo da spline em X (paralelo) e Y (perpendicular). |
| <b>Ângulo de Propagação</b> <i>Precisão decimal</i> (Disponível quando o &#39;Modo de Distribuição&#39; está definido como &#39;Circular&#39;) | O arco do círculo virtual ao longo do qual as duplicatas são distribuídas, como o ângulo desse arco onde 1 é o círculo completo. |
| <b>Distância de deslocamento</b> <i>Precisão decimal</i> (Disponível quando o &#39;Modo de Distribuição&#39; está definido como &#39;Circular&#39;) | O raio do círculo virtual ao longo do qual as duplicatas são distribuídas. |
| <b>Rotação</b> <i>Flutuante</i> | Gira o círculo virtual ao longo do qual as duplicatas são distribuídas. |
| <b>Atenuação De Início/Término De Deslocamento</b> <i>Flutuante2</i> | Avalia a distância do ponto médio da spline até seu início e fim ao aplicar deslocamentos a duplicatas.<br>Isso significa que os deslocamentos são diminuídos para duplicatas mais próximas aos extremos de uma spline. |
| <b>Atenuação de deslocamento por Thickness</b> <i>Flutuante</i> | Fatores no thickness da spline ao aplicar deslocamentos a duplicatas.<br>Isso significa que os deslocamentos são reduzidos para duplicatas em uma parte de uma spline com um thickness inferior. |
| <b>Tamanho</b> |  |
| <b>Modo de Tamanho</b> <i>Inteiro</i> | O método de definição do tamanho dos padrões dispersos:<br><br>- <i>Normal</i>: o tamanho é controlado uniformemente usando um parâmetro &#39;Scale&#39; global;<br>- <i>Usar Thickness da spline</i>: o tamanho é controlado pelo thickness da spline. |
| <b>O Thickness Afeta</b> <i>Inteiro</i> (Disponível quando &#39;Modo de Tamanho&#39; estiver definido como &#39;Usar Thickness da Spline&#39;) | Especifica qual eixo da escala de um padrão deve ser orientado pelo thickness da spline:<br><br>- X &amp; Y: o Thickness é multiplicado em relação ao tamanho nos eixos X e Y;<br>- <span id="_Hlk135741125"></span>X: o Thickness é multiplicado em relação ao tamanho somente no eixo X;<br>- Y: o Thickness é multiplicado em relação ao tamanho somente no eixo Y.<br><br>Quando não multiplicada, a escala original do padrão é toda a extensão da imagem.<br>Isso significa que, no modo &#39;X&#39;, o tamanho no eixo Y é a extensão completa da imagem e precisa ser ajustado usando o parâmetro Size. O mesmo se aplica ao tamanho no eixo X ao usar o modo &#39;Y&#39;. |
| <b>Tamanho</b> <i>Flutuante2</i> | O tamanho original dos padrões em X e Y antes que outros ajustes sejam feitos por outros parâmetros. |
| <b>Tamanho aleatório</b> <i>Flutuante2</i> | Aplica um multiplicador aleatório até o valor especificado para reduzir o tamanho dos padrões em X e Y. |
| <b>Escala de Thickness</b> <i>Precisão decimal</i> (Disponível quando &#39;Modo de Tamanho&#39; estiver definido como &#39;Usar Thickness da Spline&#39;) | Um multiplicador adicional para a escala dos padrões quando acionado pelo thickness da spline. |
| <b>Escala</b> <i>Precisão decimal</i> (Disponível quando &#39;Modo de Tamanho&#39; estiver definido como &#39;Normal&#39;) | Um controle global para o tamanho de todos os padrões, onde 1 é a extensão completa da imagem.<br>O dimensionamento é aplicado relativamente à tabela dinâmica de um padrão. A posição de pivô pode ser deslocada usando o parâmetro &#39;Shape Pivot&#39;. |
| <b>Escala aleatória</b> <i>Flutuante</i> | Aplica um multiplicador aleatório até o valor especificado para diminuir o tamanho dos padrões. |
| <b>Multiplicador de Entrada de Mapa de Escala</b> <i>Flutuante</i> | Controla a intensidade da entrada do Mapa de Escala. Esse mapa atua como um multiplicador para o tamanho atual dos padrões.<br>O efeito deste mapa é combinado com outros parâmetros no grupo &#39;Tamanho&#39;. |
| <b>Modo de Amostragem de Entrada de Escala</b> <i>Espaço de Textura</i> | O método de mapear os valores no Mapa de Escala para os splines:<br><br>- <i>espaço de Textura</i>: os valores são aplicados aos splines nos quais estariam se fossem colocados em uma textura usando as coordenadas UV da textura. Isso aplica efetivamente o valor às linhas de spline &#39;no local&#39;;<br>- <i>Horizontal ao longo da linha de spline</i>: os valores são aplicados diretamente às coordenadas das linhas de spline codificadas (consulte entrada de Palavras de spline), onde cada linha é aplicada a uma linha de spline diferente de cima para baixo;<br>- <i>Hor. ao longo do spline (rand. deslocamento X)</i>: os valores são aplicados diretamente às coordenadas das splines codificadas (consulte a entrada de Coords de spline), com um deslocamento horizontal aleatório no mapa de Escala para cada spline (ou seja, cada linha nas Coords de Spline);<br>- <i>Hora. ao longo do spline (rand. deslocamento Y)</i>: os valores são aplicados diretamente às coordenadas das splines codificadas (consulte entrada de Coords de spline), com um deslocamento vertical aleatório no mapa de Escala para cada spline (ou seja, cada linha nas Coords de spline). |
| <b>Atenuação de Início/Término</b> <i>Flutuante2</i> | Afeta a distância do ponto médio da spline até seu início e fim ao dimensionar os padrões.<br>Isso significa que o tamanho é reduzido para padrões mais próximos aos extremos de uma spline. |
| <b>Posição</b> |  |
| <b>Deslocamento local</b> <i>Flutuante2</i> | Aplica um deslocamento às posições dos padrões ao longo da tangente (paralela) e do normal (perpendicular) da spline. |
| <b>Deslocamento Local Aleatório</b> <i>Flutuante2</i> | Aplica um deslocamento aleatório adicional às posições dos padrões ao longo da tangente (paralela) e do normal (perpendicular) da spline. |
| <b>Centro Aleatório de Deslocamento Local</b> <i>Flutuante2</i> | Desloca o centro do deslocamento aleatório aplicado pelo parâmetro Deslocamento local aleatório ao longo da tangente (paralela) e do normal (perpendicular) da spline. |
| <b>Atenuação De Início/Fim Do Deslocamento Local</b> <i>Flutuante2</i> | Afeta a distância do ponto médio da spline até seu início e fim ao aplicar deslocamentos de posição aos padrões.<br>Isso significa que os deslocamentos são diminuídos para padrões mais próximos aos extremos de uma spline. |
| <b>Atenuação de Deslocamento Local por Thickness</b> <i>Flutuante</i> | Fatores no thickness da spline ao aplicar deslocamentos a padrões.<br>Isso significa que os deslocamentos são reduzidos para duplicatas em uma parte de uma spline com um thickness inferior. |
| <b>Deslocamento na spline</b> <i>Flutuante</i> | Aplica um deslocamento de posição aos padrões ao longo das linhas divisórias. |
| <b>Deslocamento aleatório na spline</b> <i>Flutuante</i> | Aplica um deslocamento de posição adicional aos padrões ao longo das linhas divisórias. |
| <b>Rotação</b> |  |
| <b>Alinhar com Tangent</b> <i>Booleano</i> | Gira os padrões para corresponder à direção da spline em seu local. |
| <b>Rotação (Dinâmica)</b> <i>Flutuante</i> | Gira os padrões ao redor de suas tabelas dinâmicas.<br>A posição de pivô pode ser deslocada usando o parâmetro &#39;Shape Pivot&#39;. |
| <b>Rotação Aleatória (Dinâmica)</b> <i>Flutuante</i> | Aplica uma rotação aleatória adicional aos padrões ao redor de suas tabelas dinâmicas.<br>A posição de pivô pode ser deslocada usando o parâmetro &#39;Shape Pivot&#39;. |
| <b>Rotação Aleatória Centralizada (Tabela Dinâmica)</b> <i>Flutuante</i> | Gira ao redor das tabelas dinâmicas do padrão o centro das rotações aleatórias aplicadas pelo parâmetro Rotação aleatória. |
| <b>Rotação (Centro)</b> <i>Flutuante</i> | Gira os padrões ao redor de seu centro. |
| <b>Rotação aleatória (ao centro)</b> <i>Flutuante</i> | Aplica uma rotação aleatória adicional aos padrões ao redor de seu centro. |
| <b>Rotação aleatória centralizada (centro)</b> <i>Flutuante</i> | Gira ao redor do centro do padrão o centro das rotações aleatórias aplicadas pelo parâmetro Rotação aleatória. |
| <b>Cor</b> |  |
| <b>Modo de Mesclagem</b> <i>Inteiro</i> | O método de mesclar as cores de padrões com o plano de fundo e outros padrões sobrepostos:<br><br>- <i>Máx</i>: usar a cor mais clara;<br>- <i>Adicionar</i>: adicionar as cores juntas. |
| <b>Cor Base Da Forma</b> <i>Flutuante</i> | A cor de base dos padrões. |
| <b>Multiplicador de Cores Base da Forma</b> <i>Flutuante</i> | A intensidade da Cor de base de Forma dos padrões.<br>Observação: a cor de saída é o resultado ponderado de todos os multiplicadores de cores. |
| <b>Multiplicador de Thickness de spline</b> <i>Flutuante</i> | A intensidade com que a cor de cada padrão é multiplicada em relação ao thickness da spline em seu local.<br>Observação: a cor de saída é o resultado ponderado de todos os multiplicadores de cores. |
| <b>Multiplicador do Índice de Forma</b> <i>Flutuante</i> | A intensidade com que a cor de cada padrão é multiplicada em relação ao índice normalizado.<br>Observação: a cor de saída é o resultado ponderado de todos os multiplicadores de cores. |
| <b>Modo de Height do Hemisfério</b> <i>Inteiro</i> (Disponível quando &#39;Padrão&#39; está definido como &#39;Hemisfério&#39;) | O efeito do height da spline em um padrão do Hemisfério espalhado nele:<br><br>- <i>Deslocamento</i>: o height da spline é adicionado ao height do Hemisfério;<br>- <i>Escala</i>: o height da spline é multiplicado em relação ao height do Hemisfério. |
| <b>Multiplicador de Height de spline</b> <i>Flutuante</i> | A intensidade com que a cor de cada padrão é multiplicada em relação ao height da spline em seu local.<br>Observação: a cor de saída é o resultado ponderado de todos os multiplicadores de cores. |
| <b>Multiplicador de Escala de Forma</b> <i>Flutuante</i> | A intensidade com que a cor de cada padrão é multiplicada em relação à sua escala.<br>Observação: a cor de saída é o resultado ponderado de todos os multiplicadores de cores. |
| <b>Luminância aleatória</b> <i>Flutuante</i> | Aplica um multiplicador aleatório até o valor especificado para diminuir a luminância dos padrões.<br>Observação: a cor de saída é o resultado ponderado de todos os multiplicadores de cores. |
| <b>Multiplicador de Entrada de Height</b> <i>Flutuante</i> | Controla a intensidade da entrada do Mapa de altura. Esse mapa atua como um multiplicador da luminância atual dos padrões.<br>O efeito deste mapa é combinado com outros parâmetros no grupo &#39;Cor&#39;.<br>Observação: a cor de saída é o resultado ponderado de todos os multiplicadores de cores. |
| <b>Modo de Amostragem de Entrada do Mapa de Heights</b> <i>Inteiro</i> | O método de mapear os valores no Mapa de Altura para os splines:<br><br>- <i>espaço de Textura</i>: os valores são aplicados aos splines nos quais estariam se fossem colocados em uma textura usando as coordenadas UV da textura. Isso aplica efetivamente o valor às linhas de spline &#39;no local&#39;;<br>- <i>Horizontal ao longo da linha de spline</i>: os valores são aplicados diretamente às coordenadas das linhas de spline codificadas (consulte entrada de Palavras de spline), onde cada linha é aplicada a uma linha de spline diferente de cima para baixo;<br>- <i>Hor. ao longo do spline (rand. deslocamento X)</i>: os valores são aplicados diretamente às coordenadas das splines codificadas (consulte a entrada de Coords de spline), com um deslocamento horizontal aleatório no mapa de Escala para cada spline (ou seja, cada linha nas Coords de Spline);<br>- <i>Hora. ao longo do spline (rand. deslocamento Y)</i>: os valores são aplicados diretamente às coordenadas das splines codificadas (consulte entrada de Coords de spline), com um deslocamento vertical aleatório no mapa de Escala para cada spline (ou seja, cada linha nas Coords de spline). |
| <b>Máscara aleatória</b> <i>Flutuante</i> | Ajusta o intervalo do mascaramento aleatório de padrões, onde 0 significa que nenhum padrão está mascarado e 1 significa que todos os padrões estão. |
| <b>Limite de mapa de máscaras</b> <i>Flutuante</i> | Os valores no Mapa de máscaras abaixo desse valor de limite são processados como preto, enquanto os valores acima do limite são processados como branco.<br>Isso significa que todos os padrões em áreas do Mapa de Máscara abaixo desse valor serão mascarados. |
| <b>Modo de Amostragem de Entrada do Mapa de Máscaras</b> <i>Inteiro</i> | O método de mapear os valores no Mapa de Máscara para os splines:<br><br>- <i>espaço de Textura</i>: os valores são aplicados aos splines nos quais estariam se colocados em uma textura usando as coordenadas UV da textura. Isso aplica efetivamente o valor às linhas de spline &#39;no local&#39;;<br>- <i>Horizontal ao longo da linha de spline</i>: os valores são aplicados diretamente às coordenadas das linhas de spline codificadas (consulte entrada de Palavras de spline), onde cada linha é aplicada a uma linha de spline diferente de cima para baixo;<br>- <i>Hor. ao longo do spline (rand. deslocamento X)</i>: os valores são aplicados diretamente às coordenadas das splines codificadas (consulte a entrada de Coords de spline), com um deslocamento horizontal aleatório no mapa de Escala para cada spline (ou seja, cada linha nas Coords de Spline);<br>- <i>Hora. ao longo do spline (rand. deslocamento Y)</i>: os valores são aplicados diretamente às coordenadas das splines codificadas (consulte entrada de Coords de spline), com um deslocamento vertical aleatório no mapa de Escala para cada spline (ou seja, cada linha nas Coords de spline). |
| <b>Inverter mapa de máscara</b> <i>Booleano</i> | Inverte os valores do Mapa de Máscara usando uma operação &#39;Um menos&#39; (1 - x). |
| <b>Inversão de máscara</b> <i>Booleano</i> | Inverte o mascaramento dos padrões. |
| <b>Correção Não Quadrada</b> <i>Booleano</i> | Ajuste as posições dos pontos para manter a forma de spline em resoluções não quadradas. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="scatter-on-spline-grayscale.resources/ScatterOnSplineGrayscale-Variant1-Before.jpg" alt="ScatterOnSplineGrayscale-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="scatter-on-spline-grayscale.resources/ScatterOnSplineGrayscale-Variant1-After.jpg" alt="ScatterOnSplineGrayscale-Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="scatter-on-spline-grayscale.resources/ScatterOnSplineGrayscale-Variant2-Before.jpg" alt="ScatterOnSplineGrayscale-Variant2-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="scatter-on-spline-grayscale.resources/ScatterOnSplineGrayscale-Variant2-After.jpg" alt="ScatterOnSplineGrayscale-Variant2-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Exemplo de nó 2](scatter-on-spline-grayscale.resources/ScatterOnSplineGrayscale-Demo.gif "Exemplo de nó 2")

</td>
<td style="border: 0;" valign="top">

![Demonstração de nó 2](scatter-on-spline-grayscale.resources/ScatterOnSplineGrayscale-Demo2.gif "Demonstração de nó 2")

</td>
</tr>
</table>
