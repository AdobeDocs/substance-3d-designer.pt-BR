---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/hald-clut.html"
breadcrumb-title: ''
description: Use o nó Hald CLUT para aplicar tabelas de pesquisa de cores usando o formato Hald CLUT para correção e correção de cores.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Hald CLUT
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Hald CLUT
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---


# Hald CLUT

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hald-clut.png){width="128px"}

## Hald CLUT

**Entrada:** *Filtros/Ajustes*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Aplica uma LUT na imagem de entrada. A LUT deve estar no formato Hald na resolução 4096\*4096. Consulte <http://www.quelsolaar.com/technology/clut.html> para obter mais informações.

### Entradas

* **entrada**: *entrada de cores*\
  Imagem na qual aplicar o LUT.
* **lut**: *Entrada de cor* slot de entrada Lut. Deve ser de 4096 x 4096.

## Parâmetros

* **Intensidade LUT por Alpha**: *False/True* Define se o efeito LUT é ponderado pelo canal alfa.

Exemplos

![](../../../../../../assets/content-hald-clut.jpg)

</td>
</tr>
</table>
