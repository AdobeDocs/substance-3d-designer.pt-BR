---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/scatter-splines-on-splines.html"
breadcrumb-title: ''
description: Use o nó Dispersão splines em splines para distribuir splines filhas ao longo de caminhos de spline pai.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Scatter Splines on Splines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dispersão Splines em Splines
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '2840'
ht-degree: 0%

---


# Dispersão Splines em Splines

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Dispersão Splines em Splines: Ícone](../../../../../../assets/scatter-splines-on-splines-icon.png "Dispersão Splines em Splines: Ícone")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Coloca as splines ao longo das splines principais de entrada.

O nó oferece opções de personalização detalhadas para controlar como as splines são dispersas e permite dispersão splines retas simples ou suas próprias splines personalizadas.

O nó permite criar estruturas intrincadas para mapear cores e imagens usando os nós [Mapeador de spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-grayscale/spline-mapper-grayscale.md) ou usado como um esqueleto para inserir formas usando os nós [Dispersão no Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/scatter-spline-grayscale/scatter-on-spline-grayscale.md).

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Tutorial

Clique na imagem à direita para acessar nosso <b>tutorial dedicado</b>, para obter um tour guiado sobre os recursos do nó e seu uso no contexto de um fluxo de trabalho baseado em spline.

</td>
<td style="border: 0;" valign="top">

[![Nós de Spline de Vídeo](../../../../../../assets/video_spline.png)](https://youtu.be/aUUWV1dYQdI)

</td>
</tr>
</table>

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Visualizar</b> *Tons de cinza* | A visualização das linhas de entrada como uma imagem em tons de cinza. |
| <b>Cordas de spline</b> *Cor* | As coordenadas dos pontos das splines pai codificadas nos canais RGBA de uma imagem colorida: <b>R</b> - posição X <b>G</b> - posição Y <b>B</b> - Height <b>A</b> - Dados empacotados: - Sinal: a spline está fechada (negativa) ou aberta (positiva) - Valor absoluto: Thickness + 1 |
| <b>Dados de Spline</b> *Cor* | Dados adicionais das splines pai codificadas nos canais RGBA de uma imagem colorida: <b>R</b> - Tangentes X <b>G</b> - Tangentes Y <b>B</b> - Tangentes Z <b>A</b> - Não Usados |
| <b>Valor da spline</b> *Inteiro* | O número de splines pai. |
| <b>Cordas de Spline Personalizadas</b> *Cor* | As coordenadas dos pontos das splines personalizadas codificadas nos canais RGBA de uma imagem colorida: <b>R</b> - posição X <b>G</b> - posição Y <b>B</b> - Height <b>A</b> - Dados empacotados: - Sinal: a spline está fechada (negativa) ou aberta (positiva) - Valor absoluto: Thickness + 1 |
| <b>Dados de Spline Personalizados</b> *Cor* | Dados adicionais das splines personalizadas codificadas nos canais RGBA de uma imagem colorida: <b>R</b> - Tangentes X <b>G</b> - Tangentes Y <b>B</b> - Tangentes Z <b>A</b> - Não Usadas |
| <b>Valor de Spline Personalizado</b> *Inteiro* | O número de splines personalizados. |
| <b>Mapa de Escala</b> *Tons de cinza* | O mapa em tons de cinza que controla a escala dos splines dispersos.  O efeito deste mapa é controlado pelo parâmetro <b>Multiplicador de Entrada de Mapa de Escala</b> e é combinado com outros parâmetros no grupo <b>Tamanho</b>. |
| <b>Mapa de rotação</b> *Tons de cinza* | O mapa em tons de cinza que controla a rotação dos splines dispersos.  O efeito desse mapa é controlado pelo parâmetro <b>Multiplicador de Entrada de Mapa de rotação</b> e é combinado com outros parâmetros no grupo <b>Rotação</b>. |

## Conectores de saída

|  |  |
| --- | --- |
| <b>Visualizar</b> *Tons de cinza* | A visualização das splines dispersas como uma imagem em tons de cinza. |
| <b>Cordas de spline</b> *Cor* | As coordenadas dos pontos das splines dispersas codificadas nos canais RGBA de uma imagem colorida: <b>R</b> - posição X <b>G</b> - posição Y <b>B</b> - Height <b>A</b> - Dados empacotados: - Sinal: a spline está fechada (negativa) ou aberta (positiva) - Valor absoluto: Thickness + 1 |
| <b>Dados de Spline</b> *Cor* | Dados adicionais das linhas dispersas codificadas nos canais RGBA de uma imagem colorida: <b>R</b> - Tangentes X <b>G</b> - Tangentes Y <b>B</b> - Não Usados <b>A</b> - Não Usados |
| <b>Valor da spline</b> *Inteiro* | O número de splines dispersos. |

## Parâmetros

|  |  |
| --- | --- |
| <b>Lado</b> *Inteiro* | Controla em que lado(s) das splines pai as splines devem ser espalhadas, considerando que &#39;forward&#39; é a direção das splines *pai*: Left Posiciona as splines no lado esquerdo.   Direita Coloque os splines no lado direito.   Esquerda + Direita Colocam os splines em ambos os lados.   Esquerda/Direita - alternar linhas de Inserção à esquerda e à direita alternadamente (por exemplo, todos os outros lados).   Esquerda / Direita - Escolher aleatoriamente o lado aleatoriamente para cada spline. |
| <b>Modo de Valor</b> *Inteiro* | O método de dispersão dos splines ao longo dos splines pai, o que afeta a quantidade de splines dispersos em cada spline pai: quantidade fixa por spline A quantidade especificada de splines espaçados uniformemente é dispersa.   Espaçamento A quantidade de splines é ajustada automaticamente para se ajustar ao espaçamento uniforme especificado.   Em ambos os casos, o primeiro e o último spline dispersos caem exatamente no início e no final de cada spline pai, respectivamente. |
| <b>Quantidade De Spline Por Spline</b> *Inteiro* | A quantidade de splines com espaçamento uniforme espalhados ao longo de cada spline pai. |
| <b>Espaçamento da spline</b> *Flutuante* | A distância mínima ao longo das linhas divisórias principais pela qual as linhas divisórias devem ser espaçadas, ainda aterrando a primeira e última linha divisória no início e no fim de cada linha divisória principal, respectivamente. |
| <b>Tipo de Spline</b> *Inteiro* | Seleciona o tipo de spline que deve ser espalhado nas splines principais: Seta reta Uma spline simples e reta.   Curva personalizada A(s) curva(s) fornecida(s) para as entradas de <b>Curva personalizada</b>. Várias splines são compatíveis quando anexadas juntas em uma lista. |
| <b>Seleção de Spline Personalizada</b> *Inteiro* | Ao usar várias splines personalizadas anexadas a uma lista, esse parâmetro permite selecionar como essas splines devem ser distribuídas na dispersão.   Lista completa Todas as linhas divisórias são dispersas juntas como um grupo.   Sequencial Cada spline individual é espalhada em ordem, repetindo em torno da lista.   Aleatório Uma spline aleatória é selecionada na lista para cada spline disperso. |
| <b>Iniciar</b> *Flutuante* | Desloca o ponto a partir do início das splines principais onde a dispersão começa.  O valor é o comprimento normalizado de cada spline pai. |
| <b>Fim</b> *Flutuante* | Desloca o ponto a partir do início das splines principais onde a dispersão termina.  O valor é o comprimento normalizado de cada spline pai. |
| <b>Inverter Direção</b> *Booleano* | Inverte a direção dos splines dispersos. |
| <b>Modo de Simetria Esquerda/Direita</b> *Inteiro* | O método de simetria aplicado aos splines espalhados em cada lado dos splines pai.   Desativado Nenhuma simetria é aplicada, as splines são colocadas em cada lado usando uma rotação simples.   Simetria esquerda A spline à esquerda é simétrica à da direita em relação à spline principal.   Simetria direita A spline à direita é simétrica à da esquerda em relação à spline principal. |
| <b>Vínculo Aleatório à Esquerda/Direita</b> *Booleano* | Controla se os splines em cada lado do spline pai devem usar os mesmos valores ao usar rotação aleatória, dimensionamento aleatório etc. Em outras palavras: *- Falso:* cada spline usa valores aleatórios separados *- Verdadeiro:* ambas as splines compartilham os mesmos valores aleatórios |
| <b>Modo de Tabela Dinâmica de Spline</b> *Inteiro* | Define o método de inserção da tabela dinâmica de splines dispersos, o que afeta a rotação e o dimensionamento.   Observe que a tabela dinâmica é *sempre colocada na spline pai* e seus controles afetam a spline dispersa. Em outras palavras: o pivô não se move, é o spline disperso que se move e dimensiona relativamente a ele.   Posição ao longo da spline Mova a tabela dinâmica ao longo da spline dispersa.   Posição absoluta Defina uma posição arbitrária para a tabela dinâmica. |
| <b>Posição de pivô ao longo da spline</b> *Flutuante* | A posição normalizada do pivô ao longo da spline dispersa, onde 0 é o início e 1 é o fim.   Observe que a tabela dinâmica segue a *direção* da spline dispersa e a orientação da spline pode mudar para preservar a posição e a rotação da tabela dinâmica em relação à spline pai. |
| <b>Posição Absoluta da Tabela Dinâmica</b> *Flutuante2* | A posição no espaço UV do pivô. |
| <b>Correção Não Quadrada</b> *Booleano* | Ajuste as posições e o thickness das splines para manter a forma em resoluções não quadradas.   *Observação:* ao usar splines personalizadas, a spline personalizada deve usar a *mesma proporção de imagem* dos nós <b>Splines de Dispersão em Splines</b>. |

+++Tamanho

|  |  |
| --- | --- |
| <b>Escala de spline</b> *Flutuante* | Um controle global para o tamanho de todos os splines, em que 1 é o tamanho original completo.   O dimensionamento é aplicado relativamente à tabela dinâmica de um spline. A posição de pivô pode ser deslocada usando o parâmetro <b>Tabela Dinâmica de Spline</b>. |
| <b>Escala de spline aleatória</b> *Flutuante* | Aplica um multiplicador aleatório até o valor especificado para diminuir o tamanho das splines. |
| <b>Multiplicador de Entrada de Mapa de Escala</b> *Flutuante* | Controla a intensidade da entrada do <b>Mapa de Escala</b>. Esse mapa atua como um multiplicador para o tamanho atual dos padrões.   O efeito deste mapa é combinado com outros parâmetros no grupo <b>Tamanho</b>. |
| <b>Modo de Amostragem de Entrada de Mapa de Escala</b> *Inteiro* | O método de mapear os valores no <b>Mapa de escala</b> para as linhas: espaço de textura. Os valores são aplicados às linhas nas quais estariam se fossem colocadas em uma textura usando as coordenadas UV da textura. Isso aplica efetivamente o valor às splines na horizontal ao longo da spline. Os valores são aplicados diretamente às coordenadas das splines codificadas (consulte entrada <b>Coords de spline</b>), onde cada linha é aplicada a uma spline diferente da parte superior à parte inferior da Hor. ao longo do spline (rand. deslocamento X) Os valores são aplicados diretamente às coordenadas das splines codificadas (consulte a entrada <b>Coords de spline</b>), com um deslocamento horizontal aleatório no <b>Mapa de Escala</b> para cada spline (isto é, cada linha em <b>Coords de spline</b>) Hor. ao longo do spline (rand. Deslocamento Y) Os valores são aplicados diretamente às coordenadas das splines codificadas (consulte a entrada <b>Cordas de spline</b>), com um deslocamento vertical aleatório no <b>Mapa de Escala</b> para cada spline (isto é, cada linha em <b>Cordas de spline</b>) |
| <b>Atenuação de Início/Término</b> *Flutuante2* | Fatores na distância do ponto médio da spline até seu <b>Início</b> e <b>Fim</b> ao dimensionar as splines.   Isso significa que o tamanho é diminuído para splines mais próximos aos membros de um spline. |


+++

+++Posição

|  |  |
| --- | --- |
| <b>Deslocamento local</b> *Flutuante2* | Aplica um deslocamento às posições das splines ao longo da tangente (paralela) e do normal (perpendicular) da spline pai. |
| <b>Deslocamento no Intervalo de Spline</b> *Inteiro* | Define o intervalo de deslocamento aplicado às splines dispersas ao longo das splines pai.   Intervalo O intervalo abrange o intervalo *entre* cada spline dispersa.   spline pai O intervalo abrange o *comprimento total* da spline pai. |
| <b>Deslocamento na spline</b> *Flutuante* | Aplica um deslocamento de posição às linhas ao longo das linhas pai. |
| <b>Intervalo de deslocamento aleatório</b> *Inteiro* | Define o intervalo de deslocamento aleatório aplicado às splines dispersas ao longo das splines pai.   Intervalo O intervalo abrange o intervalo *entre* cada spline dispersa.   spline pai O intervalo abrange o *comprimento total* da spline pai. |
| <b>Deslocamento aleatório na spline</b> *Flutuante* | Aplica um deslocamento de posição adicional às splines ao longo das splines principais. |
| <b>Deslocamento por Thickness</b> *Flutuante* | Aplica um deslocamento às splines dispersas ao longo do normal das splines pai, até o thickness dessas splines.   Efetivamente, um valor de 1 permite colocar as splines dispersas na *superfície* do envelope das splines pai. |


+++

+++Giro

|  |  |
| --- | --- |
| <b>Alinhamento de Spline Personalizado</b> *Inteiro* | Controla a orientação inicial da(s) spline(s) personalizada(s) nas splines pai.   tangente do primeiro ponto Os splines são orientados de acordo com a tangente do primeiro ponto. Em outras palavras, eles saem das linhas principais na direção definida pelo primeiro ponto.   Espaço da imagem As splines são colocadas como aparecem originalmente, sem nenhum ajuste adicional à sua posição ou orientação, como se a imagem que as representa estivesse na spline pai. |
| <b>Modo de rotação</b> *Inteiro* | Define a orientação inicial das splines dispersas.   Da spline As splines são orientadas para corresponder ao *normal* das splines pai em seu local.   Absoluto As splines são todas orientadas da *mesma maneira*, independentemente da direção das splines pai. |
| <b>Rotação</b> *Flutuante* | Gira os splines ao redor de seus pivôs, em número de voltas. A posição de pivô pode ser deslocada usando o parâmetro <b>Tabela Dinâmica de Spline</b>. |
| <b>Rotação aleatória</b> *Flutuante* | Aplica uma rotação aleatória adicional aos splines ao redor de seus pivôs, em número de voltas. A posição de pivô pode ser deslocada usando o parâmetro <b>Tabela Dinâmica de Spline</b>. |
| <b>Ângulo esquerdo/direito</b> *Flutuante* | Controla o ângulo de rotação simétrica aplicado às splines em cada lado das splines pai, em número de voltas. |
| <b>Ângulo Aleatório à Esquerda/Direita</b> *Flutuante* | Adiciona uma quantidade aleatória de rotação simétrica às splines de cada lado das splines pai, em número de voltas. |
| <b>Multiplicador de Entrada de Mapa de rotação</b> *Flutuante* | Controla a intensidade da entrada de <b>Mapa de rotação</b>. Este mapa atua como um multiplicador para a rotação atual dos padrões.   O efeito deste mapa é combinado com outros parâmetros no grupo <b>Rotação</b>. |
| <b>Modo de Amostragem de Entrada de Mapa de rotação</b> *Inteiro* | O método de mapear os valores no <b>Mapa de rotação</b> para as linhas: espaço de textura. Os valores são aplicados às linhas nas quais estariam se fossem colocadas em uma textura usando as coordenadas UV da textura. Isso aplica efetivamente o valor às splines “no local”, horizontais ao longo da spline. Os valores são aplicados diretamente às coordenadas das splines codificadas (consulte entrada <b>Coords de spline</b>), onde cada linha é aplicada a uma spline diferente de cima para baixo, Hor. ao longo do spline (rand. deslocamento X) Os valores são aplicados diretamente às coordenadas das splines codificadas (consulte a entrada <b>Coords de spline</b>), com um deslocamento horizontal aleatório no <b>Mapa de rotação</b> para cada spline (isto é, cada linha em <b>Coords de spline</b>).   Hor. ao longo do spline (rand. Deslocamento Y) Os valores são aplicados diretamente às coordenadas das splines codificadas (consulte a entrada <b>Coords de spline</b>), com um deslocamento vertical aleatório no <b>Mapa de rotação</b> de cada spline (isto é, cada linha em <b>Coords de spline</b>)<b>.</b> |
| <b>A Entrada Do Mapa de rotação Afeta</b> *Inteiro* | Seleciona o parâmetro de rotação afetado pelo <b>Mapa de rotação</b>: rotação da spline. O mapa afeta a rotação global das splines no sentido horário.   Ângulo esquerdo/direito O mapa afeta a rotação simétrica das <b>linhas esquerda/direita</b>. |


+++

+++Altura

|  |  |
| --- | --- |
| <b>Iniciar Modo de Height</b> *Inteiro* | O método de calcular o height inicial dos splines dispersos.   Manual Defina o mesmo valor absoluto para todas as splines dispersas.   Da spline pai (+ spline personalizada) Use o height da spline pai e, em seguida, adicione o height da spline personalizada usando a <b>Mult de height de início de spline personalizada</b> parâmetro.   Na spline personalizada, use o height da spline personalizada como está.   *Observação:* defina <b>Tipo de Spline</b> como &#39;Spline Personalizada&#39; e conecte as entradas de <b>Spline Personalizada</b> para usar o height de splines personalizadas. |
| <b>Mult de Height de Início de Spline Personalizado.</b> *Flutuante* | Controla a contribuição do próprio height inicial da spline personalizada para o height inicial das splines dispersas, onde 1 significa que o height completo da spline personalizada é usado.   O height da spline personalizada é usado de forma diferente, de acordo com o <b>Modo de Height Inicial</b> selecionado: *- Da spline pai (+ spline personalizada):* O height é adicionado à spline pai *- Da spline personalizada:* O height é usado diretamente |
| <b>Iniciar Deslocamento de Height</b> *Flutuante* | Aplica um deslocamento absoluto ao height inicial da spline dispersa. |
| <b>Iniciar Height</b> *Flutuante* | Define um valor absoluto para o height inicial da spline dispersa. |
| <b>Encerrar Modo de Height</b> *Inteiro* | O método de calcular o height final dos splines dispersos.   Manual Defina o mesmo valor absoluto para todas as splines dispersas.   Da spline pai (+ spline personalizada) Use o height da spline pai e adicione o height da spline personalizada usando o <b>Módulo de Height de extremidade de spline personalizada.</b> parâmetro.   Na spline personalizada, use o height da spline personalizada como está.     *Observação:* defina <b>Tipo de Spline</b> para Spline Personalizada e conecte as entradas de <b>Spline Personalizada</b> para usar o height de splines personalizadas. |
| <b>Mult de Height de Fim de Spline Personalizado.</b> *Flutuante* | Controla a contribuição do próprio height final da spline personalizada para o height final das splines dispersas, onde 1 significa que o height completo da spline personalizada é usado.   O height da spline personalizada é usado de forma diferente, de acordo com o <b>Modo de Height Final</b> selecionado: *- Da spline pai (+ spline personalizada):* O height é adicionado à spline pai *- Da spline personalizada:* O height é usado diretamente |
| <b>Deslocamento do Height Final</b> *Flutuante* | Aplica um deslocamento absoluto ao height final da spline dispersa. |
| <b>Encerrar Height</b> *Flutuante* | Define um valor absoluto para o height final da spline dispersa. |


+++

+++Espessura

|  |  |
| --- | --- |
| <b>Iniciar Modo de Thickness</b> *Inteiro* | O método de calcular o thickness inicial dos splines dispersos.   Manual Defina o mesmo valor absoluto para todas as splines dispersas.   Da spline pai Use o thickness da spline pai.   Na spline personalizada Use o thickness da spline personalizada.   *Observação:* defina <b>Tipo de Spline</b> para Spline Personalizada e conecte as entradas de <b>Spline Personalizada</b> para usar o thickness de splines personalizadas. |
| <b>Iniciar Multiplicador de Thickness</b> *Flutuante* | Dimensiona o thickness inicial dos splines dispersos, onde 1 é o thickness completo. |
| <b>Iniciar Deslocamento de Thickness</b> *Flutuante* | Aplica um deslocamento absoluto ao thickness inicial da spline dispersa. |
| <b>Iniciar Thickness</b> *Flutuante* | Define um valor absoluto para o thickness inicial da spline dispersa. |
| <b>Encerrar Modo de Thickness</b> *Inteiro* | O método de calcular o thickness final dos splines dispersos.   Manual Defina o mesmo valor absoluto para todas as splines dispersas.   Da spline pai Use o thickness da spline pai.   Na spline personalizada Use o thickness da spline personalizada.   *Observação:* defina <b>Tipo de Spline</b> para Spline Personalizada e conecte as entradas de <b>Spline Personalizada</b> para usar o thickness de splines personalizadas. |
| <b>Encerrar Multiplicador de Thickness</b> *Flutuante* | Dimensiona o thickness inicial dos splines dispersos, onde 1 é o thickness completo. |
| <b>Deslocamento do Thickness Final</b> *Flutuante* | Aplica um deslocamento absoluto ao thickness final da spline dispersa. |
| <b>Encerrar Thickness</b> *Flutuante* | Define um valor absoluto para o thickness final da spline dispersa. |


+++

+++Visualização

|  |  |
| --- | --- |
| <b>Mostrar Auxiliar de Direção</b> *Booleano* | Exibe um ponto no início da spline e uma ponta de seta no final da saída de <b>Visualização</b>. |
| <b>Mostrar Envelope de Thickness</b> *Booleano* | Exibe linhas adicionais nas bordas do thickness da spline. |
| <b>Thickness (px)</b> *Flutuante* | Ajusta o thickness da visualização da spline na saída de <b>Visualização</b>, em número de pixels. |
| <b>Valor de Segmentos</b> *Inteiro* | Ajusta o número de segmentos usados para desenhar a visualização de spline na saída de <b>Visualização</b>. Um valor mais alto resulta em uma linha mais suave. |
| <b>Intensidade de fundo</b> *Flutuante* | A intensidade da entrada <b>Visualizar</b> na visualização de saída <b>Visualizar</b>. |


+++

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Dispersão Splines em Splines: Exemplo 1](../../../../../../assets/scatter-splines-on-splines-example-1.png "Dispersão Splines em Splines: Exemplo 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Dispersão Splines em Splines: Exemplo 1](../../../../../../assets/scatter-splines-on-splines-example-2.png "Dispersão Splines em Splines: Exemplo 1"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Dispersão Splines em Splines: Exemplo 3](../../../../../../assets/scatter-splines-on-splines-example-4.png "Dispersão Splines em Splines: Exemplo 3"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Dispersão Splines em Splines: Exemplo 4](../../../../../../assets/scatter-splines-on-splines-example-3.png "Dispersão Splines em Splines: Exemplo 4"){zoomable="yes"}

</td>
</tr>
</table>

## Renderizações

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Splines de Dispersão em Splines: Renderizar 1](../../../../../../assets/scatter-splines-on-splines-demo-1.png "Splines de Dispersão em Splines: Renderizar 1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Splines de Dispersão em Splines: Renderizar 2](../../../../../../assets/scatter-splines-on-splines-demo-3.png "Splines de Dispersão em Splines: Renderizar 2"){zoomable="yes"}

</td>
</tr>
</table>

![Splines de Dispersão em Splines: Renderizar 3](../../../../../../assets/scatter-splines-on-splines-demo-2.png "Splines de Dispersão em Splines: Renderizar 3"){zoomable="yes"}
