---
title: Girar P
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Transformo > Girar página
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# Girar P

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone Girar P](./3d-sdf-transform-rotate-p.png "Girar P")

<b>Em:</b> Função SDF > Transformar

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gire o espaço mundial ao redor de um eixo em um ângulo ajustável.<br>A posição mundial de saída transformada pode ser conectada à entrada <b>P</b> da maioria das Funções SDF para defini-las neste espaço mundial transformado.<br><br>Use o auxiliar <b>Tabela dinâmica de Transformas</b> do <b>Visualizador 3D</b> para visualizar a rotação executada.<br><br><i>Dica:</i> transformas P podem ser encadeadas, mas lembre-se de que os resultados dependem da ordem de operações.

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
| <b>Ângulo</b> *Flutuante* | O ângulo, em rotações, em que o espaço do mundo é girado.<br><br>O ângulo é visualizado por um círculo no auxiliar <b>Tabela dinâmica de transformação</b> do <b>Visualizador 3D</b>. Alinhe a câmera para ver a seta do <b>Eixo</b> como o centro deste círculo e ver claramente o ângulo de sua rotação como uma fração de uma curva. |
| <b>Eixo</b> *Flutuante3* | O vetor normalizado que define o eixo ao redor do qual o espaço global é girado.<br>Por exemplo: (0, 1, 0) girará o espaço global em torno do eixo Y do ponto dinâmico.<br><br>O eixo é visualizado por uma seta no <b>auxiliar de tabela dinâmica de Transformo</b> do <b>Visualizador 3D</b>. A cor da seta é mapeada nos componentes XYZ deste vetor.<br><br><i>Padrão: (0, 1, 0)</i> |
| <b>Posição de pivô</b> *Flutuante3* | A posição do espaço global do pivô que define a origem da rotação.<br><br>O ponto dinâmico é visualizado pelo início da seta no <b>auxiliar de tabela dinâmica Transformada</b> do <b>Visualizador 3D</b>. |
| <b>P</b> *Flutuante3* | A posição transformada do espaço mundial. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
