---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-crop.html"
breadcrumb-title: ''
description: Use o nó Corte múltiplo para cortar vários canais de textura simultaneamente para processar materiais digitalizados de maneira eficiente.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Corte múltiplo
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 4%

---


# Corte múltiplo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/crop-multi.png){width="128px"}

![](../../../../../../assets/crop-multi-grayscale.png){width="128px"}

<b>Entrada:</b> Filtros Materiais > Processamento de materiais escaneados

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

Esta é a versão multicanal do Crop. Ele recorta uma área de uma imagem e destina-se principalmente ao uso com fotos multiângulo, que são então combinadas com [Multiângulo para Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) ou [Multiângulo para Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Consulte o [Corte](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) original para obter mais informações.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Contagem de entradas</b> <i>1 - 8</i> | Define o número de entradas a serem processadas em paralelo. |
| <b>Tamanho de entrada</b> <i>0 - 8192</i> | Insira a resolução e as proporções das imagens. Muito importante para imagens não quadradas. |
| <b>Fundo</b> <i>(Valor da cor) / (Valor em tons de cinza)</i> | Valor uniforme do plano de fundo para as áreas não cobertas pela cultura. |
| <b>Transformar</b> <i>(Matriz de Transformação)</i> | Gira e dimensiona o resultado. O resultado pode ser modificado ao interagir diretamente com a tela. |
| <b>Deslocamento</b> <i>0.0 - 1.0</i> | Move ou traduz o resultado. O resultado pode ser modificado ao interagir diretamente com a tela. |
| <b>É Normal (somente para a versão Color)</b> <i>Falso/Verdadeiro</i> | Se a entrada deve ou não ser tratada como um mapa normal. |
