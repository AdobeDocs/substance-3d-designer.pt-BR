---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-flow-mapper.html"
breadcrumb-title: ''
description: Use o nó Mapeador de fluxo de spline para criar padrões de textura fluida ao longo de caminhos de spline para efeitos orgânicos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Flow Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mapeador do fluxo de spline
user-guide-description: ''
user-guide-title: ''
source-git-commit: e4c44720897b98db608bc9feabb860d4b1baf332
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---


# Mapeador do fluxo de spline

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de nó](../../../../../../assets/spline-flow-mapper-icon.png "Ícone de nó")

<b>Ferramentas De Spline E Caminho </b> Em: > Ferramenta de linha flexível

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Desenha um mapa de fluxo no qual os dados do vetor de fluxo são desenhados ao longo das linhas de entrada.

Isso permite usar splines para controlar a direção, a trajetória, a intensidade e o thickness do fluxo, bem como a rampa de gradiente usada para esmaecer os dados desenhados em um plano de fundo neutro.

</td>
</tr>
</table>

>[!IMPORTANT]
>
> O resultado pode incluir artefatos indesejados fora do envelope da spline ao usar valores de thickness muito baixos. Esse é um problema conhecido.

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Cordas de spline</b> <i>Cor</i> | As coordenadas dos pontos das linhas divisórias de entrada codificadas nos canais RGBA de uma imagem colorida:<br><b>R</b> - Posição X<br><b>G</b> - Posição Y<br><b>B</b> - Height<br><b>A</b> - Dados empacotados:<br>- Sinal: a linha divisória é fechada (negativa) ou aberta (positiva);<br>- Valor absoluto: Thickness + 1. |
| <b>Dados de Spline</b> <i>Cor</i> | Dados adicionais das splines de entrada codificadas nos canais RGBA de uma imagem colorida.<br><b>R</b> - Tangentes X<br><b>G</b> - Tangentes Y<br><b>B</b> - Não Usadas<br><b>A</b> - Não Usadas |
| <b>Valor da spline</b> <i>Inteiro</i> | O número de splines de entrada. |
| <b>Curva de Perfil de Atenuação</b> <i>Tons de cinza</i> | <span id="_Hlk135812146"></span>A imagem que descreve uma curva usando os valores de sua primeira linha de pixels. Quando o parâmetro Perfil de atenuação é definido como Curva de perfil de entrada, essa entrada é usada para controlar o gradiente de atenuação dos dados de vetor de fluxo desenhados ao longo da spline.<br>Você pode usar um nó [Curva](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) para criar a curva. |

<a name="outputs"></a>

## Saídas

|  |  |
|:---|:---|
| <b>Saída</b> <i>Cor</i> | O mapa de fluxo de saída codificado em uma imagem colorida. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Valor de Segmentos</b> <i>Inteiro</i> | As splines são simplificadas em segmentos antes que os dados de fluxo vetorial os atravessem. Uma quantidade maior de segmentos resulta em um mapeamento de fluxo mais suave ao longo das curvas. |
| <b>Modo</b> <i>Inteiro</i> | O método de seleção das splines ao longo das quais os dados de fluxo vetorial devem ser desenhados:<br><br>- <i>Desenhar Lista de Spline</i>: todas as splines na lista de entrada são usadas;<br>- <i>Desenhar Spline Único</i>: apenas a spline com o índice especificado é usada;<br>- <i>Desenhar Intervalo de Spline</i>: apenas as splines com índice incluído no intervalo especificado são usadas. |
| <b>Desenhar Índice de Spline</b> <i>Inteiro</i> (Disponível quando &#39;Mode&#39; está definido como &#39;Draw Single Spline&#39;) | O índice da spline ao longo da qual os dados de fluxo vetorial devem ser desenhados. |
| <b>Desenhar Intervalo De Spline</b> <i>Inteiro2</i> (Disponível quando &#39;Mode&#39; estiver definido como &#39;Draw Spline Range&#39;) | A faixa de índices das splines na qual os dados de fluxo vetorial devem ser desenhados. |
| <b>Modo de Thickness</b> <i>Inteiro</i> | O método de definição do thickness dos dados de fluxo vetorial desenhados<br><br>- <i>Manual</i>: defina o thickness explicitamente com um valor arbitrário;<br>- <i>Da spline</i>: use o thickness da spline. |
| <b>Thickness</b> <i>Precisão decimal</i> (Disponível quando &#39;Modo de Thickness&#39; estiver definido como &#39;Manual&#39;) | O valor arbitrário para o thickness dos dados de fluxo vetorial desenhados ao longo das splines. |
| <b>Multiplicador de Thickness</b> <i>Precisão decimal</i> (Disponível quando &#39;Modo de Thickness&#39; estiver definido como &#39;De Spline&#39;) | Um multiplicador global para o thickness dos dados de fluxo vetorial desenhados ao longo das splines, quando esse thickness é impulsionado pela splines. |
| <b>Direção</b> <i>Inteiro</i> | A direção do fluxo do vetor em relação à spline.<br><br>- <i>Tangente</i>: usar o vetor tangente da spline;<br>- <i>Normal</i>: usar o vetor normal da spline;<br>- <i>Normal Espelhado</i>: usar a versão espelhada do vetor normal da spline. |
| <b>Inverter Direção</b> <i>Booleano</i> | Inverte a direção dos splines, o que também afeta a direção do vetor de fluxo. |
| <b>Perfil de Atenuação</b> <i>Inteiro</i> | A rampa de gradiente usada para desenhar a atenuação dos dados de vetor de fluxo desenhados ao longo da spline:<br><br>- <i>Linear</i>: use uma rampa de gradiente linear;<br>- <i>Gaussiana</i>: use uma rampa de gradiente gaussiana<br>- <i>Curva de Perfil de Entrada</i>: use a curva fornecida para a entrada da Curva de Perfil de Atenuação como uma rampa de gradiente. |
| <b>Iniciar Atenuação</b> <i>Booleano</i> | <span id="_Hlk135769398"></span>Adiciona um semicírculo no início da spline. O semicírculo usa a mesma atenuação do spline. |
| <b>Encerrar atenuação</b> <i>Booleano</i> | Adiciona um semicírculo no final da spline. O semicírculo usa a mesma atenuação do spline. |
| <b>Atenuação do Height da spline</b> <i>Flutuante</i> | A intensidade dos dados do vetor de fluxo desenhados ao longo da spline é multiplicada pelo height da spline, no qual os dados desenhados desaparecem para a cor neutra (0,5, 0,5, 0) do plano de fundo à medida que a height se aproxima de 0. |
| <b>Correção Não Quadrada</b> <i>Booleano</i> | Ajuste as posições e o thickness dos pontos para manter a forma de spline em resoluções não quadradas. Isso também afeta a distribuição uniforme. |

## Exemplos

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineFlowMapper-Variant1-Before.jpg" alt="SplineFlowMapper-Variant1-Before">
      <br><i>Antes</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineFlowMapper-Variant1-After.jpg" alt="SplineFlowMapper-Variant1-After">
      <br><i>Depois</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![Exemplo de nó 2](../../../../../../assets/SplineFlowMapper-Demo.gif "Exemplo de nó 2")

</td>
</tr>
</table>
