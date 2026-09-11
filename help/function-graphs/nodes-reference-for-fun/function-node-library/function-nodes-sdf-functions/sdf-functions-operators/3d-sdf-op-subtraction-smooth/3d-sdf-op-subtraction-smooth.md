---
title: 'Subtração suave '
description: 'Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Operador > Suavização de subtração '
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 1%

---


# Subtração suave

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone suave de subtração](./3d-sdf-op-subtraction-smooth.png "Subtração suave ")

<b>Entrada:</b> Função SDF > Operador

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Subtrai o volume da forma SDF 1 da forma SDF 2, com suavização ajustável aplicada na interseção dos dois.

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
| <b>SDF 1</b> *Precisão decimal* | A forma SDF sendo subtraída de. |
| <b>SDF 2</b> *Precisão decimal* | A forma SDF que está sendo subtraída da forma SDF 1. |
| <b>Smoothness</b> *Precisão decimal* | A suavização aplicada na interseção das duas formas.<br><br><i>Observação:</i> bordas sólidas podem aparecer onde os raios de suavização se cruzam. |
