---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise-fractal.html"
breadcrumb-title: ''
description: Use o nó Fractal de ruído Perlin 3D para gerar padrões de ruído Perlin fractais no espaço 3D para criar texturas volumétricas detalhadas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Perlin Noise Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Fractal de ruído Perlin 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---


# Fractal de ruído Perlin 3D

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoisefractal.png){width="200px"}

**Entrada:** *Geradores De Textura**/Ruídos*

**Intermediário**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrição

O nó **Fractal de Ruído Perlin 3D** gera um ruído Perlin *fractal* no espaço 3D com base na entrada do **Mapa de Posições**.

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
* **Escala** *Flutuante*\
  Controla a escala do ruído fractal de Perlin 3D.
* **Tamanho** *Flutuante3*\
  Controla o tamanho do ruído fractal de Perlin 3D nos eixos **X**, **Y** e **Z**. Valores não uniformes resultam em um efeito de *amplificação ou esmagamento*.
* **Deslocamento** *Flutuante3*\
  Aplica um deslocamento à *posição* do ruído fractal de Perlin 3D nos eixos **X**, **Y** e **Z**.
* **Intensidade de Distorção** *Flutuante*\
  Controla a intensidade de um *efeito de distorção* aplicado no ruído fractal de Perlin 3D.
* **Multiplicador de Escala de Distorção** *Flutuante*\
  Controla a escala do *padrão de deformação* usado no efeito de distorção controlado pela **Intensidade de Distorção**.
* **Nível mínimo** *Inteiro*\
  O *nível mínimo de repetição* usado no padrão fractal. Um intervalo mínimo/máximo mais amplo resulta em um *padrão mais rico* com variação em intervalos de frequência mais amplos.
* **Nível Máximo** *Inteiro*\
  O *nível máximo de repetição* usado no padrão fractal. Um intervalo mínimo/máximo mais amplo resulta em um *padrão mais rico* com variação em intervalos de frequência mais amplos.
* **Aspereza** *Flutuante*\
  Controla o *equilíbrio* entre *níveis de repetição* baixos e altos no padrão fractal.\
  *Observação*: um valor de **0** resulta em uma saída que *não está alinhada* com outros valores baixos que a seguem. Isso é esperado.
* **Lacunaridade** *Flutuante*\
  Controla como o padrão fractal *aplicado preenche o espaço*. Um valor *mais alto* resulta em *menos lacunas* no padrão e em um ruído *mais denso*.
* **Opacidade Global** *Flutuante*\
  Controla o *intervalo* dos valores de ruído fractais de Perlin 3D *ao redor* do valor de **Linha de base**.
* **Linha de base** *Flutuante*\
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

![](../../../../../../assets/3dfractal.gif){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoisefractal-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoisefractal-variant2.jpg){width="256px"}

</td>
</tr>
</table>
