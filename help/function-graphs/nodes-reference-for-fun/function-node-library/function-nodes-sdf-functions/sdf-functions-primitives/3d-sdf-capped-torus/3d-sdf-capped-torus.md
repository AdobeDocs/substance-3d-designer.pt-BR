---
title: Toro limitado
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Primitiva > Toro limitado
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---


# Toro limitado

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de toro limitado](./3d-sdf-capped-torus.png "Toro limitado")

<b>Entrada:</b> Função SDF > Primitiva

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Uma Função SDF para um toro arremate, onde a varredura do círculo menor ao longo de um círculo maior pode ser arrematada em um ângulo.<br>Ambos os círculos têm raios ajustáveis.

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
| <b>Raio principal</b> *Flutuante* | O raio do círculo principal ao longo do qual o círculo secundário é varrido para formar a superfície do toro.<br><br><i>Padrão: 0,5</i> |
| <b>Raio menor</b> *Flutuante* | O raio do círculo secundário sendo varrido ao longo do círculo principal para formar a superfície do toro.<br><br><i>Padrão: 0.2</i> |
| <b>Ângulo</b> *Flutuante* | O ângulo central, por sua vez, que define o arco de recorte do círculo principal ao longo do qual o círculo secundário não será varrido.<br><br><i>Padrão: 0,75</i> |
| <b>Deslocamento de ângulo</b> *Flutuante* | O deslocamento, ao longo do raio principal, do arco de aparagem ao longo do qual o círculo secundário não será varrido.<br><br><i>Padrão: 0</i> |
| <b>Simétrico</b> *Booleano* | Controla se o arco de aparo deve ser desenhado em uma ou duas direções.<br><br><i>Padrão: Verdadeiro</i> |
| <b>Posição central</b> *Flutuante3* | A posição do espaço global da tabela dinâmica do toro limitado.<br><br><i>Padrão: (0, 0, 0,5)</i> |
| <b>P</b> *Precisão decimal 3* | A posição transformada do espaço mundial. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
