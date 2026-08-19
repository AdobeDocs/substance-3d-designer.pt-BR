---
title: Arredondamento
description: Designer > Gráficos de composição de Substance > Referência dos nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Operador > Arredondamento
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 2%

---


# Arredondamento

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de arredondamento](./3d-sdf-op-rounding.png "Arredondamento")

<b>Entrada:</b> Função SDF > Operador

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Expande uma forma SDF, inflando-a e suavizando suas bordas sólidas.

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
| <b>Raio</b> *Flutuante* | O raio dos arcos arredondados aplicados às bordas da forma.<br><br><i>Observação:</i> bordas sólidas podem aparecer onde os raios de arredondamento se cruzam.<br><br><i>Padrão: 0,05</i> |
