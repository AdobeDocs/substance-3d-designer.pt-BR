---
title: Cone de arremate 2 pontos
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Primitiva > Cone limitado de 2 pontos
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---


# Cone de arremate 2 pontos

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de cone de 2 pontos com arremate](./3d-sdf-capped-cone-2-points.png "Cone de 2 pontos com arremate")

<b>Entrada:</b> Função SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma Função SDF para um cone limitado definido pelas posições de sua base e topo.<br>A base e o topo têm raios ajustáveis.

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
| <b>Posição base</b> *Flutuante3* | A posição da base do cone limitado.<br><br><i>Padrão: (0, 0, 0)</i> |
| <b>Posição superior</b> *Flutuante3* | A posição da parte superior do cone limitado.<br><br><i>Padrão: (0, 0, 1)</i> |
| <b>Base do raio</b> *Flutuante* | O raio da base do cone limitado.<br><br><i>Padrão: 0,5</i> |
| <b>Raio superior</b> *Flutuante* | O raio da parte superior do cone limitado.<br><br><i>Padrão: 0,2</i> |
| <b>P</b> *Flutuante3* | A posição transformada do espaço mundial. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
