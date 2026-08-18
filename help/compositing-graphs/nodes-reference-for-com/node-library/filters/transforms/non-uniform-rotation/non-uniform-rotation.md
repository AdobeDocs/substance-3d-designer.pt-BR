---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-uniform-rotation.html"
breadcrumb-title: ''
description: Use o nó Rotação não uniforme para aplicar transformações de rotação não uniformes para criar efeitos de espiral e vórtice.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Uniform Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Rotação não uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 1%

---


# Rotação não uniforme

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotationgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotationcolor.png){width="200px"}

</td>
</tr>
</table>

**Em:** Filtros*/Transformações*

**Intermediário**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrição

O nó **Rotação Não Uniforme** gira a **Entrada** usando a entrada **Mapa de rotação**.

Os valores da imagem representam um *número de rotações*. A rotação é executada em torno da posição especificada pelo valor de **Posição de pivô** ou pela entrada de **mapa de Posição de pivô**.\
Valores positivos na entrada **Mapa de rotação** resultam em uma rotação *horária*.

</td>
</tr>
</table>

## Parâmetros

### Entradas

* **Entrada** *Tons de Cinza/Cor*\
  A imagem em tons de cinza de entrada que deve ser girada.
* **Mapa de rotação** *Tons de cinza* O mapa usado para controlar a intensidade de rotação, em *número de voltas*. Os valores amostrados são multiplicados pelo **Multiplicador do ângulo de rotação**. Valores negativos resultam em uma rotação *no sentido anti-horário*.
* **Mapa de Posição de pivô de Rotação** *Cor*\
  A imagem usada para especificar a posição da rotação *dinâmica*. A posição **X/Y** está mapeada para os canais **R/G** da imagem.

### Parâmetros

* **Multiplicador De Ângulo De Rotação** *Flutuante*\
  Ajusta a intensidade da entrada de **Mapa de rotação**.
* **Deslocamento Do Ângulo De Rotação** *Flutuante*\
  Aplica a quantidade adicional especificada de rotação.
* **Usar Mapa de Posição de pivô** *Booleano*\
  Use uma *entrada de bitmap* para especificar a posição da tabela dinâmica de rotação. A posição **X/Y** está mapeada para os canais **R/G** da entrada **Mapa de Posições**.
* **Posição de pivô** *Flutuante2*\
  A posição da tabela dinâmica em torno da qual a imagem é girada.
* **Cor do plano de fundo** *Flutuante/Flutuante4*\
  Cor do plano de fundo para exibir *fora* dos limites da imagem caso a divisão em blocos gráficos não esteja definida como **Divisão em blocos gráficos em H e V**.
* **Modo de Filtragem** *Inteiro*\
  Define como tratar os resultados de amostra ao *interpolar* entre pixels:
  * *Mais próximo*: fará uma amostra exatamente do valor *igual* (mais rápido)
  * *Bilinear*: aplicará um filtro bilinear no resultado para uma aparência *mais suave*

## Imagens de exemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-demo-02-resized.gif){width="768px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-variant-png.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/nonuniformrotation-node.png){width="256px"}

</td>
</tr>
</table>
