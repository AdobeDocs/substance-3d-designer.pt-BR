---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-drop-shadow.html"
breadcrumb-title: ''
description: Use o nó Sombra projetada da forma para adicionar efeitos de sombra projetada às formas para criar profundidade e dimensão nas texturas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Drop Shadow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Sombra projetada da forma
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# Sombra projetada da forma

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-dropshadow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-dropshadow.png){width="128px"}

## Sombra projetada da forma (tons de cinza)

**Entrada:** *Filtros/Efeitos*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Executa o conhecido efeito “Sombra projetada” de outro software de processamento de imagens 2D, em uma máscara em preto e branco de entrada (para a versão em tons de cinza) ou imagem com transparência (para a versão colorida).

Ele difere do efeito [Sombras](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shadows-filter-node/shadows-filter-node.md) por retornar imagens com transparência total aplicada, proporcionando um efeito mais completo semelhante ao que você esperaria em outro software.

## Parâmetros

* **Ângulo**: *0.0 - 1.0*&#x200B;Ângulo de incidência da luz (falsa).
* **Distância**: *-0.5 - 0.5* Distância do menu suspenso de sombras para/se afasta da forma.
* **Tamanho**: *0.0 - 1.0* Controla o desfoque/fuzzines da sombra.
* **Propagação**: *0.0 - 1.0* Corte/limiar para o efeito de desfoque faz com que a sombra se espalhe ainda mais.
* **Opacidade**: *0.0 - 1.0*\
  Opacidade de mistura para o efeito de sombra.
* **(Sombra) Cor**: *(Valor da cor)*Tonalidade da cor a ser aplicada à sombra.
* **Cor da máscara**: *(Valor da cor) *(Somente versão em tons de cinza)**Cor sólida a ser usada para a saída mapeada de transparência.
* **A Entrada É Pré-Multiplicada**: *False/True *(Somente Versão de Cor)**Se a entrada deve ser assumida como pré-multiplicada.
* **Saída de Pré-Multiplicação**: *Falso/Verdadeiro* Se a saída deve ser pré-multiplicada.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/dropshadowex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
