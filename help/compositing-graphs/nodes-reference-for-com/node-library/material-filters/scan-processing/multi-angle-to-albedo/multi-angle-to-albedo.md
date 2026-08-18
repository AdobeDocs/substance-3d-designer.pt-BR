---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-angle-to-albedo.html"
breadcrumb-title: ''
description: Use o nó Multiângulo para Albedo para extrair mapas de albedo de imagens digitalizadas multiângulo para cores de material limpo.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi-Angle to Albedo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Multiângulo para Albedo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---


# Multiângulo para Albedo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-angle-to-albedo.png){width="128px"}

## Multiângulo para Albedo

**Entrada:** *Filtros de Material/Processamento de Digitalização*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Este nó tenta remover todas as informações de iluminação de um conjunto de fotografias/digitalizações de entrada que foram tiradas sob ângulos de iluminação diferentes. Ele combina todas as amostras em uma única imagem que deve ser tão neutra em termos de iluminação e, portanto, PBR-correta, quanto possível.

Lembre-se de que quanto mais amostras você tiver e quanto maior a diferença no ângulo de iluminação, maior será o sucesso alcançado. A partir de quatro amostras, deve ser possível obter resultados quase perfeitos, dependendo das imagens de entrada. As imagens de entrada devem ser tiradas com um tripé e ter o mínimo de diferenças, ou idealmente nenhuma diferença, exceto para iluminação de um ângulo diferente!

>[!NOTE]
>
> Consulte [Múltiplo-ângulo para Normal](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md) para obter a versão de Normalmap deste nó. Se você quiser pré-processar suas entradas, o [Multi Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md), o [Multi Crop](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md) e o [Multi Clone Patch](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md) podem ser úteis, pois devem ser combinados com esses nós.
> 
> [A postagem no blog “Seu Smartphone é um scanner de material” ilustra um pouco melhor esse processo.](https://www.allegorithmic.com/blog/your-smartphone-material-scanner)

## Parâmetros

### Entradas

* **Entrada 1-8**: *Entrada de cores* O número de entradas é determinado pelo parâmetro Valor de Amostras.

### Parâmetros

* **Quantidade de Amostras**: *2 - 8* Define o número de amostras (entradas) a serem usadas no processamento.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
