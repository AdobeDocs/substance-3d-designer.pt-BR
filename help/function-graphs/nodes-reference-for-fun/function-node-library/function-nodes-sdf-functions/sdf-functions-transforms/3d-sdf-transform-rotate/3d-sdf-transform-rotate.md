---
title: Girar
description: Designer > Gráficos de composição de Substance > Referência dos nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Transformar > Girar
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 1%

---


# Girar

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de rotação](./3d-sdf-transform-rotate.png "Girar")

<b>Em:</b> Função SDF > Transformar

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gire uma forma SDF ao redor de um ou vários eixos de um ponto de giro ajustável, em rotações.<br>Use o <b>auxiliar de tabela dinâmica de Transformo</b> do <b>Visualizador 3D</b> para visualizar a rotação executada.

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
| <b>Ângulo</b> *Flutuante* | O ângulo, em rotações, em que a forma SDF é girada.<br><br>O ângulo é visualizado por um círculo no auxiliar <b>Tabela dinâmica de transformação</b> do <b>Visualizador 3D</b>. Alinhe a câmera para ver a seta do <b>Eixo</b> como o centro deste círculo e ver claramente o ângulo de sua rotação como uma fração de uma curva.<br><br><i>Padrão: 0</i> |
| <b>Eixo</b> *Flutuante3* | O vetor normalizado que define o eixo em torno do qual a forma SDF é girada.<br>Por exemplo: (0, 1, 0) girará a forma SDF em torno do eixo Y de seu ponto dinâmico local.<br><br>O eixo é visualizado por uma seta no <b>auxiliar de tabela dinâmica de Transformo</b> do <b>Visualizador 3D</b>. A cor da seta é mapeada nos componentes XYZ deste vetor.<br><br><i>Padrão: (0, 1, 0)</i> |
| <b>Posição de pivô</b> *Flutuante3* | A posição do espaço global da tabela dinâmica local da forma SDF, onde (0, 0, 0) coloca a tabela dinâmica no centro da forma SDF. Define a origem da rotação.<br><br>A tabela dinâmica é visualizada pelo início da seta no auxiliar <b>Transformar tabela dinâmica</b> do <b>Visualizador 3D</b>. |
| <b>P</b> *Flutuante3* | A posição transformada do espaço mundial. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
