---
title: Grade de atlas cor
description: Designer > Gráficos de composição de Substance > Referência dos nós para gráficos de composição de Substance > Biblioteca de nós > Gerador > Padrão > Cor de Grade de atlas
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---


# Grade de atlas cor

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de cor da Grade de atlas](grid-atlas-color.resources/grid-atlas-color.png "Cor da Grade de atlas")

<b>Entrada:</b> Gerador > Padrão

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Empacotar até 16 imagens coloridas em uma grade com tamanho XY ajustável.<br>A imagem do atlas de saída pode ser amostrada por um nó de [respingo de forma v2](../shape-splatter-v2/shape-splatter-v2.md) ou de [cor do mapeador de respingo de forma](../shape-splatter-v2-mapper-color/shape-splatter-v2-mapper-color.md).

Consulte também [Grade de atlas de tons de cinza](../grid-atlas-grayscale/grid-atlas-grayscale.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|                         |                            |
|:------------------------|:---------------------------|
| <b>Entrada 1</b> *Cor* | A entrada da imagem colorida #1. |
| <b>Entrada 2</b> *Cor* | A entrada da imagem colorida #2. |
| <b>Entrada 3</b> *Cor* | A entrada da imagem colorida #3. |
| <b>Entrada 4</b> *Cor* | A entrada da imagem colorida #4. |
| <b>Entrada 5</b> *Cor* | A entrada da imagem colorida #5. |
| <b>Entrada 6</b> *Cor* | A entrada da imagem colorida #6. |
| <b>Entrada 7</b> *Cor* | A entrada da imagem colorida #7. |
| <b>Entrada 8</b> *Cor* | A entrada da imagem colorida #8. |
| <b>Entrada 9</b> *Cor* | A entrada da imagem colorida #9. |
| <b>Entrada 10</b> *Cor* | A entrada da imagem colorida #10. |
| <b>Entrada 11</b> *Cor* | A entrada da imagem colorida #11. |
| <b>Entrada 12</b> *Cor* | A entrada da imagem colorida #12. |
| <b>Entrada 13</b> *Cor* | A entrada da imagem colorida #13. |
| <b>Entrada 14</b> *Cor* | A entrada da imagem colorida #14. |
| <b>Entrada 2</b> *Cor* | A entrada da imagem colorida #15. |
| <b>Entrada 2</b> *Cor* | A entrada da imagem colorida #16. |

<a name="outputs"></a>

## Saídas

|               |                              |
|:--------------|:-----------------------------|
| <b>Saída</b> | A grade de atlas de cores de saída. |

<a name="parameters"></a>

## Parâmetros

|                                   |                                                                                                                                                                                                                                                                                                                                                                    |
|:----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Tamanho da grade X</b> *Inteiro* | O tamanho da grade no eixo X.<br>Ou seja, o número de imagens sendo empacotadas no eixo X. |
| <b>Tamanho da grade Y</b> *Inteiro* | O tamanho da grade no eixo Y.<br>Ou seja, o número de imagens sendo empacotadas no eixo Y. |
| <b>Modo de tamanho de saída</b> *Inteiro* | O método de definir o tamanho da imagem de saída de acordo com o parâmetro base &#39;Tamanho de saída&#39; do nó:<br><br>- <b>Manual:</b> Use o tamanho como está.<br>- <b>Proporção automática:</b> Ajuste a proporção da imagem de acordo com o tamanho da grade para minimizar o tamanho da imagem. A deformação ocorrerá para grades não quadradas usando 3 linhas ou colunas, por exemplo (3, 2), (4, 3) |

## Exemplos

<img src="./grid-atlas-color.resources/grid-atlas-color-graph.png" alt="Grade de atlas nó de cores no contexto de um gráfico" style="width: 50%"><br>
<i>Grade de atlas nó de cores no contexto de um gráfico</i>