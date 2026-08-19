---
title: Morph
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Operador > Morph
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 1%

---


# Morph

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de metamorfose](./3d-sdf-op-morph.png "Metamorfose")

<b>Entrada:</b> Função SDF > Operador

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Retorna a interpolação linear entre uma forma SDF de base e uma forma SDF de destino de acordo com um fator de mistura ajustável.

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
| <b>SDF Base</b> *Flutuante* | A forma SDF base. |
| <b>SDF de Destino</b> *Flutuante* | A forma SDF de destino. |
| <b>Fator de combinação</b> *Flutuante* | O fator de mistura usado para combinar as formas de entrada, onde 0 é a forma de base e 1 a forma de destino. |
