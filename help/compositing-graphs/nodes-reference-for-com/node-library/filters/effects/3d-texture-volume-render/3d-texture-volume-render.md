---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-volume-render.html"
breadcrumb-title: ''
description: Use o nó Renderização de volume de textura 3D para renderizar texturas volumétricas a partir de dados 3D para criar efeitos de nuvem e neblina.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Volume Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Renderização de volume de textura 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---


# Renderização de volume de textura 3D

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender.png){width="200px"}

**Entrada:** *Filtro/Efeito*

**Simples**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrição

O nó **Renderização de Volume de Textura 3D** renderiza o volume de uma forma descrita por uma *textura 3D*, usando seu *campo de distância assinado* correspondente da entrada de imagem **Campo de distância sinalizado 3D**.

O volume é representado dentro dos limites de um *cubo de unidade*. A iluminação é calculada usando a *luz direcional* e uma *claraboia hemisférica*.

>[!NOTE]
>
> Espera-se que o campo de distância assinado seja uma textura **4096x4096** descrevendo a forma com uma grade **16x16** de 256 fatias.\
> Você pode usar o nó [SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) de Textura 3D para calcular o campo de distância assinada para uma textura 3D de 256 fatias.

</td>
</tr>
</table>

## Parâmetros

### Entradas

* **Campo de distância sinalizado 3D** *Tons de cinza*\
  A imagem 4096x4096 que representa as 256 *fatias* do *campo de distância assinado* de uma forma, organizada em uma grade de 16x16.\
  Você pode usar o nó [SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) de Textura 3D para calcular o campo de distância assinada para uma textura 3D de 256 fatias.
* **Densidade** *Tons de cinza*\
  A imagem 4096x4096 que representa as 256 *fatias* de *densidade* de uma forma, organizadas em uma grade de 16x16. A densidade é mapeada usando valores de tons de cinza de 0 (totalmente transparente) a 1 (totalmente opaco).\
  Você pode usar a [Máscara de Volume 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) ou os nós de ruído 3D ([Ruído de Perlin 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md), [Voronoi 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-voronoi/3d-voronoi.md), [Fractal de Ruído Ondulado 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-ridged-noise-fractal/3d-ridged-noise-fractal.md) etc.), combinados com um nó [Posição de Textura 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-position/3d-texture-position.md) como entrada de posição, para gerar uma máscara de volume como uma textura 3D de 256 fatias.

### Parâmetros

* **Resolução de Saída** *Inteiro2*\
  A resolução da imagem de saída em **X** e **Y**, expressa como uma *potência de dois*.
* **Posição da Câmera** *Flutuante2*\
  A posição da câmera ao redor da forma.\
  Quando o nó for selecionado, você poderá usar o gizmo de posição na **Exibição 2D** para *orbitar* a câmera.
* **Posição da Luz** *Flutuante2*\
  A posição da *luz direcional* ao redor da forma.\
  Quando o nó for selecionado, você poderá usar o gizmo de posição na **Exibição 2D** para *orbitar* a fonte de luz.
* **Distância da Câmera** *Flutuante*\
  A distância da câmera até a forma.
* **CDV de câmera** *Flutuante*\
  O campo de visualização da câmera em *graus*.
* **Absorção** *Flutuante*\
  Ajusta a quantidade de luz que é absorvida à medida que passa *pelo* volume.
* **Difusão** *Flutuante*\
  Multiplica o valor fornecido pela entrada **Densidade** pelo valor de campo de distância *interna*.\
  Isso ajusta efetivamente a largura do *gradiente de atenuação* do limite externo do volume para dentro.
* **Modo de Cores Claras** *Inteiro*\
  Define o método de aquisição da cor da luz direcional:
  * *Temperatura (Kelvin)*: a cor resulta da temperatura da luz, onde um valor *menor* resulta em uma cor *mais quente*
  * *Cor do RGB*: defina a cor usando valores de RGB
* **Temperatura da Luz (Kelvin)** *Flutuar*\
  A temperatura da luz direcional, que afeta sua *cor*. Um valor *mais baixo* resulta em uma cor *mais quente*.\
  Valores úteis:\
  1800 K - Luz de vela\
  2800 K - Lâmpada incandescente\
  5500 K - Luz do dia\
  6200 K - Branco natural\
  7000 K - Céu nublado\
  *Observação*: este parâmetro só está disponível quando o parâmetro **Modo de Cor Claro** está definido como *Temperatura (Kelvin)*.
* **Cor clara** *Flutuante3*\
  A cor da luz direcional.\
  *Observação*: este parâmetro só está disponível quando o parâmetro **Modo de Cor Claro** está definido como *Cor de RGB*.
* **Intensidade de luz** *Flutuante*\
  A intensidade da luz direcional.
* **Cor do ambiente** *Flutuante3*\
  A cor da claraboia ambiente.
* **Intensidade do ambiente** *Flutuante*\
  A intensidade da claraboia ambiente.
* **Albedo** *Flutuante3*\
  A cor do albedo do volume.
* **Modo de plano de fundo** *Inteiro*\
  O método de sombreamento do plano de fundo da cena renderizada, com base na **Cor do Plano de Fundo**:
  * *Sombreada*: a cor é afetada pela *cor* e pela *intensidade* da luz direcional- *Cor constante*: a cor é aplicada uniformemente *independentemente* da luz direcional
* **Cor do plano de fundo** *Flutuante4*\
  A cor usada para preencher o plano de fundo da cena renderizada.
* **Pontilhamento** *Flutuante*\
  Ajusta a intensidade do *pontilhamento de ruído azul* usado para suavizar o sombreamento.
* **Habilitar Plano Terrestre** *Booleano*\
  Quando *True*, renderiza um plano terrestre *infinito*. O *cubo de unidade* que inclui a forma está neste plano.
* **Plano infinito** *Booleano*\
  Define o plano do solo para *se estender infinitamente* para o horizonte.\
  *Observação*: este parâmetro só está disponível quando o parâmetro **Habilitar plano horizontal** está definido como *Verdadeiro*.
* **Tamanho do plano do solo** *Flutuante2* Ajusta o tamanho do plano do solo.\
  *Observação*: este parâmetro só está disponível quando o parâmetro **Habilitar Plano Terrestre** está definido como *Verdadeiro* e o parâmetro **Plano Infinito** está definido como *Falso*.

## Imagens de exemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-node.png){width="512px"}

</td>
</tr>
</table>
