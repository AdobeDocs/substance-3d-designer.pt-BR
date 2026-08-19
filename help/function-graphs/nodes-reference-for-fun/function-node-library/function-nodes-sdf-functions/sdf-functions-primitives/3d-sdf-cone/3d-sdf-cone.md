---
title: Cone
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Primitiva > Cone
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---


# Cone

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de cone](./3d-sdf-cone.png "Cone")

<b>Entrada:</b> Função SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma Função SDF para um cone de height, raio e posição ajustáveis.

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
| <b>Raio</b> *Flutuante* | O raio da base do cone.<br><br><i>Padrão: 0,5</i> |
| <b>Height</b> *Flutuante* | O height Z-up do ápice do cone a partir de sua base.<br><br><i>Padrão: 1</i> |
| <b>Posição central</b> *Flutuante3* | A posição do espaço global da tabela dinâmica do cone.<br><br><i>Padrão: (0, 0, 0)</i> |
| <b>P</b> *Flutuante3* | A posição do espaço mundial transformado. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
