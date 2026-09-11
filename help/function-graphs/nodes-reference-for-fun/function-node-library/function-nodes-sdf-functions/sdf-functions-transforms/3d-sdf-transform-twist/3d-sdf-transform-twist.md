---
title: Torção (inexata)
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Transformo > Torção (inexato)
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 1%

---


# Torção (inexata)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de torção (inexato)](./3d-sdf-transform-twist.png "Torção (inexato)")

<b>Em:</b> Função SDF > Transformar

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Gire uma forma SDF ao redor de seu eixo Z local entre um ponto inicial e final, em um ângulo ajustável.<br><br><i>Observação:</i>como esta função de transformação é inexata, artefatos podem aparecer ao renderizá-la.

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
| <b>FDS</b> *Precisão decimal* | A forma SDF de entrada. |
| <b>Ângulo</b> *Precisão decimal* | Ângulo, em rotações, da rotação aplicada no fim da torção. |
| <b>Iniciar</b> *Precisão decimal* | A posição mundial no eixo Z onde a torção começa. Todo o volume embaixo não está torcido. |
| <b>Fim</b> *Precisão decimal* | A posição mundial no eixo Z onde a torção termina. Todo o volume acima é girado uniformemente no ângulo especificado. |
| <b>P</b> *Precisão decimal 3* | A posição transformada do espaço mundial. Use esta entrada para aplicar transformações adicionais usando os nós <b>Deslocamento P</b> e <b>Girar P</b>.<br><br><i>Padrão: a posição do espaço mundial não transformado.</i> |
