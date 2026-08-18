---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter-to-mask.html"
breadcrumb-title: ''
description: Use o nó respingos de forma para máscara para converter padrões de respingos de forma em máscaras para mesclagem de material e efeitos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter to Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dispersão de forma para máscara
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---


# Dispersão de forma para máscara

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-splatter-to-mask.png){width="128px"}

## Dispersão de forma para máscara

**Entrada:** *Geradores De Textura**/Padrões*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Converte Dados de [Respingo de Forma](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md) em uma máscara preto e branco com base na ID de Padrão. Permite, por exemplo, criar uma máscara com apenas um determinado tipo de padrão. Tem opções extras para selecionar um intervalo de IDs de padrão e ocultar aleatoriamente algumas das formas.

## Parâmetros

### Parâmetros

* **Intervalo Inicial de ID de Padrão**: *1 - 8* Defina a primeira ID de Padrão no intervalo a ser selecionado.
* **Intervalo Final de ID de Padrão**: *1 - 8* Defina a última ID de Padrão no intervalo a ser selecionado.
* **Máscara aleatória**: *0.0 - 1.0* Defina a proporção de Padrões para mascarar aleatoriamente.
* **Saída**: *Máscara binária, Máscara de número inteiro, Valores em tons de cinza* Determine o tipo de valores de saída. A Máscara binária retorna apenas valores em preto e branco, 0-ou-1, a Máscara de inteiro codificará valores mais altos até 8 para cada Padrão no formato HDR e os Valores em tons de cinza propagarão o intervalo proporcionalmente entre 0 e 1.

</td>
</tr>
</table>
