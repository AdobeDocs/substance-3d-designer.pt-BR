---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/basecolor-metallic-roughness-converter.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 1%

---


# Conversor de BaseColor / Metálico / Aspereza

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](basecolor-metallic-roughness-converter.resources/basecolor-metallic-roughness-converter-01.png){width="128px"}

<b>Entrada:</b> Filtros Materiais > Utilitários PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Este nó converte os mapas de Basecolor, Metallic e Roughness em diferentes saídas de modelo PBR, como o modelo de Specular/Textura reluzente. Alguns dos alvos de saída incluídos são motores de renderização bem conhecidos, como Vray, Corona, Redshift, Renderman e Arnold.

Isso é útil se você tiver gráficos ou materiais criados com um modelo de PBR, enquanto seu destino requer um modelo diferente.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Usar entrada SpecularLevel</b> <i>Falso/Verdadeiro</i> | Expõe um slot de entrada extra para a entrada SpecularLevel. Isso também é levado em conta durante a conversão. |
| <b>Destino</b> <i>Difusões/Speculares/Brilho PBR, Vray (GGX), Corona, Corona 1.6+, Redshift 1.x, Arnold 4 (AiStandard), Arnold 4 (AlSurface), RenderMan (PxrSurface)</i> | Define o modelo de destino de conversão. |
