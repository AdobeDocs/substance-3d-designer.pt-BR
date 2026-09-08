---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/material-height-blend.html"
breadcrumb-title: ''
description: Use o nó Mesclagem de Height de material para mesclar vários materiais com base em mapas de height para criar efeitos de material em camadas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Material Height Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mesclagem de Height de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 4%

---


# Mesclagem de Height de material

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/material-height-blend.png){width="128px"}

<b>Em:</b> Filtros Materiais > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Este nó é uma versão mais avançada da [Mesclagem de Heights](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/height-blend/height-blend.md) que mescla dois materiais com base em seus Heightmaps. Não há uma máscara definida pelo usuário, portanto, você deve ter dois mapas de altura, um para cada material, dos quais pelo menos um não é um valor uniforme.

Isso pode ser útil para combinar dois materiais diferentes e de alta qualidade sem uma máscara de mesclagem de alta qualidade.

Se você quiser se misturar na água ou na neve, os nós [Snow Cover](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md) e [Water Level](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md) estão disponíveis.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Canais</b> | Ative e desative os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza. |
| <b>Deslocamento de Height</b> <i>0.0 - 1.0</i> | Desloca mapas de altura para que o nível de mesclagem seja movido ao longo do eixo do height. Esse é o principal controle da mesclagem. |
| <b>Contraste</b> <i>0.0 - 1.0</i> | Ajusta o contraste da mesclagem, torna as transições mais nítidas. |
| <b>Modo</b> <i>height balanceado, prioridade de height inferior</i> |  |
| <b>Opacidade</b> <i>0.0 - 1.0</i> | Mesclando a Opacidade do height de primeiro plano, ela aparece ou desaparece gradualmente. |
| <b>Correspondência de Albedo</b> <i>0.0 - 1.0</i> | A quantidade de correspondência de cor interna a ser executada entre cores de Albedo. |
