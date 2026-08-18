---
title: Curvar (inexato)
description: Designer > Gráficos de composição de Substance > Referência dos nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Transformar > Dobrar (inexato)
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 1%

---


# Curvar (inexato)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de curva (inexato)](./3d-sdf-transform-bend.png "Curvar (inexato)")

<b>Em:</b> Função SDF > Transformar

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Inverte uma forma SDF ao redor de seu eixo Y local entre um ponto inicial e final em um ângulo.<br><br><i>Observação:</i>como esta função de transformação é inexata, artefatos podem aparecer ao renderizá-la.

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
| <b>Ângulo</b> *Flutuante* | O ângulo, em rotações, da rotação aplicada no final da dobra. |
| <b>Iniciar</b> *Flutuante* | A posição do mundo no eixo Z onde a dobra começa. Todo o volume embaixo não está dobrado. |
| <b>Fim</b> *Flutuante* | A posição do mundo no eixo Z onde a dobra termina. Todo o volume acima é girado uniformemente no ângulo especificado. |
| <b>P</b> *Flutuante3* | A posição do espaço mundial transformado. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
