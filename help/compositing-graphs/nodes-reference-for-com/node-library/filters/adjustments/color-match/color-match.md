---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-match.html"
breadcrumb-title: ''
description: Use o nó Correspondência de cores para corresponder cores entre texturas para criar paletas de cores consistentes e harmonizar texturas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color Match
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Correspondência de cores
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 1%

---


# Correspondência de cores

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-match-3.png){width="128px"}

## Correspondência de cores

**Entrada:** *Filtros/Ajustes*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Tenta corresponder o intervalo de *Cores de Origem* definido a um intervalo de *Cores de Destino*, com suporte para slots de entrada para definir Origem e Destino.

Para versões mais simples, consulte [Substituir intervalo de cores](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color-range/replace-color-range.md) ou [Substituir cor](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color/replace-color.md).

## Parâmetros

### Entradas

* **Entrada**: entrada *colorida*\
  Entrada principal a ser modificada para resultado.
* **Cor De Origem**: *Entrada De Cores*\
  Slot de entrada para cor de Origem, usado somente quando o &#39;Modo de Cor de Origem&#39; está definido como *Entrada*.
* **Cor de Destino**: *Entrada de Cores* slot de entrada para a cor de Destino, usado somente quando &#39;Modo de Cores de Destino&#39; está definido como *Entrada*.

### Parâmetros

* **Modo de Cores de Origem**: *Média, Parâmetro, Entrada* Define se a Cor de Origem é definida calculando a média da imagem de entrada, definindo um parâmetro ou usando um slot de entrada.
* **Cor de origem**: *(valor da cor)* Se o Modo da Cor de Origem estiver definido como *Parâmetro*, esse parâmetro determinará a Cor de Origem.
* **Modo de Cores de Destino**: *Parâmetro, Entrada de Imagem* Define se a Cor de Origem é definida calculando a média da imagem de entrada, definindo um parâmetro ou usando um slot de entrada.
* **Cor de Destino**: *(valor da Cor)* Se o Modo da Cor de Destino estiver definido como *Parâmetro*, esse parâmetro determinará a Cor de Destino.
* **Variação de Cor Personalizada**: False/True\
  Ativa uma variação de cor adicional.
* **Variação de cor**\
  Define as variações de Matiz, Crominância ou Luminância para o resultado, se ativadas.
* **Usar máscara**: *Falso/Verdadeiro*\
  Alterna o uso de Entrada ou Saída de máscara, dependendo do Modo de máscara abaixo.
* **Modo de máscara**: *Parâmetro, Entrada* O modo de parâmetro gera uma máscara detalhando como a cor foi alterada. O modo de entrada permite que uma máscara controle a intensidade do efeito Correspondência de cores.
* **Máscara**\
  Gera a saída de uma máscara mostrando onde exatamente o efeito Correspondência de cores foi aplicado, com controles adicionais para suavizar e desfocar a máscara resultante.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
