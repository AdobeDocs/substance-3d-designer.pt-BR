---
title: Grade de atlas em escala de cinza
description: Designer > Gráficos de composição de Substance > Referência de nós para gráficos de composição de Substance > Biblioteca de nós > Gerador > Padrão > Tons de cinza de Grade de atlas
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---


# Grade de atlas em escala de cinza

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Ícone de Grade de atlas de tons de cinza](grid-atlas-grayscale.resources/grid-atlas-grayscale-01.png "Grade de atlas de tons de cinza")

<b>Entrada:</b> Gerador > Padrão

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Empacotar até 16 imagens em tons de cinza em uma grade com tamanho XY ajustável.<br>A imagem do atlas de saída pode ser amostrada por um nó [Shape splatter v2](../shape-splatter-v2/shape-splatter-v2.md) ou um nó [Shape splatter mapper grayscale](../shape-splatter-v2-mapper-grayscale/shape-splatter-v2-mapper-grayscale.md).

Consulte também [cor de Grade de atlas](../grid-atlas-color/grid-atlas-color.md).

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|                             |                                |
|:----------------------------|:-------------------------------|
| <b>Entrada 1</b> *Tons de cinza* | A entrada da imagem em tons de cinza #1. |
| <b>Entrada 2</b> *Tons de cinza* | A entrada da imagem em tons de cinza #2. |
| <b>Entrada 3</b> *Tons de cinza* | A entrada da imagem em tons de cinza #3. |
| <b>Entrada 4</b> *Tons de cinza* | A entrada da imagem em tons de cinza #4. |
| <b>Entrada 5</b> *Tons de cinza* | A entrada da imagem em tons de cinza #5. |
| <b>Entrada 6</b> *Tons de cinza* | A entrada da imagem em tons de cinza #6. |
| <b>Entrada 7</b> *Tons de cinza* | A entrada da imagem em tons de cinza #7. |
| <b>Entrada 8</b> *Tons de cinza* | A entrada da imagem em tons de cinza #8. |
| <b>Entrada 9</b> *Tons de cinza* | A entrada da imagem em tons de cinza #9. |
| <b>Entrada 10</b> *Tons de cinza* | A entrada da imagem em tons de cinza #10. |
| <b>Entrada 11</b> *Tons de cinza* | A entrada da imagem em tons de cinza #11. |
| <b>Entrada 12</b> *Tons de cinza* | A entrada da imagem em tons de cinza #12. |
| <b>Entrada 13</b> *Tons de cinza* | A entrada da imagem em tons de cinza #13. |
| <b>Entrada 14</b> *Tons de cinza* | A entrada da imagem em tons de cinza #14. |
| <b>Entrada 15</b> *Tons de cinza* | A entrada da imagem em tons de cinza #15. |
| <b>Entrada 16</b> *Tons de cinza* | A entrada da imagem em tons de cinza #16. |

<a name="outputs"></a>

## Saídas

|               |                                  |
|:--------------|:---------------------------------|
| <b>Saída</b> | A grade de atlas em tons de cinza de saída. |

<a name="parameters"></a>

## Parâmetros

|                                   |                                                                                                                                                                                                                                                                                                                                                                    |
|:----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>Tamanho da grade X</b> *Inteiro* | O tamanho da grade no eixo X.<br>Ou seja, o número de imagens sendo empacotadas no eixo X. |
| <b>Tamanho da grade Y</b> *Inteiro* | O tamanho da grade no eixo Y.<br>Ou seja, o número de imagens sendo empacotadas no eixo Y. |
| <b>Modo de tamanho de saída</b> *Inteiro* | O método de definir o tamanho da imagem de saída de acordo com o parâmetro base &#39;Tamanho de saída&#39; do nó:<br><br>- <b>Manual:</b> Use o tamanho como está.<br>- <b>Proporção automática:</b> Ajuste a proporção da imagem de acordo com o tamanho da grade para minimizar o tamanho da imagem. A deformação ocorrerá para grades não quadradas usando 3 linhas ou colunas, por exemplo (3, 2), (4, 3) |

## Exemplos

<img src="./grid-atlas-grayscale.resources/grid-atlas-grayscale-02.png" alt="Grade de atlas nó de escala de cinza no contexto de um gráfico" style="width: 50%"><br>
<i>Grade de atlas nó de tons de cinza no contexto de um gráfico</i>
