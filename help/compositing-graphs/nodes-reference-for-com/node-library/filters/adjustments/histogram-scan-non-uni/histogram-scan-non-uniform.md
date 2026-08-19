---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan-non-uniform.html"
breadcrumb-title: ''
description: Use o nó Não uniforme de varredura do histograma para executar a varredura não uniforme do histograma para correção avançada de cores.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan Non-Uniform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Varredura de histograma não uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---


# Varredura de histograma não uniforme

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/histogram-scan-non-uniform.png){width="128px"}

## Varredura de histograma não uniforme

**Entrada:** *Filtros/Ajustes*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Versão avançada do [Varredura de histograma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md), com controles e entrada adicionais para orientar o efeito em um nível por pixel, em vez de uniformemente em toda a imagem. Pode ser usado para obter contraste e transições ainda mais complexos em máscaras.

É muito mais complexo de usar do que a [Verificação do histograma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md) comum, portanto, certifique-se de estar familiarizado antes de tentar usar a versão Não Uniforme.

## Parâmetros

### Entradas

* **Entrada**: *Entrada em tons de cinza* Resultado da origem a ser modificado.
* **Mapa de Posição**: *Entrada em Tons de Cinza* Slot de entrada para definir o parâmetro de Posição. Ativado quando “Usar entrada de posição” estiver definido como Verdadeiro. O intervalo de valores efetivo é pequeno e depende do mapa e da configuração de Contraste.
* **Mapa de Contraste**: *Entrada em Tons de Cinza* slot de entrada para definir o parâmetro de contraste. Ativado quando “Usar entrada de contraste” estiver definido como Verdadeiro. O intervalo de valor efetivo é pequeno.

### Parâmetros

* **Usar Entrada de Posição**: *Falso/Verdadeiro* Alterna o uso do slot de entrada do Mapa de Posição.
* **posição**: *0.0 - 1.0* controla ou modifica os resultados do mapa para orientar a configuração de posição.
* **Usar a Entrada de Contraste**: *Falso/Verdadeiro* Alterna o uso do slot de entrada do Mapa de Contraste.
* **contraste**: *0.0 - 1.0* controla ou modifica os resultados do mapa para orientar a configuração de contraste.

## Imagens de exemplo

</td>
</tr>
</table>
