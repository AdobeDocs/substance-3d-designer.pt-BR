---
title: Cilindro
description: Designer > Gráficos de composição de Substance > Referência dos nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Primitiva > Cilindro
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 2%

---


# Cilindro

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de cilindro](./3d-sdf-cylinder.png "Cilindro")

<b>Entrada:</b> Função SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma Função SDF para um cilindro com height ajustável, raio e arredondamento de bordas.

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
| <b>Height</b> *Flutuante* | O height Z-up do cilindro de sua base.<br><br><i>Padrão: 1</i> |
| <b>Raio</b> *Flutuante* | O raio do cilindro.<br><br><i>Padrão: 0,5</i> |
| <b>Arredondamento</b> *Flutuante* | O raio dos arcos arredondados aplicados às bordas do cilindro.<br><br><i>Observação:</i> bordas sólidas podem aparecer onde os raios de arredondamento se cruzam.<br><br><i>Padrão: 0</i> |
| <b>Posição de pivô (local)</b> *Flutuante3* | A posição do espaço global do pivô local do cilindro, onde (0, 0, 0) coloca o pivô no centro do cilindro.<br><br><i>Padrão: (0, 0, -0,5)</i> |
| <b>Posição central</b> *Flutuante3* | A posição do espaço global da tabela dinâmica do cilindro.<br><br><i>Padrão: (0, 0, 0)</i> |
| <b>P</b> *Flutuante3* | A posição do espaço mundial transformado. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
