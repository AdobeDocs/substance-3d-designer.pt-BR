---
title: Cilindro 2 pontos
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Primitiva > Cilindro 2 pontos
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---


# Cilindro 2 pontos

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de 2 pontos do cilindro](./3d-sdf-cylinder-2-points.png "Cilindro 2 pontos")

<b>Entrada:</b> Função SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma Função SDF para um cilindro de raio ajustável definido pelas posições de seus discos inicial e final.

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
| <b>Iniciar</b> *Flutuante3* | A posição do disco de início do cilindro.<br><br><i>Padrão: (0, 0, 0)</i> |
| <b>Fim</b> *Flutuante3* | A posição do disco final do cilindro.<br><br><i>Padrão: (0, 0, 1)</i> |
| <b>Raio</b> *Flutuante* | O raio do cilindro.<br><br><i>Padrão: 0,25</i> |
| <b>P</b> *Flutuante3* | A posição do espaço mundial transformado. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
