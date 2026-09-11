---
title: Hélice (aprox.)
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Primitiva > Hélice (aprox.)
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# Hélice (aprox.)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Hélice (aprox.) ícone](./3d-sdf-helix.png "Hélice (aprox.)")

<b>Entrada:</b> Função SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma Função SDF para uma aproximação de uma hélice, que é uma forma formada pela varredura de um círculo ao longo de uma curva enrolada ao longo de uma curva para cima em torno de um eixo.<br><br><i>Observação:</i>Como esta Função SDF é uma aproximação, artefatos podem aparecer ao renderizá-la.

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
| <b>Raio principal</b> *Flutuante* | A distância da curva de contorno do eixo.<br><br><i>Padrão: 0,4</i> |
| <b>Raio menor</b> *Flutuante* | O raio do círculo sendo varrido ao longo da curva para formar a superfície da hélice.<br><br><i>Padrão: 0.1</i> |
| <b>Height</b> *Flutuante* | O height Z-up da hélice.<br><br><i>Padrão: 0,5</i> |
| <b>Enrolamentos</b> *Flutuante* | O número de vezes que a curva se enrola totalmente ao redor do eixo em etapas de 0,5.<br>Ou seja, quantas vezes a hélice girará dentro de um height de 0,5.<br><br><i>Padrão: 4</i> |
| <b>Posição central</b> *Flutuante3* | A posição do espaço global do pivô da hélice.<br><br><i>Padrão: (0, 0, 0)</i> |
| <b>P</b> *Flutuante3* | A posição transformada do espaço mundial. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
