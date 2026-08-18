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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Snow Cover

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/snow-cover.png){width="128px"}

## Snow Cover

**Entrada:** *Filtros/Efeitos de Material*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Efeito multifuncional para adicionar neve acumulada em um material completo. Altamente depende de um mapa de altura bom e de alta qualidade, como de uma varredura de fotos. O resultado deve ser PBR-correto.

## Parâmetros

### Entradas

* **Máscara (opcional)**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Canais**\
  Ative e desative os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza.
* **Snow fresco**: *0.0 - 1.0* Define a quantidade de neve em áreas elevadas. O resultado está vinculado ao parâmetro Snow derretido.
* **Snow derretido**: *0.0 - 1.0* Define a quantidade de neve derretida nos cantos inferiores.
* **Compilação**: *0.0 - 1.0* Afeta principalmente a saída do Height, determina o efeito de empilhamento do height.
* **Smoothness**: *0.0 - 1.0* Define a suavização dos detalhes do height pelo acúmulo de neve.
* **Intensidade de flocos**: *0.0 - 1.0* Afeta principalmente o Normalmap, a intensidade dos detalhes de flocos.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
