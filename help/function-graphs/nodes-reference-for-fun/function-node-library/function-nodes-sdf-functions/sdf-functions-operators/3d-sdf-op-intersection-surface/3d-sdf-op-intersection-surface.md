---
title: Superfície de interseção
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Operador > Superfície de interseção
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# Superfície de interseção

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de superfície de interseção](./3d-sdf-op-intersection-surface.png "Superfície de interseção")

<b>Entrada:</b> Função SDF > Operador

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Retorna a superfície da parte de uma forma SDF base que é cruzada por outra forma SDF, com thickness ajustável.

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
| <b>SDF Base</b> *Flutuante* | A forma SDF na qual a superfície resultante se baseia. |
| <b>SDF de interseção</b> *Flutuante* | A forma SDF que faz interseção com a forma SDF base. |
| <b>Thickness</b> *Flutuante* | O thickness da superfície resultante.<br><br><i>Padrão: 0,02</i> |
