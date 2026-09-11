---
title: Torus
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Primitiva > Toro
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---


# Torus

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de toro](./3d-sdf-torus.png "Toro")

<b>Entrada:</b> Função SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma Função SDF para um toro, que é uma forma formada pela varredura de um círculo menor ao longo de um círculo maior.<i>Ambos os círculos têm raios ajustáveis.

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
| <b>Raio principal</b> *Flutuante* | O raio do círculo ao longo do qual o disco secundário é varrido para formar a superfície do toro.<br><br><i>Padrão: 0,5</i> |
| <b>Raio menor</b> *Flutuante* | O raio do círculo sendo varrido ao longo do círculo principal para formar a superfície do toro.<br><br><i>Padrão: 0.2</i> |
| <b>Posição central</b> *Flutuante3* | A posição do espaço global da tabela dinâmica do toro.<br><br><i>Padrão: (0, 0, 0)</i> |
| <b>P</b> *Flutuante3* | A posição transformada do espaço mundial. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
