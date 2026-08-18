---
title: Quadrado de pirâmide
description: Designer > Gráficos de composição de Substance > Referência dos nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Primitiva > Quadrado de pirâmide
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 1%

---


# Quadrado de pirâmide

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de quadrado da pirâmide](./3d-sdf-pyramid-square.png "Quadrado da pirâmide")

<b>Entrada:</b> Função SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma Função SDF para uma pirâmide com uma base quadrada, com height ajustável e posição base.

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
| <b>Height</b> *Flutuante* | O height Z-up do ápice da pirâmide a partir de sua base.<br><br><i>Padrão: 1</i> |
| <b>Tamanho base</b> *Flutuante* | O comprimento das bordas de base da pirâmide.<br>Todas as bordas têm o mesmo comprimento.<br><br><i>Padrão: 1</i> |
| <b>Posição base</b> *Flutuante3* | A posição do espaço global da base da pirâmide.<br><br><i>Padrão: (0, 0, 0)</i> |
| <b>P</b> *Flutuante3* | A posição do espaço mundial transformado. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
