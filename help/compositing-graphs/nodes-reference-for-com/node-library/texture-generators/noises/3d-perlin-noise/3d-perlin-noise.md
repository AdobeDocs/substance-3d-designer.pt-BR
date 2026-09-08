---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise.html"
breadcrumb-title: ''
description: Use o nó Ruído de perlin 3D para gerar padrões de ruído de perlin suaves no espaço 3D para criar texturas volumétricas de aparência natural.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Perlin Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ruído Perlin 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---


# Ruído Perlin 3D

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise.png){width="200px"}

**Entrada:** *Geradores De Textura**/Ruídos*

**Intermediário**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrição

O nó **Ruído de Perlin 3D** gera um ruído de Perlin no espaço 3D com base na entrada do **Mapa de Posições**.

Este nó pode ser testado com [GBuffers 3D de cubo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) como entrada em vez de um mapa baked real (como visto na Imagem de Exemplo abaixo).

>[!WARNING]
>
> Este ruído deve ser usado somente com o *mecanismo de GPU* (por exemplo, **Direct3D** ou **OpenGL**). Vá para **Ferramentas > Alternar mecanismo...** ou pressione a tecla **F9** para selecionar o mecanismo desejado.

</td>
</tr>
</table>

## Parâmetros

* **Inverter** *Booleano*\
  Inverte a imagem de saída.
* **Escala** *Precisão decimal*\
  Controla a escala do ruído de Perlin 3D.
* **Tamanho** *Precisão decimal 3*\
  Controla o tamanho do ruído de Perlin 3D nos eixos **X**, **Y** e **Z**. Valores não uniformes resultam em um efeito de *amplificação ou esmagamento*.
* **Deslocamento** *Flutuante3*\
  Aplica um deslocamento à *posição* do ruído de Perlin 3D nos eixos **X**, **Y** e **Z**.
* **Intensidade de Distorção** *Precisão decimal*\
  Controla a intensidade de um *efeito de distorção* aplicado no ruído 3D Perlin.
* **Multiplicador de Escala de Distorção** *Precisão decimal*\
  Controla a escala do *padrão de deformação* usado no efeito de distorção controlado pela **Intensidade de Distorção**.
* **Linha de base** *Precisão decimal*\
  Aplica um *deslocamento* ao valor de *luminância* da linha de base para a distribuição do valor de ruído Perlin 3D.
* **Contraste** *Flutuante*\
  Ajusta o contraste do ruído de Perlin 3D.
* **Absoluto** *Booleano*\
  Usa valores absolutos no ruído Perlin 3D. Isso efetivamente *inverte* a distribuição de valores *abaixo de 0,5*.
* **Habilitar divisão em blocos** *Booleano*\
  Ajusta o ruído de Perlin 3D para que seu padrão resultante *se repita* nos eixos X, Y e Z.

## Imagens de exemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlin.gif){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoise-variant.jpg){width="256px"}

</td>
</tr>
</table>
