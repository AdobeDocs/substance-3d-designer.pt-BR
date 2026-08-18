---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic-validate.html"
breadcrumb-title: ''
description: Use o nó Validação metálica de PBR BaseColor para validar e corrigir a cor base e os valores metálicos dos materiais PBR.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR BaseColor  Metallic Validate
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Validação metálica de PBR BaseColor
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# PBR BaseColor / Validação metálica

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-basecolor-metallic-validate.png){width="128px"}

## PBR BaseColor / Validação metálica

**Entrada:** *Filtros de Material/Utilitários PBR*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Um nó de utilitário que gera um “Heatmap” de boa a ruim no qual os valores estão corretos ou incorretos de acordo com os padrões PBR.

É muito útil como uma ferramenta de aprendizado para a PBR, pois fornece um feedback visual muito claro sobre quais são os erros e onde eles podem ser encontrados.

Não use essa ferramenta como uma ferramenta completa, mas sempre tenha certeza de que sabe muito bem por que está quebrando todas as regras que essa ferramenta possa destacar.

## Parâmetros

* **Modo de Validação**: *Albedo, Metal, Combinado* Define se a verificação deve ser feita apenas no Albedo, Metal ou em ambos, combinados como um modo de visão geral.
* **Limite de Intervalo Escuro de Albedo**: *50 sRGB, 30 sRGB* Define o limite de Albedo inferior para 50 ou 30 sRGB. Pode diminuir ou aumentar a tolerância para áreas vermelhas.
* **Intervalo de Reflexão Metálica**: *70-100% Reflexivo, 60-100% Reflexivo* Altera o intervalo Metálico para ser considerado correto. Pode diminuir ou aumentar a tolerância para áreas vermelhas.
* **Mapa de Sobreposição**: *Falso/Verdadeiro* O modo de depuração rápida para sobrepor mapas de entrada permite um rastreamento mais rápido das áreas com problemas.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
