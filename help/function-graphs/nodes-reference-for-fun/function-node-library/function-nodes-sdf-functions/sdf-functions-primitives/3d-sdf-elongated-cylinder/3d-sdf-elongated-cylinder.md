---
title: Cilindro alongado
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Primitivo > Cilindro alongado
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 1%

---


# Cilindro alongado

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de cilindro alongado](./3d-sdf-elongated-cylinder.png "Cilindro alongado")

<b>Entrada:</b> Função SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma Função SDF para um cilindro alongado de comprimento ajustável, raio e arredondamento de bordas.<br>O cilindro alongado é o resultado da conexão de dois cilindros.

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
| <b>Height</b> *Flutuante* | O height Z-up dos cilindros de início e de término de sua base.<br><br><i>Padrão: 0,5</i> |
| <b>Raio</b> *Flutuante* | O raio dos cilindros de início e de término.<br><br><i>Padrão: 0,5</i> |
| <b>Arredondamento</b> *Flutuante* | O raio dos arcos arredondados aplicados às bordas do cilindro alongado.<br><br><i>Observação:</i> bordas sólidas podem aparecer onde os raios de arredondamento se cruzam.<br><br><i>Padrão: 0</i> |
| <b>Posição central</b> *Flutuante3* | A posição do espaço global da tabela dinâmica do cilindro alongado.<br><br><i>Padrão: (0, 0, 0)</i> |
| <b>Distância de alongamento</b> *Flutuante* | A distância ao longo da qual o cilindro inicial é alongado.<br>Ou seja, a distância entre os centros dos cilindros inicial e final.<br><br><i>Padrão: 0,5</i> |
| <b>P</b> *Flutuante3* | A posição do espaço mundial transformado. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
