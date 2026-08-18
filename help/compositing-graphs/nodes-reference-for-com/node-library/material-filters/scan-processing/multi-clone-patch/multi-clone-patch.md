---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-clone-patch.html"
breadcrumb-title: ''
description: Use o nó Patch de Clonagem Múltipla para clonar e aplicar patch em vários canais de textura para reparar artefatos de material digitalizado.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Patch de vários clones
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---


# Patch de vários clones

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch-multi.png){width="128px"}

![](../../../../../../assets/clone-patch-multi-grayscale.png){width="128px"}

## Patch de vários clones (tons de cinza)

**Entrada:** *Filtros de Material/Processamento de Digitalização*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Este nó é a versão de várias entradas do [Patch de clone](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Ele vincula até oito entradas e executa exatamente a mesma operação de Patch de clone em todas elas. Destina-se principalmente ao uso com fotos de vários ângulos, que são então combinadas com [Vários ângulos para Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) ou [Vários ângulos para Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Consulte [Patch de clonagem](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md) para obter mais informações, consulte [Patch de clonagem de material](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md) para a versão do material.

## Parâmetros

### Parâmetros

* **Contagem de Entrada**: *1 - 8* Define a quantidade de entradas que receberão a mesma operação de Patch.
* **É Normal (somente para Cor)**: **Falso/Verdadeiro** Define se a entrada é um Mapa Normal e se a mesclagem deve ser tratada como tal.
* **Forma**: **Quadrado, Disco** Define a forma do carimbo. Usado somente como base.
* **Borda**
  * **Limite**: *0.0 - 1.0* Define até onde a área mesclada deve chegar. Isso cresce em etapas ao longo das formas na área de destino; tem muito pouco efeito com fundos uniformes*.*
  * **Desfoque**: *0.0 - 2.0* Desfoca as bordas da área do carimbo, caso seja necessária uma transição mais suave.
  * **Smoothness**: *0.0 - 2.0* Arredonda as bordas da forma do carimbo, criando contornos mais suaves.
  * **Resolução da grade**: *1 - 11* Define a resolução de qualidade da análise de mesclagem. Um valor mais alto significa uma mesclagem mais precisa.
* **Transformações**
  * **Matriz de Origem**: *(Matriz de Transformação)*Transforma a origem (Escala e Rotação). Não pode ser feito na tela, altere somente através destes parâmetros.
  * **Deslocamento de Origem**: *-0.5 - 0.5* Converte o local de origem. Não pode ser feito na tela, altere somente através destes parâmetros. *Este parâmetro é provavelmente o principal que você deseja alterar!*
  * **Matriz de Destino**: *(Matriz de Transformação)*Transforma o local de destino (Escala e Rotação). Também pode ser feito por meio do gizmo na tela.
  * **Deslocamento de Destino**: *-0.5 - 0.5* Converte o local de destino. Também pode ser feito por meio do gizmo na tela.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
