---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/glow.html"
breadcrumb-title: ''
description: Use o nó Brilho para adicionar efeitos de brilho às texturas para criar aparências de materiais luminosos e emissivos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Brilho
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---


# Brilho

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/glow-greyscale.png){width="128px"}

![](../../../../../../assets/glow-3.png){width="128px"}

## Brilho

**Entrada:** *Filtros/Efeitos*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Executa um efeito do tipo “Brilho externo”, como visto em outros softwares populares de edição de imagens. Basicamente, adiciona um contorno de gradiente esmaecido ao redor da entrada.

Lembre-se de que esse recurso não deve funcionar para imagens com canais de Alpha, como seria de esperar. Mesmo a versão colorida espera apenas máscaras binárias, pretas e brancas como entrada; ela só permite o uso de um brilho colorido. Se você está atrás de uma versão que funcione em imagens com transparência, consulte [Brilho da forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-glow/shape-glow.md).

Importante: certifique-se de usar a versão apropriada para sua entrada! Use “Brilho” para entradas de cor ou “Escala de cinza brilhante” para entradas de tons de cinza.

## Parâmetros

* **Quantidade de brilho**: *0.0 - 1.0* Opacidade global para o efeito de brilho.
* **Limpar Quantidade**: *0.0 - 1.0* Limite para quando cortar o efeito de brilho. Útil para áreas semitransparentes.
* **Tamanho do Brilho**: *0.0 - 20.0* Controla até onde o efeito de brilho alcança.
* **Cor do brilho**: *(Valor da cor) (Somente versão da cor)*Define a cor do efeito de brilho.

## Imagens de exemplo

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/glow-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
