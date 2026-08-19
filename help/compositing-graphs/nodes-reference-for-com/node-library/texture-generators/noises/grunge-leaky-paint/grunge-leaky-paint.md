---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/grunge-leaky-paint.html"
breadcrumb-title: ''
description: Use o nó Pintura de Desgaste vazada para gerar padrões de vazamento de tinta para criar efeitos de superfície envelhecidos e envelhecidos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Grunge Leaky Paint
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Desgaste Leaky Paint
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---


# Desgaste Leaky Paint

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/grungeleakypaint.jpg){width="200px"}

**Entrada:** *Geradores De Textura* */Ruídos*

**Simples**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrição

O nó **Pintura de Desgaste Vazado** gera um mapa de desgaste semelhante ao gotejamento de tinta através de vazamentos.

</td>
</tr>
</table>

## Parâmetros

* **Equilíbrio** *Flutuante* Ajusta o equilíbrio entre valores escuros e brilhantes.
* **Contraste** *Flutuar* Ajusta o contraste da imagem.
* **Inverter** *Booleano* Inverte a saída da imagem usando uma operação `1-x`.
* **Expansão não quadrada** *Booleano* Habilita a compensação de squash e alongamento com proporções não quadradas.
* Avançado
  * **Intensidade de vazamento** *Flutuante* Ajusta a densidade e a intensidade das gotas.
  * **Escala de vazamento** *Inteiro* Ajusta a escala da separação de gotas.
  * **Ângulo de fuga Aleatório** *Flutuante* Ajusta o *ângulo máximo* para o qual gotas podem ser giradas aleatoriamente, em *número de voltas*.
  * **Vazamento de nitidez** *Flutuar* Ajusta a nitidez e a nitidez das gotas.

## Imagens de exemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/grungeleakypaint-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/grungeleakypaint-variant2.jpg){width="256px"}

</td>
</tr>
</table>
