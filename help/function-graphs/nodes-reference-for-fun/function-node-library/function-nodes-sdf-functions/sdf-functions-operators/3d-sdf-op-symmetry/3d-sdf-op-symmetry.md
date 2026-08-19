---
title: Simetria
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Função SDF > Operador > Simetria
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# Simetria

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de simetria](./3d-sdf-op-symmetry.png "simetria")

<b>Entrada:</b> Função SDF > Operador

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Inverte e duplica uma forma SDF em um plano espelhado e, em seguida, retorna a união da forma SDF base e sua(s) duplicata(s).<br>A simetria pode ser aplicada em qualquer eixo simultaneamente.

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
| <b>Posição do plano espelho</b> *Flutuante3* | A posição do espaço global do centro do plano do espelho.<br>Esta posição é compartilhada por todos os planos espelhados se a simetria for aplicada em vários eixos.<br><br><i>Padrão: (0, 0, 0)</i> |
| <b>Eixo do espelho</b> *Inteiro3* | Define os eixos do espelho desejados.<br><br>Por exemplo, (1, 0, 0) aplicará simetria no eixo X.<br><br><i>Padrão: (1, 0, 0)</i> |
| <b>Virar eixo</b> *Inteiro3* | Define quais eixos devem ser invertidos.<br><br>Por exemplo, (1, 0, 0) inverterá a direção da simetria no eixo X.<br><br><i>Padrão: (0, 0, 0)</i> |
| <b>Pré-deslocamento</b> *Flutuante3* | O deslocamento nos eixos X, Y, Z aplicado à forma antes da aplicação do operador de simetria. |
