---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise-fractal.html"
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
source-git-commit: 10884d1625fcdcebcbdfd7fbed776453c4f1267a
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---


# Fractal de ruído Perlin 3D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-perlin-noise-fractal.resources/3dperlinnoisefractal.png){width="200px"}

<b>Entrada:</b> Geradores de Textura > Ruídos

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Descrição

O nó <b>Fractal de Ruído Perlin 3D</b> gera um ruído Perlin <i>fractal</i> no espaço 3D com base na entrada do <b>Mapa de Posições</b>.

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
| <b>Escala</b> <i>Flutuante</i> | Controla a escala do ruído fractal de Perlin 3D. |
| <b>Tamanho</b> <i>Flutuante3</i> | Controla o tamanho do ruído fractal de Perlin 3D nos eixos <b>X</b>, <b>Y</b> e <b>Z</b>. Valores não uniformes resultam em um efeito de <i>amplificação ou esmagamento</i>. |
| <b>Deslocamento</b> <i>Flutuante3</i> | Aplica um deslocamento à <i>posição</i> do ruído fractal de Perlin 3D nos eixos <b>X</b>, <b>Y</b> e <b>Z</b>. |
| <b>Intensidade de Distorção</b> <i>Flutuante</i> | Controla a intensidade de um <i>efeito de distorção</i> aplicado no ruído fractal de Perlin 3D. |
| <b>Multiplicador de Escala de Distorção</b> <i>Flutuante</i> | Controla a escala do <i>padrão de deformação</i> usado no efeito de distorção controlado pela <b>Intensidade de Distorção</b>. |
| <b>Nível Mínimo</b> <i>Inteiro</i> | O <i>nível mínimo de repetição</i> usado no padrão fractal. Um intervalo mínimo/máximo mais amplo resulta em um <i>padrão mais rico</i> com variação em intervalos de frequência mais amplos. |
| <b>Nível Máximo</b> <i>Inteiro</i> | O <i>nível máximo de repetição</i> usado no padrão fractal. Um intervalo mínimo/máximo mais amplo resulta em um <i>padrão mais rico</i> com variação em intervalos de frequência mais amplos. |
| <b>Aspereza</b> <i>Flutuante</i> | Controla o <i>equilíbrio</i> entre <i>níveis de repetição</i> baixos e altos no padrão fractal.<br><br><i>Observação</i>: um valor de <b>0</b> resulta em uma saída <i>não alinhada</i> com outros valores baixos que o seguem. Isso é esperado. |
| <b>Lacunaridades</b> <i>Flutuante</i> | Controla como o padrão fractal <i>aplicado preenche o espaço</i>. Um valor <i>mais alto</i> resulta em <i>menos lacunas</i> no padrão e em um ruído <i>mais denso</i>. |
| <b>Opacidade Global</b> <i>Flutuante</i> | Controla o <i>intervalo</i> dos valores de ruído fractais de Perlin 3D <i>ao redor</i> do valor de <b>Linha de base</b>. |
| <b>Linha de base</b> <i>Flutuante</i> | Aplica um <i>deslocamento</i> ao valor de <i>luminância</i> da linha de base para a distribuição do valor de ruído Perlin 3D. |
| <b>Contraste</b> <i>Flutuante</i> | Ajusta o contraste do ruído de Perlin 3D. |
| <b>Absoluto</b> <i>Booleano</i> | Usa valores absolutos no ruído Perlin 3D. Isso efetivamente <i>inverte</i> a distribuição de valores <i>abaixo de 0,5</i>. |
| <b>Habilitar divisão em blocos</b> <i>Booleano</i> | Ajusta o ruído de Perlin 3D para que seu padrão resultante <i>se repita</i> nos eixos X, Y e Z. |

## Exemplos

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise-fractal.resources/3dfractal.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise-fractal.resources/3dperlinnoisefractal-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-perlin-noise-fractal.resources/3dperlinnoisefractal-variant2.jpg" />
        </td>
    </tr>
</table>
