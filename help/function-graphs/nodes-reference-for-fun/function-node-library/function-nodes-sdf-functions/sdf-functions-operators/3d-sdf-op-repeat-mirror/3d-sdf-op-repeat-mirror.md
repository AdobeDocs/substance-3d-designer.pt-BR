---
title: Repetir intervalo espelhado
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Operador > Intervalo de espelhamento de repetição
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---


# Repetir intervalo espelhado

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de repetição de intervalo espelhado](./3d-sdf-op-repeat-mirror.png "Repetição de intervalo espelhado")

<b>Entrada:</b> Função SDF > Operador

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Reflete e duplica uma forma SDF várias vezes em um espaçamento regular nos eixos X, Y e Z positivos ou negativos.<br>Sempre que este operador repete uma forma, ele também a espelha. Isso resulta visualmente em uma alternância entre a orientação original da forma e uma cópia invertida.

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
| <b>Valor +</b> *Inteiro3* | A quantidade de duplicações nos eixos X, Y, Z positivos.<br><br><i>Padrão: (2, 0, 0)</i> |
| <b>Valor -</b> *Inteiro3* | A quantidade de duplicações nos eixos X, Y, Z negativos.<br><br><i>Padrão: (2, 0, 0)</i> |
| <b>Espaçamento</b> *Flutuante3* | O espaço de mundo entre cada duplicata.<br><br>O espaçamento é visualizado por um auxiliar cúbico, que é o tamanho do espaço entre as duplicatas nas direções X, Y e Z. O espaçamento começa na <b>Posição de origem</b> e é aumentado simetricamente a partir dela.<br><br><i>Padrão: (2, 2, 2)</i> |
| <b>Posição de origem</b> *Flutuante3* | Define o centro da forma SDF que será duplicada.<br><br>A posição de origem é visualizada pela posição central do auxiliar cúbico.<br><br><i>Padrão: (0, 0, 0)</i> |
| <b>P</b> *Flutuante3* | A posição transformada do espaço mundial. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
