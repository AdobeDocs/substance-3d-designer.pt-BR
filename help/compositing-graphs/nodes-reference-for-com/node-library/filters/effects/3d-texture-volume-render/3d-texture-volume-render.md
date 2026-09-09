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
source-git-commit: 132a27ad47b0272a877b913eaa7957ccf8b549fd
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---


# Renderização de volume de textura 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-texture-volume-render.resources/3dtexturevolumerender.png){width="200px"}

<b>Entrada:</b> Filtro > Efeito

</td>
<td width="100.00%" style="border: 0;" valign="top">

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

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Campo de distância sinalizado 3D</b> <i>Tons de cinza</i> | A imagem 4096x4096 que representa as 256 <i>fatias</i> do <i>campo de distância assinado</i> de uma forma, organizada em uma grade de 16x16.<br>Você pode usar o nó [SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) de Textura 3D para calcular o campo de distância assinada para uma textura 3D de 256 fatias. |
| <b>Densidade</b> <i>Tons de cinza</i> | A imagem 4096x4096 que representa as 256 <i>fatias</i> de <i>densidade</i> de uma forma, organizadas em uma grade de 16x16. A densidade é mapeada usando valores em tons de cinza de 0 (totalmente transparente) a 1 (totalmente opaco).<br>Você pode usar a [Máscara de Volume 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md) ou os nós de ruído 3D ([Ruído de Perlin 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md), [Voronoi 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-voronoi/3d-voronoi.md), [Fractal de Ruído Ondulado 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-ridged-noise-fractal/3d-ridged-noise-fractal.md), etc.), combinados com um nó de [Posição de Textura 3D](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-position/3d-texture-position.md) como entrada de posição, para gerar uma máscara de volume como uma textura 3D de 256 fatias. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Resolução de Saída</b> <i>Inteiro2</i> | A resolução da imagem de saída em <b>X</b> e <b>Y</b>, expressa como uma <i>potência de dois</i>. |
| <b>Posição da Câmera</b> <i>Flutuante2</i> | A posição da câmera ao redor da forma.<br>Quando o nó for selecionado, você poderá usar o gizmo de posição no <b>Visualização 2D</b> para <i>orbitar</i> a câmera. |
| <b>Posição da luz</b> <i>Flutuante2</i> | A posição da <i>luz direcional</i> ao redor da forma.<br>Quando o nó for selecionado, você poderá usar o cursor de posição no <b>Visualização 2D</b> para <i>orbitar</i> a fonte de luz. |
| <b>Distância da câmera</b> <i>Flutuante</i> | A distância da câmera até a forma. |
| <b>CDV de câmera</b> <i>Flutuante</i> | O campo de visualização da câmera em <i>graus</i>. |
| <b>Absorção</b> <i>Flutuante</i> | Ajusta a quantidade de luz que é absorvida à medida que passa <i>pelo</i> volume. |
| <b>Difusão</b> <i>Flutuante</i> | Multiplica o valor fornecido pela entrada <b>Densidade</b> pelo valor de campo de distância <i>interna</i>.<br>Isso ajusta efetivamente a largura do <i>gradiente de atenuação</i> do limite externo do volume para dentro. |
| <b>Modo de Cores Claras</b> <i>Inteiro</i> | Define o método de aquisição da cor da luz direcional:<br>- <i>Temperatura (Kelvin)</i>: A cor resulta da temperatura da luz, em que um valor <i>menor</i> resulta em uma cor <i>mais quente</i><br>- <i>Cor de RGB</i>: defina a cor usando valores de RGB |
| <b>Temperatura da luz (Kelvin)</b> <i>Flutuante</i> | A temperatura da luz direcional, que afeta sua <i>cor</i>. Um valor <i>mais baixo</i> resulta em uma cor <i>mais quente</i>.<br>Valores úteis:<br>1800 K - Luz de vela<br>2800 K - Lâmpada incandescente<br>5500 K - Luz do dia<br>6200 K - Branco natural<br>7000 K - Céu nublado<br><i>Observação</i>: este parâmetro só está disponível quando o parâmetro <b>Modo de cor clara</b> está definido como <i>Temperatura (Kelvin)</i>. |
| <b>Cor clara</b> <i>Flutuante3</i> | A cor da luz direcional.<br><i>Observação</i>: este parâmetro só está disponível quando o parâmetro <b>Modo de Cor de Luz</b> está definido como <i>Cor de RGB</i>. |
| <b>Intensidade da luz</b> <i>Flutuante</i> | A intensidade da luz direcional. |
| <b>Cor do ambiente</b> <i>Flutuante3</i> | A cor da claraboia ambiente. |
| <b>Intensidade do ambiente</b> <i>Flutuante</i> | A intensidade da claraboia ambiente. |
| <b>Albedo</b> <i>Flutuante3</i> | A cor do albedo do volume. |
| <b>Modo de Tela de Fundo</b> <i>Inteiro</i> | O método de sombreamento do plano de fundo da cena renderizada, com base na <b>Cor do Plano de Fundo</b>:<br>- <i>Sombreada</i>: a cor é afetada pela <i>cor</i> e pela <i>intensidade</i><br>- <i>Cor Constante</i> da luz direcional: a cor é aplicada uniformemente <i>independentemente</i> da luz direcional |
| <b>Cor do plano de fundo</b> <i>Flutuante4</i> | A cor usada para preencher o plano de fundo da cena renderizada. |
| <b>Pontilhamento</b> <i>Flutuante</i> | Ajusta a intensidade do <i>pontilhamento de ruído azul</i> usado para suavizar o sombreamento. |
| <b>Habilitar Plano Terrestre</b> <i>Booleano</i> | Quando <i>True</i>, renderiza um plano terrestre <i>infinito</i>. O <i>cubo de unidade</i> que inclui a forma está neste plano. |
| <b>Plano infinito</b> <i>Booleano</i> | Define o plano do solo para <i>se estender infinitamente</i> até o horizonte.<br><i>Observação</i>: este parâmetro só está disponível quando o parâmetro <b>Habilitar plano do solo</b> está definido como <i>Verdadeiro</i>. |
| <b>Tamanho do plano terrestre</b> <i>Precisão decimal 2</i> | Ajusta o tamanho do plano terrestre.<br><i>Observação</i>: este parâmetro só está disponível quando o parâmetro <b>Habilitar plano terrestre</b> está definido como <i>Verdadeiro</i> e o parâmetro <b>Plano infinito</b> está definido como <i>Falso</i>. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3dtexturevolumerender-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3dtexturevolumerender-variant5.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3dtexturevolumerender-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3dtexturevolumerender-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3dtexturevolumerender-variant4.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3dtexturevolumerender-node.png" />
        </td>
    </tr>
</table>
