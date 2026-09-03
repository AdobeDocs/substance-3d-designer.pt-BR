---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-clone-patch.html"
breadcrumb-title: ''
description: Use o nó Patch de vários Clonar para clonar e aplicar patches em vários canais de textura para reparar artefatos de material digitalizado.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Patch de vários Clonar
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 5%

---


# Patch de vários Clonar

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-clone-patch.resources/multi-clone-patch-01.png){width="128px"}

![](multi-clone-patch.resources/multi-clone-patch-02.png){width="128px"}

<b>Entrada:</b> Filtros Materiais > Processamento de materiais escaneados

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Este nó é a versão de várias entradas do [Clonar Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md). Ele vincula até oito entradas e executa exatamente a mesma operação de Clonar Patch em todas elas. Destina-se principalmente ao uso com fotos de vários ângulos, que são então combinadas com [Vários ângulos para Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) ou [Vários ângulos para Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Consulte [Patch de Clonar](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md) para obter mais informações, consulte [Patch de Clonar de Material](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md) para a versão do material.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Contagem de entradas</b> <i>1 - 8</i> | Define a quantidade de entradas que receberão a mesma operação de Patch. |
| <b>É Normal (somente para Cor)</b> <i>Falso/Verdadeiro</i> | Define se a entrada é um mapa normal e se a mesclagem deve ser tratada como tal. |
| <b>Forma</b> <i>Quadrado, Disco</i> | Define a forma do carimbo. Usado somente como base. |
| <b>Borda</b> |  |
| <b>Limite</b> <i>0.0 - 1.0</i> | Define o quanto a área mesclada deve chegar. Isso cresce em etapas ao longo das formas na área de destino; tem muito pouco efeito com fundos uniformes. |
| <b>Desfoque</b> <i>0.0 - 2.0</i> | Desfoca as bordas da área do carimbo, caso seja necessária uma transição mais suave. |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | Arredonda as bordas da forma do carimbo, criando contornos de fluxo mais suaves. |
| <b>Resolução da Grade</b> <i>1 - 11</i> | Define a resolução de qualidade da análise de mesclagem. Um valor mais alto significa uma mesclagem mais precisa. |
| <b>Transformações</b> |  |
| <b>Matriz de Origem</b> <i>(Matriz de Transformação)</i> | Transforma a origem (Dimensionamento e rotação). Não pode ser feito na tela, altere somente através destes parâmetros. |
| <b>Deslocamento de Origem</b> <i>-0.5 - 0.5</i> | Converte o local de origem. Não pode ser feito na tela, altere somente através destes parâmetros. *Este parâmetro é provavelmente o principal que você deseja alterar!* |
| <b>Matriz de Destino</b> <i>(Matriz de Transformação)</i> | Transforma o local de destino (Dimensionamento e rotação). Também pode ser feito por meio do gizmo na tela. |
| <b>Deslocamento de Destino</b> <i>-0.5 - 0.5</i> | Converte o local de destino. Também pode ser feito por meio do gizmo na tela. |
