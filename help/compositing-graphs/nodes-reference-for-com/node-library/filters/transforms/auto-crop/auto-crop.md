---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/auto-crop.html"
breadcrumb-title: ''
description: Use o nó Corte automático para cortar texturas automaticamente para remover bordas vazias e otimizar as dimensões da textura.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Auto Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Corte automático
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---


# Corte automático

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocropgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocropcolor.png){width="200px"}

</td>
</tr>
</table>

**Em:** Filtros*/Transformações*

**Simples**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrição

O nó **Corte automático** ajusta a **Entrada** de modo que o conteúdo seja colocado no *centro* da imagem sem ser redimensionado ou *redimensionado para a extensão* da imagem.

O conteúdo da imagem é definido por uma caixa ajustada ao *primeiro e último pixels* em **X** e **Y**, cujos valores são *superiores a 0* (ou seja, não são pretos). A versão **Cor** permite escolher entre os canais RGB e Alpha para definir essa caixa.

</td>
</tr>
</table>

## Parâmetros

* **Modo** *Inteiro* Defina o método de corte que deve ser aplicado:
  * *Quadrado de corte*: a imagem é cortada de forma que a forma fique no centro da menor imagem *quadrada* que pode incluí-la totalmente
  * *Corte automático*: a imagem é cortada de forma que a forma fique no centro da menor imagem *quadrada ou não quadrada* que pode incluí-la totalmente
  * *Ajustar (Manter proporção)*: a imagem é redimensionada para o *tamanho total* da imagem enquanto mantém suas *proporções* (ou seja, proporção largura/comprimento)
  * *Preenchimento (Esticamento)*: a imagem é redimensionada para o *tamanho total* da imagem
* **Usar alfa** *booleano* Use o canal alfa da **entrada** para determinar os *limites* do conteúdo da imagem para corte. Quando definido como *Falso*, os pixels pretos são usados.\
  *Observação*: este parâmetro só está disponível na versão **Cor** do nó.
* **Modo de Filtragem** *Inteiro* Define como tratar os resultados de amostra ao *interpolar* entre pixels:
  * *Mais próximo*: fará uma amostra exatamente do valor *igual* (mais rápido)
  * *Bilinear*: aplicará um filtro bilinear no resultado para uma aparência *mais suave*
  * *Automático*: usa o modo mais apropriado dos dois acima, dependendo do **Modo** selecionado para corte

## Imagens de exemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-demo-01-resized.gif){width="768px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant.jpg){width="128px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant4.png){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant3.png){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-node.png){width="420px"}

</td>
</tr>
</table>
