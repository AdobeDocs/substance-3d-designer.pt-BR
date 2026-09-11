---
title: Cápsula
description: Designer > Gráficos de composição de Substance > Referência dos nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Primitivo > Cápsula
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 2%

---


# Cápsula

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de cápsula](./3d-sdf-capsule.png "Cápsula")

<b>Entrada:</b> Função SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma Função SDF para uma cápsula de comprimento e raio ajustáveis.<br>A cápsula é o resultado de unir duas esferas.

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
| <b>Iniciar</b> *Flutuante3* | A posição da esfera inicial.<br><br><i>Padrão: (0, 0, 0)</i> |
| <b>Fim</b> *Flutuante3* | A posição da esfera final.<br><br><i>Padrão: (0, 0, 1)</i> |
| <b>Raio</b> *Flutuante* | O raio das esferas inicial e final.<br><br><i>Padrão: 0,25</i> |
| <b>Iniciar/terminar na ponta</b> *Booleano* | Controla se as posições <b>Início</b> e <b>Fim</b> devem estar nas extremidades das esferas.<br>Ou seja, controla se o height da cápsula deve incluir o raio das esferas.<br><br><i>Padrão: falso</i> |
| <b>Posição central</b> *Flutuante3* | A posição do espaço global da tabela dinâmica da cápsula.<br><br><i>Padrão: (0, 0, 0)</i> |
| <b>P</b> *Flutuante3* | A posição transformada do espaço mundial. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
