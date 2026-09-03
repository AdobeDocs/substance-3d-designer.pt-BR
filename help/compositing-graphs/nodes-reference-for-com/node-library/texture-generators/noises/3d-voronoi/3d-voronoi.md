---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-voronoi.html"
breadcrumb-title: ''
description: Use o nó Voronoi 3D para gerar padrões Voronoi com base na posição mundial 3D para criar texturas celulares volumétricas.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Voronoi
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Voronoi 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---


# Voronoi 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-voronoi.resources/3d-voronoi-01.png){width="200px"}

<b>Entrada:</b> Geradores de Textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O nó <b>Voronoi 3D</b> gera um ruído Voronoi no espaço 3D com base na entrada do <b>Mapa de Posição</b>.

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
| <b>Escala</b> <i>Flutuante</i> | Controla a escala do ruído de Voronoi 3D.<br><br><i>Observação</i>: quando o <b>Enquadramento</b> está habilitado em <i>qualquer eixo</i>, o ajuste de escala é <i>escalonado</i>. Isso é esperado. |
| <b>Tamanho</b> <i>Flutuante3</i> | Controla o tamanho do ruído de Voronoi 3D nos eixos <b>X</b>, <b>Y</b> e <b>Z</b>. Valores não uniformes resultam em um efeito de <i>esticamento ou esmagamento</i>.<br><br><i>Observação</i>: quando a opção <b>Lado a lado</b> está habilitada em <i>qualquer eixo</i>, o ajuste de tamanho é <i>escalonado</i>. Isso é esperado. |
| <b>Deslocamento</b> <i>Flutuante3</i> | Aplica um deslocamento à <i>posição</i> do ruído Voronoi 3D nos eixos <b>X</b>, <b>Y</b> e <b>Z</b>. |
| <b>Desordem</b> <i>Flutuante3</i> | A intensidade do <i>deslocamento aleatório</i> aplicado a cada ponto do ruído nos eixos <b>X</b>, <b>Y</b> e <b>Z</b>. |
| <b>Intensidade de Distorção</b> <i>Flutuante</i> | Controla a intensidade de um <i>efeito de distorção</i> aplicado no ruído Voronoi 3D. |
| <b>Multiplicador de Escala de Distorção</b> <i>Flutuante</i> | Controla a escala do <i>padrão de deformação</i> usado no efeito de distorção controlado pela <b>Intensidade de Distorção</b>. |
| <b>Curva arredondada</b> <i>Flutuante</i> | Arredonda a <i>inclinação</i> em torno de cada ponto do ruído para torná-lo <i>convexo</i>.<br><br><i>Observação</i>: este parâmetro não está disponível quando o parâmetro <b>Style</b> está definido como <i>Borda</i>. |
| <b>Escala de distância</b> <i>Flutuante</i> | Ajusta a <i>distância do gradiente</i> ao redor de cada ponto do ruído. |
| <b>Modo de Distância</b> <i>Inteiro</i> | Define o método para <i>calcular o gradiente de distância</i> em torno de cada ponto do ruído:<br><br>- <i>Euclidiano</i><br>- <i>Manhattan</i><br>- <i>Chebyshev</i><br>- <i>Minkowski</i> |
| <b>Número de Minkowski</b> <i>Flutuante</i> | A ordem <i>p</i> da distância de Minkowski. Se dividirmos o gradiente de distância em quadrantes, esse número afetará esses quadrantes da seguinte maneira:<br><br>- p é <i>exatamente</i> 1: reto<br>- p é <i>inferior</i> a 1: côncavo<br>- p é <i>maior</i> do que 1: Convexo<br><br>Valores interessantes:<br>- <i>1.0</i>: distância de Manhattan<br>- <i>2.0</i>: distância euclidiana<br>- <i>Infinito</i>: distância de Chebyshev<br><br><i>Observação</i>: este parâmetro só está disponível quando o parâmetro <b>Modo de distância</b> está definido como <i>Minkowski</i>. |
| <b>Estilo</b> <i>Inteiro</i> | Define o método <i>renderizando os dados</i> do ruído Voronoi 3D, considerando que o ruído é baseado em um conjunto de pontos no espaço 3D:<br><br>- <i>F1</i>: a distância ao <i>ponto mais próximo</i> no espaço 3D<br>- <i>F2</i>: a distância ao <i>segundo ponto mais próximo</i> no espaço 3D<br>- <i>F2-F1</i><br>- <i>F1\*F2</i><br>- <i>F1/F2</i><br>- <i>Borda</i>: a <i>borda entre cada célula</i> do ruído no espaço 3D<br>- <i>Cor aleatória</i>: atribuir uma <i>cor simples aleatória</i> a cada célula do ruído no espaço 3D |
| <b>Thickness de borda</b> <i>Flutuante</i> | Ajusta o thickness das bordas detectadas entre células do ruído Voronoi 3D. As bordas são detectadas nos eixos X, Y e Z, portanto, algumas espessuras podem aumentar mais rapidamente do que outras, dependendo da <i>profundidade</i> das células.<br><br><i>Observação</i>: este parâmetro só está disponível quando o parâmetro <b>Estilo</b> está definido como <i>Borda</i>. |
| <b>Habilitar divisão em blocos</b> <i>Booleano</i> | Ajusta o ruído Voronoi 3D de modo que o padrão resultante <i>se repita</i> nos eixos X, Y e Z. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3d-voronoi-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3d-voronoi-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3d-voronoi-04.jpg" />
        </td>
    </tr>
    <tr style="border: 0; background: transparent">
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3d-voronoi-05.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3d-voronoi-06.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-voronoi.resources/3d-voronoi-07.jpg" />
        </td>
    </tr>
</table>
