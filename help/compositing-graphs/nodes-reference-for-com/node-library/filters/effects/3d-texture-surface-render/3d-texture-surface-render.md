---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-surface-render.html"
breadcrumb-title: ''
description: Use o nó Renderização de superfície de textura 3D para renderizar texturas de superfície a partir de dados 3D para criar efeitos de superfície de procedimento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Surface Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Renderização de superfície de textura 3D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 132a27ad47b0272a877b913eaa7957ccf8b549fd
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---


# Renderização de superfície de textura 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-texture-surface-render.resources/3dtexturesurfacerender.png){width="200px"}

<b>Entrada:</b> Filtro > Efeito

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O nó **Renderização de superfície de textura 3D** renderiza a superfície de uma forma descrita por uma *textura 3D*, usando seu *campo de distância* correspondente da entrada de imagem do **Campo de distância 3D**.

A superfície é representada dentro dos limites de um *cubo de unidade*. A iluminação é calculada usando a imagem de entrada **Ambiente** mapeada para uma esfera infinita.

>[!NOTE]
>
> O campo de distância deve ser uma textura **4096x4096** que descreve a forma com uma grade **16x16** de 256 fatias.\
> Você pode usar o nó [SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) de Textura 3D para calcular o campo de distância para uma textura 3D de 256 fatias.

</td>
</tr>
</table>

<a name="inputs"></a>

## Entradas

|  |  |
|:---|:---|
| <b>Campo de distância 3D</b> <i>Tons de cinza</i> | A imagem 4096x4096 que representa as 256 <i>fatias</i> do <i>campo de distância</i> de uma forma, organizadas em uma grade de 16x16.<br>Você pode usar o nó [SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md) de Textura 3D para calcular o campo de distância para uma textura 3D de 256 fatias. |
| <b>Ambiente</b> <i>Cor</i> | A imagem que representa o <i>ambiente</i>, que deve ser mapeado para uma esfera infinita na renderização e usado para computar a <i>iluminação</i>.<br>A imagem também é usada para renderizar o plano de fundo da cena quando o parâmetro <b>Modo do Plano de Fundo</b> está definido como <i>Ambiente</i> ou <i>Ambiente</i>. |

<a name="parameters"></a>

## Parâmetros

|  |  |
|:---|:---|
| <b>Resolução de Saída</b> <i>Inteiro2</i> | A resolução da imagem de saída em <b>X</b> e <b>Y</b>, expressa como uma <i>potência de dois</i>. |
| <b>Posição da Câmera</b> <i>Flutuante2</i> | A posição da câmera ao redor da forma.<br>Quando o nó for selecionado, você poderá usar o gizmo de posição no <b>Visualização 2D</b> para <i>orbitar</i> a câmera. |
| <b>Distância da câmera</b> <i>Flutuante</i> | A distância da câmera até a forma. |
| <b>CDV de câmera</b> <i>Flutuante</i> | O campo de visualização da câmera em <i>graus</i>. |
| <b>Albedo</b> <i>Flutuante3</i> | A cor do albedo da superfície da forma. |
| <b>Modo de Tela de Fundo</b> <i>Inteiro</i> | O método de representar o plano de fundo da cena renderizada:<br>- <i>Irradiância do solo</i>: a irradiância computada do plano do solo<br>- <i>Ambiente</i>: a cor ambiente da entrada de imagem do <b>Ambiente</b> mapeada para uma esfera infinita, o que é semelhante a uma versão fortemente desfocada da imagem<br>- <i>Cor uniforme</i>: preencha uniformemente o plano de fundo com uma cor especificada<br>- <i>Ambiente</i>: o Entrada de imagem do <b>ambiente</b> mapeada para uma esfera infinita |
| <b>Cor do plano de fundo</b> <i>Flutuante4</i> | A cor usada para preencher uniformemente o plano de fundo da cena renderizada.<br><i>Observação</i>: este parâmetro só está disponível quando o parâmetro <b>Modo de Plano de Fundo</b> está definido como <i>Cor uniforme</i>. |
| <b>Habilitar Plano Terrestre</b> <i>Booleano</i> | Quando <i>Verdadeiro</i>, renderiza um plano terrestre. O <i>cubo de unidade</i> que inclui a forma está neste plano. |
| <b>Plano infinito</b> <i>Booleano</i> | Define o plano do solo para <i>se estender infinitamente</i> até o horizonte.<br><i>Observação</i>: este parâmetro só está disponível quando o parâmetro <b>Habilitar plano do solo</b> está definido como <i>Verdadeiro</i>. |
| <b>Tamanho do plano terrestre</b> <i>Flutuante2</i> | Ajusta o tamanho do plano terrestre.<br><i>Observação</i>: este parâmetro só está disponível quando o parâmetro <b>Habilitar plano terrestre</b> está definido como <i>Verdadeiro</i> e o parâmetro <b>Plano infinito</b> está definido como <i>Falso</i>. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-variant4.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-surface-render.resources/3dtexturesurfacerender-node.png" />
        </td>
    </tr>
</table>
