---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/basecolor-metallic-roughness-converter.html"
breadcrumb-title: ''
description: Use o nó Conversor de aspereza metálica de BaseColor para converter entre diferentes formatos de material PBR e fluxos de trabalho.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > BaseColor  Metallic  Roughness converter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Conversor de aspereza metálica de BaseColor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# Conversor de BaseColor / Metálico / Aspereza

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-convert.png){width="128px"}

## Conversor de BaseColor / Metálico / Aspereza

**Entrada:** *Filtros de Material/Utilitários PBR*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Este nó converte os mapas de Basecolor, Metallic e Roughness em diferentes saídas de modelo PBR, como o modelo de Specular/Textura reluzente. Alguns dos alvos de saída incluídos são motores de renderização bem conhecidos, como Vray, Corona, Redshift, Renderman e Arnold.

Isso é útil se você tiver gráficos ou materiais criados com um modelo de PBR, enquanto seu destino requer um modelo diferente.

## Parâmetros

* **Usar entrada SpecularLevel**: *False/True* Expõe um slot de entrada extra para a entrada SpecularLevel. Isso também é levado em conta durante a conversão.
* ***Destino**: *PBR Difusa/Specular/Brilho, Vray (GGX), Corona, Corona 1.6+, Redshift 1.x, Arnold 4 (AiStandard), Arnold 4 (AlSurface), RenderMan (PxrSurface)**Define o modelo de destino de conversão.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
