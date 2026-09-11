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
source-git-commit: db5ad9a6ad1d03fedcc3d760cc8886501d16b87f
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 0%

---


# Voronoi

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](voronoi.resources/voronoi.png){width="200px"}

<b>Entrada:</b> Geradores de Textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O nó **Voronoi** gera um ruído Voronoi 3D mapeado para uma imagem 2D usando uma *projeção ortográfica Z-down*.

Este nó pode ser testado com [GBuffers de Cubo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) como entrada em vez de um mapa baked real (como visto na Imagem de Exemplo abaixo).

>[!WARNING]
>
> Este ruído deve ser usado somente com o *mecanismo de GPU* (por exemplo, **Direct** ou **OpenGL**). Vá para **Ferramentas > Alternar mecanismo...** ou pressione a tecla **F9** para selecionar o mecanismo desejado.

</td>
</tr>
</table>

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Inverter</b> <i>Booleano</i> | Inverte a imagem de saída. |
| <b>Escala</b> <i>Flutuante</i> | Controla a escala do ruído de Voronoi.<br><br>*Observação*: quando o **Enquadramento** está habilitado em *qualquer eixo*, o ajuste de escala é *escalonado*. Isso é esperado. |
| <b>Tamanho</b> <i>Flutuante3</i> | Controla o tamanho do ruído de Voronoi nos eixos **X**, **Y** e **Z**. Valores não uniformes resultam em um efeito de *esticamento ou esmagamento*.<br><br>*Observação*: quando a opção **Lado a lado** está habilitada em *qualquer eixo*, o ajuste de tamanho é *escalonado*. Isso é esperado. |
| <b>Deslocamento</b> <i>Flutuante3</i> | Aplica um deslocamento à *posição* do ruído de Voronoi nos eixos **X**, **Y** e **Z**. |
| <b>Desordem</b> <i>Flutuante3</i> | A intensidade do *deslocamento aleatório* aplicado a cada ponto do ruído nos eixos **X**, **Y** e **Z**. |
| <b>Intensidade de Distorção</b> <i>Flutuante</i> | Controla a intensidade de um *efeito de distorção* aplicado no ruído de Voronoi. |
| <b>Multiplicador de Escala de Distorção</b> <i>Flutuante</i> | Controla a escala do *padrão de deformação* usado no efeito de distorção controlado pela **Intensidade de Distorção**. |
| <b>Curva arredondada</b> <i>Flutuante</i> | Arredonda a *inclinação* em torno de cada ponto do ruído para torná-lo *convexo*.<br><br>*Observação*: este parâmetro não está disponível quando o parâmetro **Style** está definido como *Borda*. |
| <b>Escala de distância</b> <i>Flutuante</i> | Ajusta a *distância do gradiente* ao redor de cada ponto do ruído. |
| <b>Modo de Distância</b> <i>Inteiro</i> | Define o método para *calcular o gradiente de distância* em torno de cada ponto do ruído:<br><br>- *Euclidiano*<br>- *Manhattan*<br>- *Chebyshev*<br>- *Minkowski* |
| <b>Número de Minkowski</b> <i>Flutuante</i> | A ordem *p* da distância de Minkowski. Se dividirmos o gradiente de distância em quadrantes, esse número afetará esses quadrantes da seguinte maneira:<br><br>- p é *exatamente* 1: reto<br>- p é *inferior* a 1: côncavo<br>- p é *maior* do que 1: Convexo<br><br>Valores interessantes:<br><br>- *1.0*: distância de Manhattan<br>- *2.0*: distância euclidiana<br>- *Infinito*: distância de Chebyshev <br><br>*Observação*: este parâmetro só está disponível quando o parâmetro **Modo de distância** está definido como *Minkowski*. |
| <b>Estilo</b> <i>Inteiro</i> | Define o método *renderizando os dados* do ruído de Voronoi, considerando que o ruído é baseado em um conjunto de pontos no espaço:<br><br>- *F1*: a distância ao *ponto mais próximo* no espaço<br>- *F2*: a distância ao *segundo ponto mais próximo* no espaço<br>- *F2-F1*<br>- *F1\* F2 *<br>-* F1/F2 *<br>-* Borda *: a* borda entre cada célula *do ruído no espaço<br>-* Cor aleatória *: atribuir uma* cor simples aleatória* a cada célula do ruído no espaço |
| <b>Thickness de borda</b> <i>Flutuante</i> | Ajusta o thickness das bordas detectadas entre células do ruído de Voronoi. As bordas são detectadas nos eixos X, Y e Z, portanto, algumas espessuras podem aumentar mais rapidamente do que outras, dependendo da *profundidade* das células.<br><br>*Observação*: este parâmetro só está disponível quando o parâmetro **Estilo** está definido como *Borda*. |
| <b>Modo de Distribuição de Cores Aleatórias</b> <i>Inteiro</i> | Define o método de *aquisição* da semente aleatória para a seleção de cores por célula:<br><br>- *Distribuição aleatória global*: usar a semente *herdada* pelo nó<br>- *Distribuição manual*: usar uma semente *discreta*<br><br>*Observação*: este parâmetro só está disponível quando o parâmetro **Estilo** está definido como *Cor aleatória*. |
| <b>Semente de Cor Aleatória</b> <i>Inteiro</i> | A semente aleatória discreta que deve ser usada para a seleção de cores por célula.<br><br>*Observação*: este parâmetro só está disponível quando o parâmetro **Style** está definido como *Cor aleatória* e o parâmetro **Modo de Distribuição de Cor Aleatória** está definido como ***Distribuição Manual***. |
| <b>Expansão não quadrada</b> <i>Booleano</i> | Permite a compensação de esmagamento e alongamento com proporções não quadradas. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-variant5.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-variant4.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="voronoi.resources/voronoi-variant6.jpg" />
        </td>
    </tr>
</table>
