---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/voronoi-fractal.html"
breadcrumb-title: ''
description: Use o nó fractal de Voronoi para gerar padrões fractais de Voronoi para criar texturas celulares orgânicas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Voronoi Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Voronoi Fractal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---


# Voronoi Fractal

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal.png){width="200px"}

**Entrada:** *Geradores de Textura* */Ruídos*

**Intermediário**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## Descrição

O nó **Voronoi Fractal** gera um ruído de Voronoi 3D *fractal* mapeado para uma imagem 2D usando uma *projeção ortográfica Z-down*.

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
* **Escala** *Precisão decimal*\
  Controla a escala do ruído fractal de Voronoi.\
  *Observação*: quando o **lado a lado** está habilitado em *qualquer eixo*, o ajuste de escala é *escalonado*. Isso é esperado.
* **Tamanho** *Precisão decimal 3*\
  Controla o tamanho do ruído fractal de Voronoi nos eixos **X**, **Y** e **Z**. Valores não uniformes resultam em um efeito de *amplificação ou esmagamento*.\
  *Observação*: quando a **Divisão em blocos gráficos** está habilitada em *qualquer eixo*, o ajuste de tamanho é *escalonado*. Isso é esperado.
* **Deslocamento** *Flutuante3*\
  Aplica um deslocamento à *posição* do ruído fractal de Voronoi nos eixos **X**, **Y** e **Z**.
* **Desordem** *Flutuante3*\
  A intensidade do *deslocamento aleatório* aplicado a cada ponto do ruído nos eixos **X**, **Y** e **Z**.
* **Intensidade de Distorção** *Precisão decimal*\
  Controla a intensidade de um *efeito de distorção* aplicado no ruído fractal de Voronoi.
* **Multiplicador de Escala de Distorção** *Precisão decimal*\
  Controla a escala do *padrão de deformação* usado no efeito de distorção controlado pela **Intensidade de Distorção**.
* **Nível mínimo** *Inteiro*\
  O *nível mínimo de repetição* usado no padrão fractal. Um intervalo mínimo/máximo mais amplo resulta em um *padrão mais rico* com variação em intervalos de frequência mais amplos.
* **Nível Máximo** *Inteiro*\
  O *nível máximo de repetição* usado no padrão fractal. Um intervalo mínimo/máximo mais amplo resulta em um *padrão mais rico* com variação em intervalos de frequência mais amplos.
* **Aspereza** *Precisão decimal*\
  Controla o *equilíbrio* entre *níveis de repetição* baixos e altos no padrão fractal.\
  *Observação*: um valor de **0** resulta em uma saída que *não está alinhada* com outros valores baixos que a seguem. Isso é esperado.\
  *Observação 2*: este parâmetro só está disponível quando o parâmetro **Modo de Mesclagem** está definido como *Adicionar*.
* **Lacunaridade** *Flutuante*\
  Controla como o padrão fractal *aplicado preenche o espaço*. Um valor *mais alto* resulta em *menos lacunas* no padrão e em um ruído *mais denso*.
* **Opacidade Global** *Precisão decimal*\
  Controla o *intervalo* dos valores de ruído fractal de Perlin de 0.
* **Curva arredondada** *Precisão decimal*\
  Arredonda a *inclinação* em torno de cada ponto do ruído para torná-lo *convexo*.\
  *Observação*: este parâmetro não está disponível quando o parâmetro **Estilo** está definido como *Borda*.
* **Escala de distância** *Precisão decimal*\
  Ajusta a *distância do gradiente* ao redor de cada ponto do ruído.
* **Modo de distância** *Inteiro*\
  Define o método para *calcular o gradiente de distância* ao redor de cada ponto do ruído:
  * *Euclidiano*
  * *Manhattan*
  * *Chebyshev*
  * *Minkowski*
* **Número de Minkowski** *Precisão decimal*\
  A ordem *p* da distância de Minkowski. Se dividirmos o gradiente de distância em quadrantes, esse número afetará esses quadrantes da seguinte maneira:
  * p é *exatamente* 1: direto
  * p é *mais baixo* do que 1: côncavo
  * p é *maior* do que 1: convexo\
    Valores interessantes:\
    *- 1.0*: Distância de Manhattan\
    *- 2.0*: distância euclidiana\
    *- Infinito*: distância de Chebyshev\
    *Observação*: este parâmetro só está disponível quando o parâmetro **Modo de Distância** está definido como *Minkowski*.
* **Modo Combinar** *Inteiro*\
  Define o método de mesclagem dos valores de *células sobrepostas* no espaço:
  * *Adicionar*: adicione os valores
  * *Máx*: manter o valor *mais alto*
  * *Mín*: manter o valor *mais baixo*
* **Estilo** *Inteiro* Define o método *renderizando os dados* do ruído fractal de Voronoi, considerando que o ruído é baseado em um conjunto de pontos no espaço:
  * *F1*: a distância até o *ponto mais próximo* no espaço
  * *F2*: a distância até o *segundo ponto mais próximo* no espaço
  * *F2-F1*- *F1\* F2 *-* F1/F2 *-* Borda *: a* borda entre cada célula* do ruído no espaço
  * *Cor aleatória*: atribua uma *cor simples aleatória* a cada célula do ruído no espaço
* **Thickness de borda** *Precisão decimal* Ajusta o thickness das bordas detectadas entre as células do ruído fractal de Voronoi. As bordas são detectadas nos eixos X, Y e Z, portanto, algumas espessuras podem aumentar mais rapidamente do que outras, dependendo da *profundidade* das células.\
  *Observação*: este parâmetro só está disponível quando o parâmetro **Estilo** está definido como *Borda*.
* **Modo De Semente De Cor Aleatória** *Inteiro*\
  Define o método de *aquisição* da semente aleatória para a seleção de cores por célula:
  * *Propagação Aleatória Global*: usar a propagação *herdada* pelo nó
  * *Propagação manual*: usar uma *semente discreta*\
    *Observação*: este parâmetro só está disponível quando o parâmetro **Estilo** está definido como *Cor aleatória*.
* **Semente de Cor Aleatória** *Inteiro*\
  A semente aleatória discreta que deve ser usada para a seleção de cores por célula.\
  *Observação*: este parâmetro só está disponível quando o parâmetro **Estilo** está definido como *Cor aleatória* e o parâmetro **Modo de Distribuição de Cor Aleatória** está definido como *Distribuição Manual*.
* **Habilitar divisão em blocos** *Booleano*\
  Ajusta o ruído fractal de Voronoi de modo que o padrão resultante *se repita* nos eixos X, Y e Z.

## Imagens de exemplo

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/fractal-voronoi-sea.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/fractal-voronoi-scifi-panel.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant6.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoifractal-variant4.jpg){width="256px"}

</td>
</tr>
</table>
