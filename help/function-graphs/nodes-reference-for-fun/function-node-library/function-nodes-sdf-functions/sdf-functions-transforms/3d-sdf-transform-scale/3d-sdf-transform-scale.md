---
title: Escala
description: Designer > Gráficos de composição de Substance > Referência dos nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Transformo > Escala
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---


# Dimensionar

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de escala](./3d-sdf-transform-scale.png "Escala")

<b>Em:</b> Função SDF > Transformar

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Dimensione uniformemente uma forma SDF.

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
| <b>FDS</b> *Precisão decimal* | A forma SDF de entrada. |
| <b>Escala</b> *Precisão decimal* | O fator de escala uniforme.<br><br><i>Padrão: 1</i> |
| <b>Posição de pivô</b> *Precisão decimal 3* | A posição do espaço global da tabela dinâmica local da forma SDF, onde (0, 0, 0) coloca a tabela dinâmica no centro da forma SDF. <br>Define a origem do dimensionamento.<br><br><i>Padrão: (0, 0, 0)</i> |
| <b>P</b> *Precisão decimal 3* | A posição transformada do espaço mundial. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
