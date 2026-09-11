---
title: Rock
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Primitiva > Rock
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---


# Rock

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de pedra](./3d-sdf-rock.png "Rock")

<b>Entrada:</b> Função SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma Função SDF para uma forma de rocha paramétrica e aleatória, construída com Funções SDF.

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
| <b>Máx. facetas</b> *Inteiro* | O número máximo de facetas da rocha (até 32).<br><br><i>Padrão: 8</i> |
| <b>Smoothness</b> *Flutuante* | O raio dos arcos arredondados aplicados às bordas da rocha.<br><br><i>Padrão: 0</i> |
| <b>Aleatoriedade</b> *Flutuante* | Treme a orientação e a distância das faces em relação ao centro.<br>Como resultado, valores maiores resultam em uma rocha menor.<br><br><i>Padrão: 0</i> |
| <b>Semente</b> *Flutuante* | Propagação do parâmetro <b>Aleatoriedade</b>.<br><br><i>Padrão: 0</i> |
| <b>Escala</b> *Flutuante* | Escala global da forma rochosa.<br>Aplicado após <b>Aleatoriedade</b> e antes de <b>Smoothness</b>.<br><br><i>Padrão: 0,5</i> |
| <b>Posição central</b> *Flutuante3* | A posição do espaço global do pivô da rocha.<br><br><i>Padrão: (0, 0, 0,5)</i> |
| <b>P</b> *Flutuante3* | A posição transformada do espaço mundial. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><i>Padrão: a posição do espaço mundial não transformado.</i> |
