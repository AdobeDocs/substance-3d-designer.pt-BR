---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/snow-cover.html"
breadcrumb-title: ''
description: Use o nó Capa de Snow para adicionar efeitos de acumulação de neve a materiais com base no ângulo e na posição da superfície.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Snow Cover
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Snow Cover
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 8%

---


# Snow Cover

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/snow-cover.png){width="128px"}

<b>Em:</b> Filtros Materiais > Efeitos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Efeito multifuncional para adicionar neve acumulada em um material completo. Altamente depende de um mapa de altura bom e de alta qualidade, como de uma varredura de fotos. O resultado deve ser PBR-correto.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Máscara (opcional)</b> <i>Entrada em tons de cinza</i> | Slot de máscara usado para mascarar os efeitos do nó. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Canais</b> | Ative e desative os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza. |
| <b>Snow novo</b> <i>0.0 - 1.0</i> | Define a quantidade de neve em áreas elevadas. O resultado está vinculado ao parâmetro Snow derretido. |
| <b>Snow derretido</b> <i>0.0 - 1.0</i> | Define a quantidade de neve derretida nos cantos inferiores. |
| <b>Compilação</b> <i>0.0 - 1.0</i> | Afeta principalmente a saída do Height, determina o efeito de empilhamento do height. |
| <b>Smoothness</b> <i>0.0 - 1.0</i> | Define a suavização dos detalhes do height por acumulação de neve. |
| <b>Intensidade de Flocos</b> <i>0.0 - 1.0</i> | Afeta principalmente o Normalmap, a intensidade dos detalhes do flake. |
