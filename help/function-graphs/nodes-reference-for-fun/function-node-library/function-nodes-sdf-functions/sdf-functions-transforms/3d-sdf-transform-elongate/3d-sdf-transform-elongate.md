---
title: Elongate
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Transformar > Alongar
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 1%

---


# Elongate

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de alongamento](./3d-sdf-transform-elongate.png "Alongar")

<b>Em:</b> Função SDF > Transformar

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Alongar uma forma SDF de uma posição ajustável.<br>De forma linear e eficaz, estende o volume de uma forma SDF começando com uma fatia ajustável.

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
| <b>Alongamento</b> *Flutuante3* | O comprimento do alongamento nos eixos X, Y, Z. |
| <b>Posição central</b> *Flutuante3* | A posição do espaço global a partir do qual a forma será alongada.<br>Ou seja, a posição da fatia que está sendo alongada. |
| <b>P</b> *Flutuante3* | A posição do espaço mundial transformado. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
