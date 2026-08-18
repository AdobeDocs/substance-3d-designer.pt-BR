---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/metal-weathering.html"
breadcrumb-title: ''
description: Use o nó Envelhecimento de metal para adicionar efeitos realistas de ferrugem e corrosão a materiais metálicos com base na geometria da malha.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Metal Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Metálico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 1%

---


# Metálico

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/metal-weathering.png){width="128px"}

## Metálico

**Entrada:** *Geradores Baseados Em Malha**/Clima*

**Complexo**

</td>
<td style="border: 0;" valign="top">

## Descrição

## Parâmetros

### Entradas

* **WS normal**: *Entrada de cores*\
  Mapa normal do espaço do mundo assado usado para efeitos internos e mascaramento.
* **Oclusão De Ambiente**: *Entrada Em Tons De Cinza*\
  Mapa baked usado para efeitos internos e mascaramento.
* **Máscara** : *Entrada Em Tons De Cinza*\
  Slot de máscara usado para mascarar os efeitos do nó. Pode ser alternado com o parâmetro “Máscara”.

### Parâmetros

* **Canais**
  * Ative e desative os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza.
* **Avançado**
  * **Formato Normal**: *Direct X, Open GL*\
    Alterna entre diferentes formatos de Mapas Normais (inverte o canal verde).
  * **Máscara**: *Falso/Verdadeiro*\
    Ativa ou desativa o uso do Mapa de máscaras.
* **Efeito**
  * **Dust**: *0.0 - 1.0*
  * **Sujeira**: *0.0 - 1.0*
  * **Bordas Desgastadas**: *0.0 - 1.0*
  * **Descascamento de tinta**: *0.0 - 1.0*
  * **Ferrugem**: *0.0 - 1.0*
  * **Descascamento de Ferrugem**: *0.0 - 1.0*
  * **Ferrugem Verdigris**: *Ferrugem, Verdigris*
  * **Escala do Rachadura de Pintura**: *1.0 - 16.0*
  * **Intensidade de distorção das Rachaduras de pintura**: *0.0 - 1.0*
  * **Escala de Scratches de Bordas Nítidas**: *1.0 - 32.0*
  * **Intensidade de distorção de Scratches de bordas cortantes**: *0.0 - 1.0*
  * **Cor de metal bruta**: *(valor da cor)*
  * **Cor de Specular metálico bruto**: *(Valor da cor)*
  * **Valor da Textura Reluzente Bruta**: *(valor em Tons de Cinza)*
  * **Valor de aspereza de metal bruto**: *(valor em tons de cinza)*
* **Mesclagem**
  * **Intensidade Difusa**: *0.0 - 1.0*\
    Intensidade de mesclagem do Difusa.
  * **Intensidade de cor base**: *0.0 - 1.0*\
    Intensidade de mesclagem da Cor de base.
  * **Intensidade Normal**: *0.0 - 64.0*\
    Intensidade de mesclagem do Normal.
  * **Intensidade de Specular**: *0.0 - 1.0*\
    Intensidade de mistura do Specular.
  * **Intensidade de textura reluzente**: *0.0 - 1.0*\
    Intensidade de mistura da Textura reluzente.
  * **Intensidade de aspereza**: *0.0 - 1.0*\
    Intensidade de mistura da aspereza.
  * **Intensidade Metálica**: *0.0 - 1.0*\
    Intensidade de mistura do Metálico.
  * **Intensidade de Oclusão do ambiente**: *0.0 - 1.0*\
    Intensidade de mesclagem da Oclusão ambiente.
  * **Intensidade de Height**: *0.0 - 1.0*\
    Intensidade de mistura do Height.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
