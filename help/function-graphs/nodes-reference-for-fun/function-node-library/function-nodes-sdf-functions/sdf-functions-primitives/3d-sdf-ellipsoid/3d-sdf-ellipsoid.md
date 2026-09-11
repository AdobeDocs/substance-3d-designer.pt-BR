---
title: Elipsoide
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Primitiva > Elipsoide
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 1%

---


# Elipsoide

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de elipsoide](./3d-sdf-ellipsoid.png "elipsoide")

<b>Entrada:</b> Função SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma Função SDF para um elipsoide, que é uma forma arredondada de raio tridimensional ajustável.

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
| <b>Raio</b> *Precisão decimal 3* | O raio do elipsoide em X, Y e Z.<br><br><i>Padrão: (0,35, 0,35, 0,5)</i> |
| <b>Posição central</b> *Precisão decimal 3* | A posição do espaço global da tabela dinâmica do elipsoide.<br><br><i>Padrão: (0, 0, 0)</i> |
| <b>P</b> *Precisão decimal 3* | A posição transformada do espaço mundial. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
