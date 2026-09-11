---
title: Cubo
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Primitivo > Cubo
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Cubo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de cubo](./3d-sdf-cube.png "Cubo")

<b>Entrada:</b> Função SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma Função SDF para um cubo, com tamanho XYZ ajustável e arredondamento de bordas.

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
| <b>Tamanho</b> *Precisão decimal 3* | O tamanho do cubo em X, Y e Z.<br><br><i>Padrão: (1, 1, 1)</i> |
| <b>Arredondamento</b> *Precisão decimal* | O raio dos arcos arredondados aplicados às bordas do cubo.<br><br><i>Observação:</i> bordas sólidas podem aparecer onde os raios de arredondamento se cruzam.<br><br><i>Padrão: 0</i> |
| <b>Posição de pivô (local)</b> *Precisão decimal 3* | A posição do espaço global da tabela dinâmica local do cubo, onde (0, 0, 0) coloca a tabela dinâmica no centro do cubo.<br><br><i>Padrão: (0, 0, -0,5)</i> |
| <b>Posição central</b> *Precisão decimal 3* | A posição do espaço global da tabela dinâmica do cubo.<br><br><i>Padrão: (0, 0, 0)</i> |
| <b>P</b> *Precisão decimal 3* | A posição transformada do espaço mundial. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
