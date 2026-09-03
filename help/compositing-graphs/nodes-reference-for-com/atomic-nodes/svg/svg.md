---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/svg.html"
breadcrumb-title: ''
description: Use o nó SVG para importar e renderizar gráficos vetoriais SVG como texturas para criar elementos gráficos dimensionáveis.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > SVG
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SVG
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 1%

---


# SVG

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: SVG](svg.resources/svg-01.png "Nó atômico: SVG"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Renderiza uma [imagem SVG](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) como um bitmap. Em outras palavras, mapeia formas vetoriais em pixels.

Existem algumas maneiras de criar este nó, e todas elas exigem que você entenda[a diferença entre os recursos de vinculação e importação](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md).

</td>
</tr>
</table>

Você pode criar o nó do zero ou soltar um arquivo de SVG na visualização Gráfico.

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

>[!TIP]
>
> Imagens de SVG geradas ou importadas podem ser editadas por meio das [ferramentas de edição de vetores](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md) no encaixe da [exibição 2D](../../../../interface/2d-view/2d-view.md).

>[!IMPORTANT]
>
> Este nó é dependente de um recurso externo, portanto, há alguns pontos que devem ser lembrados ao trabalhar com eles:
> 
> * Os nós de SVG podem retornar cor ou tons de cinza, mas o padrão é a cor, mesmo que o recurso seja um vetor de tons de cinza. Isso pode afetar o desempenho e a complexidade do gráfico, portanto, sempre mude para o [modo de cores](#parameters) &#39;Tons de cinza&#39; se necessário.
> * A exclusão de um nó SVG não exclui o [recurso SVG](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) no [pacote](../../../../glossary/glossary.md). Isso precisa ser feito manualmente no [Explorer](../../../../interface/the-explorer-window/the-explorer-window.md).
> * As formas de SVG são [tesseladas](../../../../glossary/glossary.md) em geometria/polígonos e *rasterizadas* para serem usadas em gráficos de Substance como bitmaps. A tecnologia usada para essas operações não suporta várias propriedades vetoriais, como contornos. Saiba mais sobre essas limitações [aqui](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md).

>[!WARNING]
>
> As formas de SVG são [tesseladas](../../../../glossary/glossary.md) em geometria/polígonos e *rasterizadas* para serem usadas em gráficos de Substance como bitmaps.
> 
> A tecnologia usada para essas operações não suporta várias propriedades vetoriais, como contornos.
> 
> Saiba mais sobre essas limitações [aqui](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md).

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Exemplos

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## Parâmetros

|  |  |
| --- | --- |
| <b>Modo de cores</b> *Booleano* | Determina o tipo de saída do nó, para retornar em cor ou em escala de cinza. |
| <b>Cor do plano de fundo</b> *Cores/Tons de Cinza* | Define a cor de fundo da imagem de saída para usar em áreas não cobertas por uma forma vetorial.   *É substituído pela entrada &#39;[Background](#inputs)&#39; quando essa entrada está conectada.* |
| <b>Caminho do recurso PKG</b> *Cadeia de Caracteres* | Caminho para o [recurso SVG](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) que está sendo referenciado pelo nó.   É recomendável não digitar manualmente, mas copiar um recurso do explorador e colá-lo no campo de texto de parâmetro ou arrastar e soltar um recurso de bitmap diretamente do [Explorador](../../../../interface/the-explorer-window/the-explorer-window.md) para o nó SVG no gráfico. |

## Ferramentas de edição de vetor

Formas vetoriais podem ser editadas no Designer. Saiba mais sobre as ferramentas de edição em [esta seção](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md).

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Fundo</b> *Tons de Cinza/Cor* PRIMÁRIO | Define a cor de fundo da imagem de saída para usar em áreas não cobertas por uma forma vetorial.   *Substitui o parâmetro &#39;[Cor do plano de fundo](#parameters)&#39; quando conectado.* |

## Conectores de saída

|  |  |
| --- | --- |
| <b>Saída</b> *Tons de cinza/Cor* |  |

## Exemplos

*Em breve.*
