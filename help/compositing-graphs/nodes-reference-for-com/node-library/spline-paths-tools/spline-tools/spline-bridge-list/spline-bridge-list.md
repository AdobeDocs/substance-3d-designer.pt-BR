---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-list.html"
breadcrumb-title: ''
description: Use o nó Lista de pontes de spline para fazer a ponte de texturas entre várias splines em uma lista para padrões complexos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge (List)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ponte de spline (lista)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---


# Ponte de spline (lista)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](spline-bridge-list.resources/spline-bridge-list-01.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gera splines atravessando todas as splines na lista de entrada, ao longo dessas splines.

As splines geradas podem ser lineares (retas) ou quadráticas (curvas).

</td>
</tr>
</table>

>[!TIP]
>
> As splines geradas vão da primeira spline na lista até a última e atravessam as splines intermediárias seguindo estritamente a ordem dessas splines na lista.
> 
> Portanto, você deve ter cuidado com a ordem na qual você acrescenta splines com antecedência.

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Visualizar</b> <i>Tons de cinza</i> | A visualização das linhas de entrada como uma imagem em tons de cinza. |
| <b>Cordas de spline</b> <i>Cor</i> | As coordenadas dos pontos das linhas divisórias de entrada codificadas nos canais RGBA de uma imagem colorida:<br><b>R</b> - Posição X<br><b>G</b> - Posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br>- Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> <i>Cor</i> | Dados adicionais das splines de entrada codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usadas<br><b>A</b> - Não Usadas |
| <b>Valor da spline</b> <i>Inteiro</i> | O número de splines de entrada. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Visualizar</b> <i>Tons de cinza</i> | A visualização das linhas de saída como uma imagem em tons de cinza. |
| <b>Cordas de spline</b> <i>Cor</i> | As coordenadas dos pontos das linhas divisórias de saída codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Posição X<br><b>G</b> - Posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br>- Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> <i>Cor</i> | Dados adicionais das splines de saída codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usadas<br><b>A</b> - Não Usadas |
| <b>Valor da spline</b> <i>Inteiro</i> | O número de splines de saída. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Quantidade de Spline da Ponte</b> <i>Inteiro</i> | O número de splines gerados nas splines de entrada. |
| <b>Tipo de Splines de Ponte</b> <i>Inteiro</i> | O tipo de spline gerado:<br><br>- Linear: uma spline nítida conectando splines intermediários com trajetórias retas do Início ao Fim;<br>- Bezier Quadrático: uma spline curva conectando splines intermediários com trajetórias suaves do Início ao Fim.<br><br>Observação: são necessárias pelo menos 3 splines de entrada para calcular uma spline de Bezier Quadrática. |
| <b>As splines de entrada estão fechadas</b> <i>Booleano</i> | Controla se o primeiro e o último pontos de splines de entrada devem ser processados como um único ponto. Isso evita a duplicação do primeiro e último splines de travessia. |
| <b>Inverter Direção</b> <i>Booleano</i> | Inverte a direção da spline. |
| <b>Fechar Spline da Ponte</b> <i>Booleano</i> | Estende as linhas divisórias transversais para conectar à primeira linha divisória da lista de entrada. |
| <b>Deslocamento da Primeira Curva da Ponte</b> <i>Flutuante2</i> | Aplica um deslocamento ao início de todos os splines atravessados. O valor é o comprimento normalizado das splines de entrada.<br>As splines geradas que atendem ao início ou ao fim das splines atravessadas são deixadas lá. |
| <b>Deslocamento da Última Curva da Ponte</b> <i>Flutuante2</i> | Aplica um deslocamento ao final de todos os splines atravessados. O valor é o comprimento normalizado das splines de entrada.<br>As splines geradas que atendem ao início ou ao fim das splines atravessadas são deixadas lá. |
| <b>Intervalo de deslocamento aleatório</b> <i>Inteiro</i> | A distância máxima usada para o deslocamento aleatório aplicado nas splines.<br><br>- <i>spline pai:</i> o comprimento total das splines pai é usado. Pode causar sobreposições.<br>- <i>Intervalo:</i> O intervalo entre as linhas de ponte é usado. Isso reduz as sobreposições. Essa distância diminui à medida que a quantidade de splines de ponte aumenta. |
| <b>Iniciar Deslocamento Aleatório</b> <i>Flutuante</i> | Um multiplicador para o deslocamento aleatório aplicado na posição inicial das linhas de ponte, onde a distância máxima é especificada pelo parâmetro <b>Intervalo de deslocamento aleatório</b>. |
| <b>Encerrar Deslocamento Aleatório</b> <i>Flutuante</i> | Um multiplicador para o deslocamento aleatório aplicado na posição final das linhas de ponte, onde a distância máxima é especificada pelo parâmetro <b>Intervalo de deslocamento aleatório</b>. |
| <b>Deslocamento Aleatório Global</b> <i>Flutuante</i> | Um multiplicador para o *valor igual* de deslocamento aleatório aplicado às *posições inicial e final das linhas de ponte, em que a distância máxima é especificada pelo parâmetro <b>Intervalo de deslocamento aleatório</b>.* |
| <b>Distribuição Uniforme</b> <i>Booleano</i> | Quando Verdadeiro, os pontos das splines geradas são espaçados uniformemente do início ao fim. |
| <b>Thickness</b> |  |
| <b>Modo de Thickness</b> <i>Inteiro</i> | O método de aquisição do valor de thickness para as linhas de ponte.<br><br>- <i>Herdar das linhas de ponte pai:</i> O thickness das linhas de ponte pai nas posições inicial e final das linhas de ponte é usado<br>- <i>Substituir:</i> O valor arbitrário especificado no parâmetro <b>Thickness</b> é usado |
| <b>Thickness</b> <i>Precisão decimal</i> | O valor de thickness absoluto aplicado às linhas de ponte. |
| <b>Thickness aleatório</b> <i>Precisão decimal</i> | Um multiplicador aleatório para o thickness das linhas de ponte, no qual o thickness inicial ao qual esse multiplicador está aplicado é especificado pelo parâmetro <b>modo de Thickness</b>. |
| <b>Height</b> |  |
| <b>Modo de Height</b> <i>Inteiro</i> | O método de aquisição do valor de height para as linhas de ponte.<br><br>- <i>Herdar das linhas de ponte pai:</i> O height das linhas de ponte pai nas posições inicial e final das linhas de ponte é usado<br>- <i>Substituir:</i> O valor arbitrário especificado no parâmetro <b>Height</b> é usado |
| <b>Deslocamento de Height</b> <i>Precisão decimal</i> | O valor de deslocamento aplicado ao height herdado das linhas de ponte pai, antes que esse height seja aplicado às linhas de ponte. |
| <b>Height</b> <i>Precisão decimal</i> | O valor de height absoluto aplicado às linhas de ponte. |
| <b>Height aleatório</b> <i>Precisão decimal</i> | Uma quantidade aleatória de ajustes no height das linhas de ponte, em que esse ajuste depende do parâmetro selecionado <b>Modo de Height</b>:<br><br>- <i>Herdar das linhas de ponte pai:</i> O valor é um multiplicador para o height herdado.<br>- <i>Substituir:</i> O valor é um deslocamento adicionado ao height. |
| <b>Correção Não Quadrada</b> <i>Booleano</i> | Ajuste as posições e o thickness dos pontos para manter a forma de spline em resoluções não quadradas. Isso também afeta a distribuição uniforme. |
| <b>Visualizar</b> |  |
| <b>Mostrar Auxiliar de Direção</b> <i>Booleano</i> | Exibe um ponto no início da spline e uma ponta de seta no final da saída de Visualização. |
| <b>Mostrar Envelope de Thickness</b> <i>Booleano</i> | Exibe linhas adicionais nas bordas do thickness da spline. |
| <b>Valor de Segmentos</b> <i>Inteiro</i> | Ajusta o número de segmentos usados para desenhar a visualização de spline na saída da Visualização. Um valor mais alto resulta em uma linha mais suave. |
| <b>Thickness (px)</b> <i>Flutuante</i> | Ajusta o thickness da visualização da spline em pixels na saída da Visualização. |
| <b>Intensidade de visualização do plano de fundo</b> <i>Flutuante</i> | A intensidade da visualização da Visualização. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-bridge-list.resources/spline-bridge-list-02.jpg" alt="SplineBridge-List_Variant1_Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="spline-bridge-list.resources/spline-bridge-list-03.jpg" alt="SplineBridge-List_Variant1_After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](spline-bridge-list.resources/spline-bridge-list-04.gif "Exemplo de nó 2")

</td>
</tr>
</table>

![Nó no gráfico](spline-bridge-list.resources/spline-bridge-list-05.jpg "Nó no gráfico")
