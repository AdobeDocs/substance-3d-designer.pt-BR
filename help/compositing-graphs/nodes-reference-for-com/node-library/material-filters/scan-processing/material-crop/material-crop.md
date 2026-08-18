---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-crop.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---


# Corte de material

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/crop-material.png){width="128px"}

## Corte de material

**Entrada:** *Filtros de Material/Processamento de Digitalização*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Este nó é a versão de material completo multicanal de [Corte](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md). Ele permite que você execute uma operação de corte em qualquer e todos os canais de material em paralelo.

>[!NOTE]
>
> [Veja o](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) [Corte](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) [original para obter mais informações.](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)

## Parâmetros

### Parâmetros

* **Canais**
  * Ative e desative os canais de material neste grupo ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza, por exemplo.
* **Tamanho de entrada**: *0 - 8192* Resolução e proporções da imagem de entrada. Muito importante para imagens não quadradas.
* **Plano de fundo**: *(Valor da cor) / (Valor da escala de cinza)*Valor uniforme do plano de fundo para áreas não cobertas pelo corte.
* **Transformar**: *(Matriz de Transformação)*\
  Gira e dimensiona o resultado. O resultado pode ser modificado interagindo diretamente com a tela.
* **Deslocamento**: *0.0 - 1.0*\
  Move ou traduz o resultado. O resultado pode ser modificado interagindo diretamente com a tela.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
