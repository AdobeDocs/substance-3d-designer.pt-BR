---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/multi-switch.html"
breadcrumb-title: ''
description: Use o nó Multiswitch para alternar entre várias texturas de entrada com base em um seletor para seleção de textura condicional.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Multi Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Comutador múltiplo
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---


# Comutador múltiplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-switch-greyscale.png){width="128px"}

![](../../../../../../assets/multi-switch.png){width="128px"}

## Chave Múltipla (Tons de Cinza)

**Entrada:** *Filtros/Mesclagem*

**Simples**

</td>
<td style="border: 0;" valign="top">

## Descrição

Atua como uma switch-box, apenas passando pela entrada definida pelo parâmetro &#39;Input Selection&#39;. Portanto, se duas entradas estiverem conectadas, somente uma delas será retornada (sem modificações), dependendo da escolha do usuário.

Muito útil para adicionar muitas opções diferentes em um gráfico. Combinado com a [exposição](../../../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)(de preferência como uma Lista Suspensa), é possível muita personalização.

Importante: certifique-se de usar a versão apropriada para sua entrada! Use “Múltiplo switch” para entradas de cor, “Múltiplo switch de tons de cinza” para entradas de tons de cinza.

## Parâmetros

### Entradas

* **Entrada 1-20**: *Entrada de Cores*

### Parâmetros

* **Número de entrada**: *2 - 20* Quantidade de entradas a serem expostas. Importante: não remove conexões quando o número é reduzido!
* **Seleção de Entrada**: *1 - 20* Qual entrada deve retornar como resultado.

## Imagens de exemplo

</td>
</tr>
</table>
