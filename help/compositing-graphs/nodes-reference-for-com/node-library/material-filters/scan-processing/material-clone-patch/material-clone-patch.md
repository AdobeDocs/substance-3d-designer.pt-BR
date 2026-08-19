---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-clone-patch.html"
breadcrumb-title: ''
description: Use o nó Patch de clonagem de material para clonar e corrigir regiões de textura para reparar artefatos em materiais digitalizados.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Patch de clonagem de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---


# Patch de clonagem de material

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch-material.png){width="128px"}

## Patch de clonagem de material

**Entrada:** *Filtros de Material/Processamento de Digitalização*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Esta é a versão completa e multicanal do [Patch de clonagem](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Ele executa um patch de clone em todos e quaisquer canais de um material. [Consulte a versão original para obter mais informações!](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)

Isso é muito útil se você quiser remover um detalhe de todos os canais de um material. Gera uma saída de imagens de depuração para vários canais, para que a área de correção inteligente fique exatamente como ela é.

## Parâmetros

### Entradas

* **Máscara**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó. Pode ser alternado com o parâmetro “Máscara”.

### Parâmetros

* **Canais**
  * Ative e desative os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza.
* **Forma**: *Quadrado, Disco* Define a forma do carimbo. Usado somente como base.
* **Borda**
  * **Limite (para vários canais)**: *0.0 - 1.0* Define até onde a área mesclada deve chegar. Isso cresce em etapas, ao longo das formas na área de destino, por isso tem muito pouco efeito com fundos uniformes*.*Tenha cuidado ao alterar isso muito entre canais, pois isso pode levar a discrepâncias visuais!
  * **Desfoque**: *0.0 - 2.0* Desfoca as bordas da área do carimbo caso seja necessária uma transição mais suave.
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
