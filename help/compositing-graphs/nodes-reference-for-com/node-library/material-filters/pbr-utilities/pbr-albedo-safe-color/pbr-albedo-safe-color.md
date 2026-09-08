---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-albedo-safe-color.html"
breadcrumb-title: ''
description: Use o nó Cor de segurança de Albedo PBR para garantir que as cores do albedo estejam dentro de intervalos fisicamente plausíveis para materiais PBR.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Albedo Safe Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cor segura para Albedo PBR
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Cor segura para Albedo PBR

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/pbr-albedo-safe-color.png){width="128px"}

<b>Entrada:</b> Filtros Materiais > Utilitários PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Este é um nó de utilitário que faz correções se os valores de Basecolor ou Diffuse estiverem fora de um intervalo aceitável, correto para PBR. Quando definido como Metálico, o nó também tenta corrigir os valores da cor-base com base na intensidade Metálica.

Consulte também [PBR BaseColor / Metallic Validate](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic/pbr-basecolor-metallic-validate.md) para obter feedback visual sobre quais áreas podem estar erradas.

Isso é útil como uma ferramenta de correção rápida, especialmente quando ainda se está aprendendo PBR, mas não tem a intenção de ser uma medida absoluta que sempre deve ser correta.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Fluxo de trabalho de PBR</b> <i>Cor de base - Metálica, Difusão - Specular</i> | Alterna entre dois fluxos de trabalho de PBR diferentes. |
| <b>Tolerância</b> <i>0.0 - 1.0</i> | Valor de tolerância para valores fora do intervalo. |
