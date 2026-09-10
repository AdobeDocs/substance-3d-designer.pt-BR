---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-voronoi-fractal.html"
breadcrumb-title: ''
description: Use o nó 3D voronoi fractal para gerar padrões Voronoi fractais com base na posição 3D para texturas volumétricas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Voronoi Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D voronoi fractal
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8be4dabbdf7bd618ca2ee21c64655952474b9df2
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---


# 3D voronoi fractal

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-voronoi-fractal.resources/3dvoronoifractal.png){width="200px"}

<b>Entrada:</b> Geradores de Textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O nó <b>3D voronoi fractal</b> gera um ruído Voronoi <i>fractal</i> no espaço 3D com base na entrada do <b>Mapa de Posições</b>.

Este nó pode ser testado com [GBuffers 3D de cubo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md) como entrada em vez de um mapa baked real (como visto na Imagem de Exemplo abaixo).

</td>
</tr>
</table>

>[!WARNING]
>
> Este ruído deve ser usado somente com o <i>mecanismo de GPU</i> (por exemplo, <b>Direct3D</b> ou <b>OpenGL</b>). Vá para <b>Ferramentas > Alternar mecanismo...</b> ou pressione a tecla <b>F9</b> para selecionar o mecanismo desejado.

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Inverter</b> <i>Booleano</i> | Inverte a imagem de saída. |
| <b>Escala</b> <i>Flutuante</i> | Controla a escala do ruído fractal de Voronoi 3D.<br><br><i>Observação</i>: quando o <b>Enquadramento</b> está habilitado em <i>qualquer eixo</i>, o ajuste de escala é <i>escalonado</i>. Isso é esperado. |
| <b>Tamanho</b> <i>Flutuante3</i> | Controla o tamanho do ruído fractal de Voronoi 3D nos eixos <b>X</b>, <b>Y</b> e <b>Z</b>. Valores não uniformes resultam em um efeito de <i>esticamento ou esmagamento</i>.<br><br><i>Observação</i>: quando a opção <b>Lado a lado</b> está habilitada em <i>qualquer eixo</i>, o ajuste de tamanho é <i>escalonado</i>. Isso é esperado. |
| <b>Deslocamento</b> <i>Flutuante3</i> | Aplica um deslocamento à <i>posição</i> do ruído fractal de Voronoi 3D nos eixos <b>X</b>, <b>Y</b> e <b>Z</b>. |
| <b>Desordem</b> <i>Flutuante3</i> | A intensidade do <i>deslocamento aleatório</i> aplicado a cada ponto do ruído nos eixos <b>X</b>, <b>Y</b> e <b>Z</b>. |
| <b>Intensidade de Distorção</b> <i>Flutuante</i> | Controla a intensidade de um <i>efeito de distorção</i> aplicado no ruído fractal de Voronoi 3D. |
| <b>Multiplicador de Escala de Distorção</b> <i>Flutuante</i> | Controla a escala do <i>padrão de deformação</i> usado no efeito de distorção controlado pela <b>Intensidade de Distorção</b>. |
| <b>Nível Mínimo</b> <i>Inteiro</i> | O <i>nível mínimo de repetição</i> usado no padrão fractal. Um intervalo mínimo/máximo mais amplo resulta em um <i>padrão mais rico</i> com variação em intervalos de frequência mais amplos. |
| <b>Nível Máximo</b> <i>Inteiro</i> | O <i>nível máximo de repetição</i> usado no padrão fractal. Um intervalo mínimo/máximo mais amplo resulta em um <i>padrão mais rico</i> com variação em intervalos de frequência mais amplos. |
| <b>Aspereza</b> <i>Flutuante</i> | Controla o <i>equilíbrio</i> entre <i>níveis de repetição</i> baixos e altos no padrão fractal.<br><br><i>Observação</i>: um valor de <b>0</b> resulta em uma saída <i>não alinhada</i> com outros valores baixos que o seguem. Isso é esperado.<br><br><i>Observação 2</i>: este parâmetro só está disponível quando o parâmetro <b>Modo de Mesclagem</b> está definido como <i>Adicionar</i>. |
| <b>Lacunaridades</b> <i>Flutuante</i> | Controla como o padrão fractal <i>aplicado preenche o espaço</i>. Um valor <i>mais alto</i> resulta em <i>menos lacunas</i> no padrão e em um ruído <i>mais denso</i>. |
| <b>Opacidade Global</b> <i>Flutuante</i> | Controla o <i>intervalo</i> dos valores de ruído fractal de Perlin 3D de 0. |
| <b>Curva arredondada</b> <i>Flutuante</i> | Arredonda a <i>inclinação</i> em torno de cada ponto do ruído para torná-lo <i>convexo</i>.<br><br><i>Observação</i>: este parâmetro não está disponível quando o parâmetro <b>Style</b> está definido como <i>Borda</i>. |
| <b>Escala de distância</b> <i>Flutuante</i> | Ajusta a <i>distância do gradiente</i> ao redor de cada ponto do ruído. |
| <b>Modo de Distância</b> <i>Inteiro</i> | Define o método para <i>calcular o gradiente de distância</i> em torno de cada ponto do ruído:<br><br>- <i>Euclidiano</i><br>- <i>Manhattan</i><br>- <i>Chebyshev</i><br>- <i>Minkowski</i> |
| <b>Número de Minkowski</b> <i>Flutuante</i> | A ordem <i>p</i> da distância de Minkowski. Se dividirmos o gradiente de distância em quadrantes, esse número afetará esses quadrantes da seguinte maneira:<br><br>- p é <i>exatamente</i> 1: reto<br>- p é <i>inferior</i> a 1: côncavo<br>- p é <i>maior</i> do que 1: Convexo<br><br>Valores interessantes:<br>- <i>1.0</i>: distância de Manhattan<br>- <i>2.0</i>: distância euclidiana<br>- <i>Infinito</i>: distância de Chebyshev<br><br><i>Observação</i>: este parâmetro só está disponível quando o parâmetro <b>Modo de distância</b> está definido como <i>Minkowski</i>. |
| <b>Modo de Mesclagem</b> <i>Inteiro</i> | Define o método de mesclagem de valores de <i>células sobrepostas</i> no espaço 3D:<br><br>- <i>Adicionar</i>: adicionar os valores<br>- <i>Máx</i>: manter o valor <i>mais alto</i><br>- <i>Mín</i>: manter o valor <i>mais baixo</i> |
| <b>Estilo</b> <i>Inteiro</i> | Define o método <i>renderizando os dados</i> do ruído fractal de Voronoi 3D, considerando que o ruído é baseado em um conjunto de pontos no espaço 3D:<br><br>- <i>F1</i>: a distância ao <i>ponto mais próximo</i> no espaço 3D<br>- <i>F2</i>: a distância ao <i>segundo ponto mais próximo</i> no espaço 3D<br>- <i>F2-F1</i><br>- <i>F1\*F2</i><br>- <i>F1/F2</i><br>- <i>Borda</i>: a <i>borda entre cada célula</i> do ruído no espaço 3D<br>- <i>Cor aleatória</i>: atribua uma <i>cor simples aleatória</i> a cada célula do ruído no espaço 3D |
| <b>Thickness de borda</b> <i>Flutuante</i> | Ajusta o thickness das bordas detectadas entre células do ruído de Voronoi 3D fractal. As bordas são detectadas nos eixos X, Y e Z, portanto, algumas espessuras podem aumentar mais rapidamente do que outras, dependendo da <i>profundidade</i> das células.<br><br><i>Observação</i>: este parâmetro só está disponível quando o parâmetro <b>Estilo</b> está definido como <i>Borda</i>. |
| <b>Habilitar divisão em blocos</b> <i>Booleano</i> | Ajusta o ruído fractal de Voronoi 3D para que seu padrão resultante <i>se repita</i> nos eixos X, Y e Z. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3dvoronoifractal-variant6.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3dvoronoifractal-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3dvoronoifractal-variant4.jpg" />
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3dvoronoifractal-variant5.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3dvoronoifractal-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi-fractal.resources/3dvoronoifractal-variant3.jpg" />
        </td>
    </tr>
</table>
