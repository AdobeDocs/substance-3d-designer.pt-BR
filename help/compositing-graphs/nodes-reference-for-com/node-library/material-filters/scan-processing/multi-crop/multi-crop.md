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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---


# Corte múltiplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/crop-multi.png){width="128px"}

![](../../../../../../assets/crop-multi-grayscale.png){width="128px"}

## Corte múltiplo (tons de cinza)

**Entrada:** *Filtros de Material/Processamento de Digitalização*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Esta é a versão multicanal do Crop. Ele recorta uma área de uma imagem e destina-se principalmente ao uso com fotos multiângulo, que são então combinadas com [Multiângulo para Albedo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md) ou [Multiângulo para Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md).

>[!NOTE]
>
> Consulte o [Corte](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) original para obter mais informações.

## Parâmetros

### Parâmetros

* **Contagem de entradas**: *1 - 8* Define o número de entradas a serem processadas em paralelo.
* **Tamanho de entrada**: *0 - 8192* Resolução e proporções das imagens de entrada. Muito importante para imagens não quadradas.
* **Plano de fundo**: *(Valor da cor) / (Valor da escala de cinza)*Valor uniforme do plano de fundo para áreas não cobertas pelo corte.
* **Transformar**: *(Matriz de Transformação)*\
  Gira e dimensiona o resultado. O resultado pode ser modificado ao interagir diretamente com a tela.
* **Deslocamento**: *0.0 - 1.0*\
  Move ou traduz o resultado. O resultado pode ser modificado ao interagir diretamente com a tela.
* **É Normal (somente para a versão Color)**: *Falso/Verdadeiro* Se a entrada deve ou não ser tratada como um Mapa Normal.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
