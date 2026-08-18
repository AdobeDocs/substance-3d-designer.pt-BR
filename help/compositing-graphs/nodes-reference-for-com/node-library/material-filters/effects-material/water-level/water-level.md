---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/water-level.html"
breadcrumb-title: ''
description: Use o nó Nível da água para misturar materiais com base no height do nível da água para criar efeitos realistas da água.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Water Level
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nível da água
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 1%

---


# Nível da água

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/water-level.png){width="128px"}

## Nível da água

**Entrada:** *Filtros/Efeitos de Material*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

Efeito multifuncional que adiciona um nível de água a uma entrada de material completa. O material de entrada deve ter um Heightmap de boa qualidade para que o efeito funcione. O resultado está correto para PBR.

## Parâmetros

### Entradas

* **Máscara**: *Entrada em tons de cinza*\
  Slot de máscara usado para mascarar os efeitos do nó.

### Parâmetros

* **Canais**\
  Ative e desative os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza.
* **Nível da água**: *0.0 - 1.0* Controle principal para aumentar ou diminuir o nível da água.
* **Escuridão da Água**: *0.0 - 1.0* Define a “transparência” geral da água.
* **Umidade das Bordas**: *0.0 - 1.0* Determina quanto de uma aparência molhada as bordas da água devem ter.
* **Distância de Umidade das Bordas**: *0.0 - 1.0* Define o quanto as bordas molhadas atingem.
* **Quantidade de Desfoque de Profundidade**: *0.0 - 1.0* Define a quantidade de desfoque com base na profundidade abaixo da água. Modifica o raio do desfoque.
* **Opacidade do desfoque de Profundidade**: *0.0 - 1.0* Determina a quantidade de desfoque de profundidade que é misturada, podendo ser usada para diminuir o efeito do desfoque.
* **Cor do lodo**: *(valor da cor)*Define a cor do efeito de lodo.
* **Profundidade de lamas**: *0.0 - 1.0* Define a profundidade em que o lodo começa a aparecer, em relação ao nível da água.
* **Opacidade do lodo**: *0.0 - 1.0* Define a opacidade global do efeito de lodo.
* **Geada**: *0.0 - 1.0* Define a quantidade de geada. Começa a aparecer a partir das bordas externas e se move para dentro.
* **Intensidade da geada**: *0.0 - 1.0* Define a intensidade da geada, controla a “opacidade” do efeito.
* **Rachaduras de geada**: *0.0 - 1.0* Define a quantidade de rachaduras nas transições de congeladas para líquidas.
* **Formato normal de geada**: *DirectX/OpenGL* Alterna o canal verde do efeito de mapa normal de geada.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
