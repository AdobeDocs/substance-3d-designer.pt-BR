---
title: Deslocamento P
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Transformar > Deslocamento P
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---


# Deslocamento P

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de deslocamento P](./3d-sdf-transform-offset-p.png "Deslocamento P")

<b>Em:</b> Função SDF > Transformar

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Desloca o espaço mundial ao longo de um vetor.<br>A posição mundial transformada de saída pode ser conectada à entrada <b>P</b> da maioria das Funções SDF para defini-las neste espaço mundial transformado.<br><br><i>Dica:</i> as transformações P podem ser encadeadas, mas tenha em mente que os resultados dependem da ordem das operações.

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
| <b>Deslocamento</b> *Flutuante3* | A distância em que o espaço do mundo será deslocado nas direções X, Y e Z. |
| <b>P</b> *Flutuante3* | A posição do espaço mundial transformado. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
