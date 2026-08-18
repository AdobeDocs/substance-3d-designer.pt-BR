---
title: Concha
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Operador > Shell
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---


# Concha

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de shell](./3d-sdf-op-shell.png "Shell")

<b>Entrada:</b> Função SDF > Operador

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Torna uma forma SDF oca, com thickness ajustável para o envelope resultante.

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
| <b>FDS</b> *Flutuante* | A forma SDF de entrada. |
| <b>Thickness</b> *Flutuante* | O thickness da concha, aplicado para dentro e para fora.<br>O shell é arredondado quando o thickness é aumentado.<br><br><i>Padrão: 0.02</i> |
