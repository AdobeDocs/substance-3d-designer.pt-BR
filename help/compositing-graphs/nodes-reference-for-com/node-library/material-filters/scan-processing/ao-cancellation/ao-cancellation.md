---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/ao-cancellation.html"
breadcrumb-title: ''
description: Use o nó Cancelamento de AO para remover a oclusão ambiente dos materiais digitalizados para o processamento de textura limpa.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > AO Cancellation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cancelamento de AO
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 1%

---


# Cancelamento de AO

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/ao-cancel.png){width="128px"}

## Cancelamento de AO

**Entrada:** *Filtros de Material/Processamento de Digitalização*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Este nó tenta remover qualquer informação de iluminação de Oclusão ambiente do mapa de Albedo (cor base), com base em uma entrada de mapa AO separada. Ele pode ser usado para garantir que as informações do seu Albedo sejam PBR corretas e na maior parte do tempo desprovidas de informações de iluminação (fortes).

Um nó útil para quando você tem um mapa de AO cozido a partir de uma malha digitalizada, ou, alternativamente, até mesmo um mapa de AO gerado a partir de informações de Height ou Normal.

## Parâmetros

* **Cancelamento de AO**: *0.0 - 1.0* Intensidade com a qual remover informações de iluminação.
* **Saturação do AO**: *0.0 - 1.0*(De)Compensação de saturação para áreas onde a iluminação é removida. Isso pode ser usado para retornar qualquer perda de cor em áreas mais escuras.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
