---
title: Virar
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Transformo > Virar
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---


# Virar

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Inverter ícone](./3d-sdf-transform-flip.png "Inverter")

<b>Em:</b> Função SDF > Transformar

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Aplica um transformo espelhado à forma SDF de entrada.<br>Basicamente, executa uma escala negativa nos eixos selecionados.

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
| <b>Eixo do espelho</b> *Inteiro3* | Use um Integer3 para definir o eixo do espelho desejado.<br>Por exemplo: (1, 0, 0) espelhará o eixo X.<br><br><i>Padrão: (1, 0, 0)</i> |
| <b>P</b> *Flutuante3* | A posição transformada do espaço mundial. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
