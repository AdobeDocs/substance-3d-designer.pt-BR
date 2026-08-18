---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/voronoi.html"
breadcrumb-title: ''
description: Use o nó Voronoi para gerar padrões Voronoi para criar texturas celulares e efeitos de material orgânico.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Voronoi
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Voronoi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---


# Voronoi

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/voronoi.png){width="200px"}

**Entrada:** *Geradores De Textura* */Ruídos*

**Intermediário**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrição

O nó **Voronoi** gera um ruído Voronoi 3D mapeado para uma imagem 2D usando uma *projeção ortográfica Z-down*.

Este nó pode ser testado com [GBuffers de Cubo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) como entrada em vez de um mapa baked real (como visto na Imagem de Exemplo abaixo).

>[!WARNING]
>
> Este ruído deve ser usado somente com o *mecanismo de GPU* (por exemplo, **Direct** ou **OpenGL**). Vá para **Ferramentas > Alternar mecanismo...** ou pressione a tecla **F9** para selecionar o mecanismo desejado.

</td>
</tr>
</table>

## Parâmetros

* **Inverter** *Booleano*\
  Inverte a imagem de saída.
* **Escala** *Flutuante*\
  Controla a escala do ruído de Voronoi.\
  *Observação*: quando o **lado a lado** está habilitado em *qualquer eixo*, o ajuste de escala é *escalonado*. Isso é esperado.
* **Tamanho** *Flutuante3*\
  Controla o tamanho do ruído de Voronoi nos eixos **X**, **Y** e **Z**. Valores não uniformes resultam em um efeito de *amplificação ou esmagamento*.\
  *Observação*: quando a **Divisão em blocos gráficos** está habilitada em *qualquer eixo*, o ajuste de tamanho é *escalonado*. Isso é esperado.
* **Deslocamento** *Flutuante3*\
  Aplica um deslocamento à *posição* do ruído de Voronoi nos eixos **X**, **Y** e **Z**.
* **Desordem** *Flutuante3*\
  A intensidade do *deslocamento aleatório* aplicado a cada ponto do ruído nos eixos **X**, **Y** e **Z**.
* **Intensidade de Distorção** *Flutuante*\
  Controla a intensidade de um *efeito de distorção* aplicado no ruído de Voronoi.
* **Multiplicador de Escala de Distorção** *Flutuante*\
  Controla a escala do *padrão de deformação* usado no efeito de distorção controlado pela **Intensidade de Distorção**.
* **Curva arredondada** *Flutuante*\
  Arredonda a *inclinação* em torno de cada ponto do ruído para torná-lo *convexo*.\
  *Observação*: este parâmetro não está disponível quando o parâmetro **Estilo** está definido como *Borda*.
* **Escala de distância** *Flutuante*\
  Ajusta a *distância do gradiente* ao redor de cada ponto do ruído.
* **Modo de distância** *Inteiro*\
  Define o método para *calcular o gradiente de distância* ao redor de cada ponto do ruído:
  * *Euclidiano*
  * *Manhattan*
  * *Chebyshev*
  * *Minkowski*
* **Número de Minkowski** *Flutuante*\
  A ordem *p* da distância de Minkowski. Se dividirmos o gradiente de distância em quadrantes, esse número afetará esses quadrantes da seguinte maneira:
  * p é *exatamente* 1: direto
  * p é *mais baixo* do que 1: côncavo
  * p é *maior* do que 1: convexo\
    Valores interessantes:\
    *- 1.0*: Distância de Manhattan\
    *- 2.0*: distância euclidiana\
    *- Infinito*: distância de Chebyshev\
    *Observação*: este parâmetro só está disponível quando o parâmetro **Modo de Distância** está definido como *Minkowski*.
* **Estilo** *Inteiro* Define o método *renderizando os dados* do ruído Voronoi, considerando que o ruído é baseado em um conjunto de pontos no espaço:
  * *F1*: a distância até o *ponto mais próximo* no espaço
  * *F2*: a distância até o *segundo ponto mais próximo* no espaço
  * *F2-F1*- *F1\* F2 *-* F1/F2 *-* Borda *: a* borda entre cada célula* do ruído no espaço
  * *Cor aleatória*: atribua uma *cor simples aleatória* a cada célula do ruído no espaço
* **Thickness de borda** *Flutuante* Ajusta o thickness das bordas detectadas entre células do ruído de Voronoi. As bordas são detectadas nos eixos X, Y e Z, portanto, algumas espessuras podem aumentar mais rapidamente do que outras, dependendo da *profundidade* das células.\
  *Observação*: este parâmetro só está disponível quando o parâmetro **Estilo** está definido como *Borda*.
* **Modo De Semente De Cor Aleatória** *Inteiro*\
  Define o método de *aquisição* da semente aleatória para a seleção de cores por célula:
  * *Propagação Aleatória Global*: usar a propagação *herdada* pelo nó
  * *Propagação manual*: usar uma *semente discreta*\
    *Observação*: este parâmetro só está disponível quando o parâmetro **Estilo** está definido como *Cor aleatória*.
* **Semente de Cor Aleatória** *Inteiro*\
  A semente aleatória discreta que deve ser usada para a seleção de cores por célula.\
  *Observação*: este parâmetro só está disponível quando o parâmetro **Estilo** está definido como *Cor aleatória* e o parâmetro **Modo de Distribuição de Cor Aleatória** está definido como ***Distribuição Manual***.
* **Expansão não quadrada** *Booleano*\
  Permite a compensação de esmagamento e alongamento com proporções não quadradas.

## Imagens de exemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant6.jpg){width="256px"}

</td>
</tr>
</table>
