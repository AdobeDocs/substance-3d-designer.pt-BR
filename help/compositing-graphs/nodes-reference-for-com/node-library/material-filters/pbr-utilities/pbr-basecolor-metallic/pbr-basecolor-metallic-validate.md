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
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---


# PBR BaseColor / Validação metálica

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/pbr-basecolor-metallic-validate.png){width="128px"}

<b>Entrada:</b> Filtros Materiais > Utilitários PBR

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Um nó de utilitário que gera um “Heatmap” de boa a ruim no qual os valores estão corretos ou incorretos de acordo com os padrões PBR.

É muito útil como uma ferramenta de aprendizado para a PBR, pois fornece um feedback visual muito claro sobre quais são os erros e onde eles podem ser encontrados.

Não use essa ferramenta como uma ferramenta completa, mas sempre tenha certeza de que sabe muito bem por que está quebrando todas as regras que essa ferramenta possa destacar.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Modo de Validação</b> <i>Albedo, Metal, Combinados</i> | Define se a verificação deve ser feita somente em Albedo, Metal ou em ambos, combinados como um modo de visão geral. |
| <b>Limite de Intervalo Escuro do Albedo</b> <i>50 sRGB, 30 sRGB</i> | Define o limite inferior de Albedos como 50 ou 30 sRGB. Pode diminuir ou aumentar a tolerância para áreas vermelhas. |
| <b>Intervalo de refletância metálica</b> <i>70-100% Reflexivo, 60-100% Reflexivo</i> | Altera o intervalo metálico para ser considerado correto. Pode diminuir ou aumentar a tolerância para áreas vermelhas. |
| <b>Sobrepor Mapa</b> <i>Falso/Verdadeiro</i> | O modo de depuração rápida para sobrepor mapas de entrada permite um rastreamento mais rápido das áreas com problemas. |
