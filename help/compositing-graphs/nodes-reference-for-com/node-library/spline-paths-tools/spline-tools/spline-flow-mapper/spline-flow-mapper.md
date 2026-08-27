---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-flow-mapper.html"
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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '705'
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

## Conectores de entrada

<b>Cordas de spline</b> *Cor* As coordenadas dos pontos das splines de entrada codificadas nos canais RGBA de uma imagem colorida:\
<b> R</b> - Posição X\
<b> G</b> - posição Y\
<b> B</b> - Height\
<b>A</b> - Dados empacotados:\
* Sinal: Spline é fechado (negativo) ou aberto (positivo);\
* Valor absoluto: Thickness + 1.

<b>Dados de Spline</b> *Cor* Dados adicionais das splines de entrada codificados nos canais RGBA de uma imagem colorida.\
<b> R</b> - Tangentes X\
<b> G</b> - Tangentes Y\
<b> B</b> - Não Usado\
<b> A</b> - Não Usado

<b>Valor da spline</b> *Inteiro* O número de splines de entrada.

<b>Curva de Perfil de Atenuação</b> *Tons de cinza*<span id="_Hlk135812146"></span> A imagem que descreve uma curva usando os valores da primeira linha de pixels.\
Quando o parâmetro Perfil de atenuação é definido como Curva de perfil de entrada, essa entrada é usada para controlar o gradiente de atenuação dos dados de vetor de fluxo desenhados ao longo da spline.\
Você pode usar um nó [Curva](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md) para criar a curva.

## Conectores de saída

<b>Saída</b> *Cor* O mapa de fluxo de saída codificado em uma imagem colorida.

## Parâmetros

<b>Valor de Segmentos</b> *Inteiros* As splines são simplificadas em segmentos antes que os dados de fluxo vetorial os atravessem.\
Uma quantidade maior de segmentos resulta em um mapeamento de fluxo mais suave ao longo das curvas.

<b>Modo</b> *Inteiro* O método de selecionar as splines ao longo das quais os dados de fluxo vetorial devem ser desenhados:\
*- Desenhar Lista Spline*: todas as linhas na lista de entrada são usadas;\
*- Desenhar spline única*: apenas a spline com o índice especificado é usada;\
*- Desenhar Intervalo de spline*: Somente as splines cujo índice está incluído no intervalo especificado são usadas.

<b>Desenhar Índice de Spline</b> *Inteiro* (Disponível quando ‘Mode’ está definido como ‘Draw Single Spline’)O índice da spline ao longo da qual os dados de fluxo vetorial devem ser desenhados.

<b>Desenhar Intervalo De Spline</b> *Inteiro2* (Disponível quando ‘Mode’ estiver definido como ‘Draw Spline Range’)O intervalo de índices para as splines ao longo do qual os dados de fluxo de vetor devem ser desenhados.

<b>Modo de Thickness</b> *Inteiro* O método de definir o thickness dos dados de fluxo vetorial desenhados\
*- Manual*: Defina o thickness explicitamente com um valor arbitrário;\
*- Da spline*: use o thickness da spline.

<b>Thickness</b> *Flutuante* (Disponível quando ‘Modo de Thickness’ está definido como ‘Manual’)O valor arbitrário para o thickness dos dados de fluxo vetorial desenhados ao longo das splines.<b></b>

<b>Multiplicador de Thickness</b> *Flutuante* (Disponível quando ‘Modo de Thickness’ está definido como ‘De spline’)Um multiplicador global para o thickness dos dados de fluxo vetorial desenhados ao longo das splines, quando esse thickness é conduzido pelo das splines.

<b>Direção</b> *Inteiro* A direção do fluxo vetorial em relação à spline.\
*- Tangente*: usar o vetor tangente da spline;\
*- Normal*: Usar o vetor normal da spline;\
*- Normal Espelhado*: Use a versão espelhada do vetor normal da spline.

<b>Inverter Direção</b> *Booleano* Inverte a direção das splines, o que também afeta a direção do vetor de fluxo.

<b>Perfil de Atenuação</b> *Inteiro* A rampa de gradiente usada para desenhar a atenuação dos dados do vetor de fluxo desenhados ao longo da spline:\
*- Linear*: Usar uma rampa de gradiente linear;\
*- Gaussiana*: Usar uma rampa de gradiente gaussiana\
*- Curva de Perfil de Entrada*: use a curva fornecida para a entrada da Curva de Perfil de Atenuação como uma rampa de gradiente.

<b>Iniciar Atenuação</b> *Booleano*<span id="_Hlk135769398"></span> Adiciona um semicírculo no início da spline. O semicírculo usa a mesma atenuação do spline.

<b>Encerrar atenuação</b> *Booleano* Adiciona um semicírculo no final da spline. O semicírculo usa a mesma atenuação do spline.

<b>Atenuação do Height da spline</b> *Flutuante* A intensidade dos dados de vetor de fluxo desenhados ao longo da spline é multiplicada em relação ao height da spline, onde os dados desenhados desaparecem gradualmente até a cor neutra do plano de fundo (0,5, 0,5, 0) à medida que o height se aproxima de 0.

<b>Correção não quadrada </b>*Booleana* Ajuste as posições e o thickness dos pontos para manter a forma de spline em resoluções não quadradas.\
Isso também afeta a distribuição uniforme.

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
