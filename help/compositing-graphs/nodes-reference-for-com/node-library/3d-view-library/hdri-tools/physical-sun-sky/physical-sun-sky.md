---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/physical-sun-sky.html"
breadcrumb-title: ''
description: Use o nó Físico do SunSky para gerar ambientes de iluminação física precisos do sol e do céu para visualização de material realista.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Physical SunSky
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SunSky físico
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---


# Sol/céu físico

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-physical-sun-sky.png){width="200px"}

## Sol/céu físico

**Entrada:** *Exibição 3D/Ferramentas HDRI*

**Intermediário**

</td>
<td style="border: 0;" valign="top">

## Descrição

Implementação física de Sun e Sky baseada no modelo de claraboia Hosek-Wikie. Fornece uma base excelente para um HDRI artificial.

## Parâmetros

* **Posição do Sol**:\
  gama = [0,1]x[0,1] (ângulos de longitude e latitude)
* **Turbidez**: *1.0 - 10.0*\
  A turbidez varia de 1 a 10
* **Albedo**: *0.0 - 1.0*\
  O albedo varia de 0 a 1.
* **Cor do solo**: *(valor da cor)*\
  Cor do plano do solo.
* **Exposição (EV)**: *-1.0 - 4.0*\
  Valor da exposição da saída resultante.
* **Tamanho do Sol**: *0.0 - 4.0*\
  Escala do Sol, qualquer valor diferente de 1 é fisicamente incorreto. O valor tem efeitos sutis!
* **Intensidade do Sol**: *0.0 - 1.0*\
  Intensidade do disco solar. O disco solar é relativamente pequeno, por isso o efeito não é imediatamente visível.
* **Intensidade do céu**: *0.0 - 1.0* Intensidade do céu. Também afeta a queima do sol no céu, não no disco em si.

## Imagens de exemplo

![](../../../../../../assets/sky-ex.gif)

</td>
</tr>
</table>
