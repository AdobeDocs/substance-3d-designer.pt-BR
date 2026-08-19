---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/multi-material-blend.html"
breadcrumb-title: ''
description: Use o nó Mesclagem de vários materiais para mesclar vários materiais para criar combinações de materiais complexas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Multi-Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Mesclagem de vários materiais
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---


# Mesclagem de vários materiais

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-material-blend.png){width="128px"}

## Mesclagem de vários materiais

**Entrada:** *Filtros/Mesclagem de Material*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Este nó combina vários materiais com base em um mapa de ID de material/ID de cor, que pode ser cozido de uma malha. São necessários até 16 materiais completos diferentes, com qualquer tipo de canais que você ative no grupo Canais.

O nó é muito útil ao texturizar adereços completos, pois permite a parametrização completa de materiais enquanto ainda combina dinamicamente todos eles. Perfeito para texturizar adereços simples a complexos que têm bolos de ID adequados, ou até mesmo para criar Substance de “Modelo” totalmente pipeline que totalmente cohere aos padrões de equipe.

Lembre-se de que, ao usar isso, o Material 1, Slot 1 é sempre o material padrão e aparecerá em qualquer lugar em que nenhum outro material apareça. É por isso que não é possível configurar uma cor para ele. Se quiser jogar este cofre, você pode, por exemplo, conectar um [Material de base](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md) definido como preto áspero.

## Parâmetros

### Entradas

* **1-16 slots de material completos** A quantidade de slots é determinada pelo menu suspenso **Materiais**.
* **ID de Cor**: *Entrada de Cor*\
  Mapa de ID de cor assada.

### Parâmetros

* **Materiais**: *2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16* Define a quantidade máxima de materiais diferentes a serem mesclados.
* **Canais**\
  Ative e desative os canais de material neste grupo, por exemplo, ao usar mapas de Specular/Textura reluzente em vez de Metálico/Aspereza.
* **Material 2-16** Um grupo aparece para cada material habilitado.
  * **Cor**: *(valor da cor)*Cor para escolher no mapa de ID que corresponde a este slot de material.
  * **Grau de seleção**: *0.01 - 1.0* Sangria para as cores vizinhas.
  * **Preenchimento**: *0.0 - 1.0* Dureza das transições: contraste de máscara.

## Imagens de exemplo

|  |
| --- |
| Não há imagens anexadas a esta página. |

</td>
</tr>
</table>
