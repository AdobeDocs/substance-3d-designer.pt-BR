---
title: Camiseta da União
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Operador > chanfro de união
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# Camiseta da União

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de chanfro de união](./3d-sdf-op-union-chamfer.png "chanfro de união")

<b>Entrada:</b> Função SDF > Operador

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Retorna os volumes adicionados de duas formas SDF, com um volume adicional de raio ajustável ao longo das bordas de sua interseção.

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
| <b>SDF 1</b> *Flutuante* | A primeira forma SDF. |
| <b>SDF 2</b> *Flutuante* | A segunda forma SDF. |
| <b>Raio</b> *Flutuante* | O raio do volume adicionado ao longo das bordas da interseção de formas.<br><br><i>Padrão: 0</i> |
