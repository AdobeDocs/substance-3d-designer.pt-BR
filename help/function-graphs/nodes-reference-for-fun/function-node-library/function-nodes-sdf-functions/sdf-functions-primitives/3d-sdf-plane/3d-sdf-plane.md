---
title: Plano
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Primitiva > Plano
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%

---


# Plano

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de plano](./3d-sdf-plane.png "Plano")

<b>Entrada:</b> Função SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma Função SDF para um plano de orientação, posição e tamanho ajustáveis.

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
| <b>Normal</b> *Flutuante3* | O vetor normal do plano do espaço de mundo, que controla sua orientação.<br>O vetor está normalizado.<br><br><i>Padrão: (0, 0, 1)</i> |
| <b>Tamanho</b> *Flutuante2* | O tamanho do plano em X e Y.<br><br><i>Padrão: (1, 1)</i> |
| <b>Thickness</b> *Flutuante* | O thickness do plano, aplicado em todas as direções.<br>O plano é arredondado quando o thickness é aumentado.<br><br><i>Padrão: 0</i> |
| <b>Posição central</b> *Flutuante3* | A posição do espaço global da tabela dinâmica do plano.<br><br><i>Padrão: (0, 0, 0)</i> |
| <b>P</b> *Flutuante3* | A posição transformada do espaço mundial. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
