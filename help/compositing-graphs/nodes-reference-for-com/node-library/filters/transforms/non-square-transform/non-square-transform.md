---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-square-transform.html"
breadcrumb-title: ''
description: Use o nó Transformação não quadrada para aplicar transformações a texturas não quadradas com dimensionamento independente de X e Y.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Square Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformação não quadrada
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# Transformação não quadrada

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

## Transformação não quadrada (tons de cinza)

**Entrada:** *Filtros/Transformações*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Versão não segura para quadrados de [Transformar 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md). Detecta automaticamente proporções não quadradas e pode transformar imagens de entrada quadradas em uma tela não quadrada.

Certifique-se de entender completamente os [Parâmetros de Gráfico](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)para fazer o melhor uso deste nó, pois você precisará definir algumas configurações corretamente:

* O tamanho do seu **gráfico** não deve ser quadrado, caso contrário, não há necessidade para este nó.
* Defina o Tamanho de Saída do **nó** de Transformação Não Quadrada como “*Relativo ao Pai*”.
* Defina o modo de divisão em blocos gráficos do **nó** como “*Sem divisão em blocos gráficos*” se desejar transformar apenas a entrada em uma única posição.

## Parâmetros

* **Modo Lado a Lado**: *Automático, Manual* Habilite ou não compensações automáticas não quadradas.
* **Bloco**: *1 - 16* Acessível somente quando o Modo Bloco está definido como Manual. Permite alterar a escala de maneira segura para a divisão em blocos gráficos.
* **Deslocamento**: *0.0 - 1.0*\
  Move ou traduz o resultado. Clique duas vezes no controle deslizante para inserir valores negativos.
* **Rotação**: *0.0 - 1.0* Gira a imagem de entrada.
* **Rotação segura (somente quadriculados)**: *Falso/Verdadeiro* Ajusta aos valores seguros para manter a nitidez dos pixels.
* **Cor do plano de fundo**: *(valor da cor)*Cor do plano de fundo para preencher a imagem. Visível somente quando o [Modo de Enquadramento em Parâmetros Básicos estiver definido como “*Sem Enquadramento*”](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md).

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/nonsquare-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
