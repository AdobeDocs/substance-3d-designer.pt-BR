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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---


# Cor segura para Albedo PBR

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-albedo-safe-color.png){width="128px"}

## Cor segura para Albedo PBR

**Entrada:** *Filtros de Material/Utilitários PBR*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Este é um nó de utilitário que faz correções se os valores de Basecolor ou Diffuse estiverem fora de um intervalo aceitável, correto para PBR. Quando definido como Metálico, o nó também tenta corrigir os valores da cor-base com base na intensidade Metálica.

Consulte também [PBR BaseColor / Metallic Validate](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic/pbr-basecolor-metallic-validate.md) para obter feedback visual sobre quais áreas podem estar erradas.

Isso é útil como uma ferramenta de correção rápida, especialmente quando ainda se está aprendendo PBR, mas não tem a intenção de ser uma medida absoluta que sempre deve ser correta.

## Parâmetros

* **Fluxo de Trabalho de PBR**: *Cor Base - Metálica, Difusa - Specular* Alterna entre dois fluxos de trabalho de PBR diferentes.
* **Tolerância**: *0.0 - 1.0* Valor de tolerância para valores fora do intervalo.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
