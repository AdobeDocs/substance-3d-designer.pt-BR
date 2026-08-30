---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-crop.html"
breadcrumb-title: ''
description: Use o nó Corte de material para cortar regiões de textura de materiais digitalizados para isolar áreas de interesse específicas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Corte de material
user-guide-description: ''
user-guide-title: ''
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# Corte de material

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-crop.resources/crop-material.png){width="128px"}

<b>Entrada:</b> Filtros Materiais > Processamento de materiais escaneados

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Este nó é a versão de material completo multicanal de [Corte](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md). Ele permite que você execute uma operação de corte em qualquer e todos os canais de material em paralelo.

>[!NOTE]
>
> [Veja o](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) [Corte](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) [original para obter mais informações.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Canais</b> | Ative e desative os canais de material neste grupo ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza, por exemplo. |
| <b>Tamanho de entrada</b> <i>0 - 8192</i> | Resolução e proporções da imagem de entrada. Muito importante para imagens não quadradas. |
| <b>Fundo</b> <i>(Valor da cor) / (Valor em tons de cinza)</i> | Valor uniforme do plano de fundo para as áreas não cobertas pela cultura. |
| <b>Transformar</b> <i>(Matriz de Transformação)</i> | Gira e dimensiona o resultado. O resultado pode ser modificado interagindo diretamente com a tela. |
| <b>Deslocamento</b> <i>0.0 - 1.0</i> | Move ou traduz o resultado. O resultado pode ser modificado interagindo diretamente com a tela. |
