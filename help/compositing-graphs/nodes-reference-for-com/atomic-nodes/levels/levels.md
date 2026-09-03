---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/levels.html"
breadcrumb-title: ''
description: Use o nó Níveis para ajustar o brilho, o contraste e a gama tonal das texturas para correção e aprimoramento de cores.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Levels
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Níveis
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 4%

---


# Níveis

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: Níveis](levels.resources/levels-01.png "Nó atômico: Níveis"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Ajusta o intervalo global e o equilíbrio de cores das sombras, tons médios e destaques de uma imagem.

O nó Níveis permite remapear os tons de uma entrada definindo fatores de remapeamento de entrada e saída, apresentados em uma interface de histograma familiar de outros editores de imagem 2D.

</td>
</tr>
</table>

É um dos nós principais e mais úteis do Substance 3D Designer e é frequentemente usado para remapear e ajustar valores em um gráfico, pois fornece a interface mais precisa e precisa para alterar valores.

Embora seja um nó importante, em alguns casos de uso, a interface pode ser um pouco incômoda, portanto, verifique se há alternativas nos [Níveis automáticos](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md), na [Contraste/Luminosidade](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/contrast-luminosity/contrast-luminosity.md) e na [Verificação de histograma](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md).

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

## Exemplos

## Parâmetros

O nó oferece duas interfaces para ajustar seus valores: histograma e controles deslizantes. Você pode alternar entre eles com o botão mais à direita na barra de cabeçalho “Parâmetros específicos”:

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

O botão amarelo realçado alterna a interface entre os controles deslizantes (inferiores) de valor do histograma (superior)

</td>
<td width="66.67%" style="border: 0;" valign="top">

![](levels.resources/levels-02.png)

![](levels.resources/levels-03.png)

</td>
</tr>
</table>

|  |  |
| --- | --- |
| <b>Nível no baixo</b> *Flutuante/Flutuante4* | Define os níveis de luz baixa da imagem de entrada. Mapeia novamente os valores de Entrada baixos para ficarem totalmente pretos. |
| <b>Nível no alto</b> *Flutuante/Flutuante4* | Define os níveis de realce da imagem de entrada.  Mapeia novamente os valores de entrada Altos para um branco completo. |
| <b>Nível no meio</b> *Flutuante/Flutuante4* | Define os níveis de tons médios da imagem de entrada.  Mapeia novamente os valores de entrada do Meio para se tornarem cinza médio. |
| <b>Nivelar abaixo</b> *Flutuante/Flutuante4* | Define os níveis de luz baixa da imagem de saída.  Agrava os valores de saída de Preto para definir o limite. |
| <b>Nivelar acima</b> *Flutuante/Flutuante4* | Define os níveis de realce da imagem de saída.  Restringe os valores de branco de saída para definir o limite. |
| <b>Pincel intermediário</b> *Booleano* | Determina se o valor de entrada transformado é fixado a [0, 1] antes do cálculo do nível de saída. |

## Guia de uso

Confira esta visão geral em vídeo do nó Níveis e seu editor de histograma:

### Ações rápidas

Na barra de cabeçalho &#39;Parâmetros específicos&#39;, você pode encontrar botões para acessar funções convenientes do histograma:

![Ações rápidas do nó de níveis](levels.resources/levels-04.png "Ações rápidas do nó de níveis")

<b>1 - Inverter:</b> alterna os valores dos parâmetros &#39;Nível para baixo&#39; e &#39;Nível da saída do realce&#39;.

<b>2 - Nível automático:</b> ajusta automaticamente os valores dos parâmetros &#39;Nivel em sombras&#39; e &#39;Nivel em realce&#39; respectivamente para o valor mais baixo e mais alto presente na imagem.

<b>3 - Interfaces de alternância:</b> alterna entre os editores do histograma e do controle deslizante.

### Histograma

O editor de histograma é destinado a ajustes visuais rápidos em que valores precisos não são realmente necessários e a exposição de parâmetros não é importante. Geralmente, é a maneira mais rápida e fácil de trabalhar com Níveis.

![](levels.resources/levels-05.gif)

Dependendo do tipo de entrada (Cor ou Tons de cinza), é possível usar a lista suspensa acima do Histograma para escolher o canal que será modificado.

### Controles deslizantes

O editor de controles deslizantes elimina qualquer editor visual e apresenta apenas controles deslizantes numéricos, úteis principalmente se você quiser fixar ou remapear para valores muito exatos, ou se você pretende [expor qualquer um desses parâmetros](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md), pois isso só é possível no editor de controles deslizantes.

Os controles deslizantes mudam dependendo de uma entrada Colorida ou Tons de cinza: as entradas de cor criam 4 controles deslizantes para cada canal RGBA separadamente. O Tons de cinza tem apenas um único controle deslizante, facilitando o trabalho com ele. Veja a listagem de Parâmetros acima para obter uma explicação sobre cada controle deslizante.

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
