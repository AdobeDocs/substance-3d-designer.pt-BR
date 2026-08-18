---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/curve.html"
breadcrumb-title: ''
description: Use o nó Curva para ajustar os valores de textura usando curvas personalizáveis para um controle preciso de cor e brilho.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Curve
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Curva
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 2%

---


# Curva

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: curva](../../../../assets/comp_curve_1.png "Nó atômico: curva"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Remapeia os valores em uma imagem usando uma curva personalizada.

O nó fornece uma interface para o remapeamento de tonalidade de imagem, semelhante a outros aplicativos de edição de imagem 2D. O usuário pode colocar pontos e ajustar curvas de Bézier para remapear a entrada, que pode ser em tons de cinza ou colorida.É especialmente útil quando usado com transições de gradiente para remapeá-los para um perfil de height específico; permite uma modelagem muito precisa de perfis de chanfro e semelhantes.

</td>
</tr>
</table>

Ao contrário da maioria dos outros nós, o nó Curva não tem uma interface padrão típica com controles deslizantes e parâmetros, mas em vez disso apresenta um editor de curva completo. Consulte a seção expansível abaixo sobre como usá-lo.

[No entanto, isso significa que nenhum dos parâmetros de um nó de Curva pode ser exposto a um subgrafo](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md). A única opção aqui é usar uma [Chave Múltipla](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md) para alternar entre diferentes perfis de curva.

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Parâmetros

### Editor de curva

</td>
<td style="border: 0;" valign="top">

### Conectores de entrada

### Conectores de saída

</td>
<td style="border: 0;" valign="top">

### Exemplos

</td>
</tr>
</table>

## Parâmetros

|  |  |
| --- | --- |
| <b>Aplicar/Expor curva</b> *Booleano* | Permite copiar a curva do usuário para a saída em vez de aplicá-la à imagem de entrada |
| <b>Endereçamento de curva</b> *Booleano* | Esse parâmetro determina como os pixels HDR fora do intervalo [0, 1] na entrada são tratados: apertados ou dobrados até [0, 1]. |
| <b>Curva</b> *Matriz de chaves curvas* | A curva personalizada usada para mapear os valores de tons de cinza de entrada.   Pode ser editado usando o [Editor de curvas](#curve-editor). |

## Editor de curva

### Criar e mover um ponto

Para criar um ponto, basta clicar duas vezes em qualquer lugar na Visualização de curva:

![](../../../../assets/createmovepoint.gif)

### Controle da influência do ponto

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Para obter resultados precisos, os nós curvos oferecem modos diferentes para cada ponto:

</td>
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../assets/image2017-2-17-14-5-36.png)

</td>
</tr>
</table>

![](../../../../assets/image2017-2-17-14-13-27.png) Redefina o modo de ponto para o valor padrão.

![](../../../../assets/image2017-2-17-14-12-6.png) Bloqueie/desbloqueie os 2 manipuladores de bézier para que o usuário possa movê-los juntos ou independentemente.

![](../../../../assets/image2017-2-17-14-14-0.png) Ambos os lados do ponto são controlados por um manipulador de Bezier.

![](../../../../assets/image2017-2-17-14-16-22.png) O lado direito do ponto é controlado por um manipulador de Bezier enquanto o lado esquerdo permanece plano.

![](../../../../assets/image2017-2-17-14-18-25.png) O lado esquerdo do ponto é controlado por um manipulador de Bezier enquanto o lado direito permanece plano.

![](../../../../assets/image2017-2-17-14-19-32.png) Os lados do ponto permanecem planos

![](../../../../assets/curvepointsmodes.gif)

### Mostrar histograma de entrada

Você pode mostrar/ocultar o histograma de sua entrada apenas clicando em ![](../../../../assets/image2017-2-17-14-50-13.png)

![](../../../../assets/image2017-2-17-14-48-35.png)

### Controle de cada canal individualmente (entrada de cores)

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Quando a entrada é um nó de cor, você pode ajustar a curva para cada canal:

Basta selecionar a curva que deseja ajustar na lista suspensa localizada na parte superior direita:

</td>
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../assets/image2017-2-17-14-52-43.png)

</td>
</tr>
</table>

No modo de curva de RGB, você pode ocultar/mostrar as curvas de canais individuais pressionando/despressionando ![](../../../../assets/image2017-2-17-14-55-0.png):

![](../../../../assets/image2017-2-17-14-55-38.png)

### Alinhamento, espelhamento e inversão

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Se você clicar com o botão direito do mouse na vista de curva, irá obter mais algumas opções.

<b>Alinhar parte superior:</b> alinhe os pontos selecionados horizontalmente com o mais alto.

<b>Alinhar ao meio:</b> alinhe os pontos selecionados horizontalmente ao height médio da seleção.

<b>Alinhar abaixo:</b> alinhe os pontos selecionados horizontalmente com o mais baixo.

</td>
<td width="50.00%" style="border: 0;" valign="top">

![](../../../../assets/image2017-6-27-16-11-9.png)

</td>
</tr>
</table>

<b>Distribuir horizontalmente/verticalmente:</b> Distribuir os pontos no eixo selecionado

<b>Virar horizontalmente/verticalmente:</b> vire os pontos selecionados de acordo com o eixo selecionado.

<b>Espelhar horizontalmente/verticalmente:</b> espelha a curva inteira, de acordo com o eixo selecionado

### Atalhos de teclado

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>LMB + arrastar</b>

Desenhe uma caixa de seleção.

</td>
<td style="border: 0;" valign="top">

![](../../../../assets/ctrl.gif)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Shift + arrastar</b>

Restringir o movimento nos eixos X ou Y.

</td>
<td style="border: 0;" valign="top">

![](../../../../assets/shift.gif)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Alt + LMB + arrastar</b>

Quebre temporariamente as alças para movê-las de forma independente.

</td>
<td style="border: 0;" valign="top">

![](../../../../assets/altclick.gif)

</td>
</tr>
</table>

### Ajustar o enquadramento da curva

Ao ajustar os manipuladores, você pode estar no caso em que um manipulador está passando sobre a visualização da curva.

Nesse caso, você pode usar o botão ![](../../../../assets/image2017-2-20-19-11-53.png) para ajustar o tamanho ao conteúdo.

O botão ![](../../../../assets/image2017-2-20-19-12-45.png) redefine o nível de zoom como 1

![](../../../../assets/viewzoom.gif)

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Tons de Cinza/Cor* PRIMÁRIO | A imagem a ser processada. |

## Conectores de saída

|  |  |
| --- | --- |
| <b>Saída</b> *Tons de cinza/Cor* |  |

## Exemplos

*Em breve.*
