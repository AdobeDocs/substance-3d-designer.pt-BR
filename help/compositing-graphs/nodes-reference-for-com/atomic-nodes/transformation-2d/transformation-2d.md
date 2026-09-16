---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/transformation-2d.html"
breadcrumb-title: ""
description: Use o nó Transformação 2D para aplicar transformações 2D às texturas, incluindo conversão, rotação e dimensionamento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Transformation 2D
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Transformação 2D
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 5%
---

# Transformação 2D

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![Nó atômico: Transformação 2D](transformation-2d.resources/comp_transformation_1.png "Nó atômico: Transformação 2D"){width="100%"}

<b>Entrada:</b> Nós Atômicos

</td>
<td style="border: 0;" valign="top">

Aplica uma matriz de transformação 2D a uma imagem: translação, rotação, escala, simetria e distorção.

É bastante semelhante a Transformar (Ctrl-T) no Photoshop ou usar o manipulador de mapeamento 2D no Substance 3D Painter.

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="transformation-2d.resources/transformation2d-tooltip.gif" alt="dica de ferramenta de transform-2d" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

Este é um nó extremamente útil e amplamente aplicado, ele permite aumentar a divisão em blocos gráficos, remover divisão em blocos gráficos, colocar uma imagem em uma posição específica, esticar ou esmagar uma entrada, etc.

No entanto, ela não pode ser uma correspondência perfeita para determinados aplicativos, portanto, os seguintes nós podem ser de interesse: [Transformo seguro](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/safe-transform/safe-transform.md), [Transformo não quadrado](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/non-square-transform/non-square-transform.md), [Transformo quádruplo](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/quad-transform/quad-transform.md) e [Transformo Trapezoid](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/trapezoid-transform/trapezoid-transform.md).


>[!TIP]
>
> Desabilitando divisão em blocos gráficos
> 
> Defina o [método de herança](../../../../glossary/glossary.md) do &#39;Modo de divisão em blocos gráficos&#39; [parâmetro base](../../../../glossary/glossary.md) como &#39;Absoluto&#39;, que permite definir o valor do parâmetro como &#39;Sem divisão em blocos gráficos&#39;:
> 
> ![](transformation-2d.resources/tilingmode.png)

>[!NOTE]
>
> Os valores de dimensionamento e rotação nas propriedades do nó são *relativos à transformação atual* e não são aplicados à Visualização 2D até você clicar no botão &#39;Aplicar&#39;.


## Parâmetros

|  |  |
| --- | --- |
| <b>Matriz de transformação</b> *Precisão decimal 4* | Abra a matriz de transformação subjacente para edição direta. Permite alterar a rotação e o dimensionamento. Também pode ser ajustado pelo gizmo no Visualização 2D.   Aviso: eles não se correlacionam diretamente com a exibição e são ajustes relativos que podem ser aplicados em etapas. |
| <b>Deslocamento</b> *Precisão decimal 2* | Define o deslocamento 2D da imagem. Permite que você altere a posição ou o deslocamento Também pode ser ajustado através do cursor no Visualização 2D.   Relaciona-se diretamente à saída Visualização 2D. |
| <b>Modo de mapa de mipmap</b> *Inteiro* | Permite alternar para um nível [mipmap](../../../../glossary/glossary.md) manual, que reduz artefatos em uma imagem usando a filtragem de textura. |
| <b>Nível do mipmap</b> *Inteiro* | Define o nível [mipmap](../../../../glossary/glossary.md) a ser usado.     *Disponível quando o &#39;Modo de mapa de mipmap&#39; estiver definido como &#39;Manual&#39;* |
| <b>Cor fosca</b> *Flutuante4* | A cor usada como plano de fundo quando a divisão em blocos gráficos da transformação está desativada. Ou seja, define a cor usada quando a entrada transformada não cobre uma área da saída.   Pode ser tornado transparente ao trabalhar com cores RGBA. |
| <b>Filtragem</b> *Inteiro* | Define o método de redução da resolução usado. Não funciona muito bem com a redução de Nível do mipmap. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Entrada</b> *Tons de Cinza/Cor* PRIMÁRIO | A imagem a ser transformada. |


## Exemplos

*Em breve.*
