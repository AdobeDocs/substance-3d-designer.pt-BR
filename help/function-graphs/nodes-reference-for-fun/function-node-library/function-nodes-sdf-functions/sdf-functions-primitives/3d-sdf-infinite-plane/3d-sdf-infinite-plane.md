---
title: Plano infinito
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Primitivo > Plano infinito
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 1%

---


# Plano infinito

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de plano infinito](./3d-sdf-infinite-plane.png "Plano infinito")

<b>Entrada:</b> Função SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma Função SDF para um plano infinito de orientação e posição ajustáveis.

</td>
</tr>
</table>

<a name='inputs'></a>

>[!INFO]
> 
> Para saber mais sobre conceitos e fluxos de trabalho que envolvem Funções SDF, acesse a página dedicada: [Trabalhando com Funções SDF](../../working-with-sdf-functions.md)

## Entradas

|  |  |
| :--- | :--- |
| <b>Normal</b> *Precisão decimal 3* | O vetor normal do espaço do mundo do plano infinito, que controla sua orientação.<br>O vetor está normalizado.<br><br><i>Padrão: (0, 0, 1)</i> |
| <b>Posição central</b> *Precisão decimal* | A posição do espaço global do pivô do plano, como uma distância da origem mundial ao longo do plano normal.<br><br><i>Padrão: 0</i> |
| <b>P</b> *Precisão decimal 3* | A posição transformada do espaço mundial. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
