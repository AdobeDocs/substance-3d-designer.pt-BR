---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/bitmap.html"
breadcrumb-title: ''
description: Use o nó Bitmap para importar e usar imagens bitmap como texturas em gráficos de composição de Substance.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Bitmap
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Bitmap
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 1%

---


# Bitmap

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: Bitmap](../../../../assets/comp_bitmap.png "Nó atômico: Bitmap"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Carrega um [recurso de bitmap](../../../../resources/bitmap-resource/bitmap-resource.md) no gráfico.

Este nó é usado para importar um [bitmap](../../../../glossary/glossary.md) para o seu gráfico ou para criar um novo bitmap a ser usado com as [ferramentas de pintura de bitmap](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md).

Existem algumas maneiras de criar este nó, e todas elas exigem que você entenda[ a diferença entre os recursos de vinculação e importação.](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)

</td>
</tr>
</table>

Você pode criar o nó do zero ou soltando um [bitmap](../../../../glossary/glossary.md) em um formato compatível na exibição Gráfico.

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
> Os bitmaps de 8 bits gerados ou importados podem ser pintados usando as [ferramentas de pintura de bitmaps](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md) no encaixe da [exibição 2D](../../../../interface/2d-view/2d-view.md).

>[!IMPORTANT]
>
> Este nó é dependente de um recurso externo, portanto, há alguns pontos a serem considerados ao trabalhar com eles:
> 
> * Os nós de bitmap podem retornar colorido ou em tons de cinza, mas o padrão é colorido mesmo que o recurso seja um bitmap em tons de cinza. Isso pode afetar o desempenho e a complexidade do gráfico, portanto, sempre mude para o [modo de cores](#parameters) &#39;Tons de cinza&#39; se necessário.
> * A exclusão de um nó de bitmap não exclui o [recurso de bitmap](../../../../resources/bitmap-resource/bitmap-resource.md) no [pacote](../../../../glossary/glossary.md). Isso precisa ser feito manualmente no [Explorer](../../../../interface/the-explorer-window/the-explorer-window.md).
> * Por outro lado, tenha cuidado ao excluir um [recurso de Bitmap](../../../../resources/bitmap-resource/bitmap-resource.md) no Explorer: ele ainda funcionará no gráfico dessa sessão, pois é mantido em cache, mas será marcado como ausente na próxima vez que você carregar o [pacote](../../../../glossary/glossary.md).
> * Quando um gráfico de Substance é [cozido](../../../../glossary/glossary.md), a resolução do bitmap será fixada em sua resolução dentro do gráfico e não com base em seu tamanho original. É recomendável verificar se o [parâmetro base](../../../../glossary/glossary.md) &#39;Tamanho de saída&#39; de um nó de Bitmap usa o [método de herança](../../../../glossary/glossary.md) &#39;Absoluto&#39;, e se o nó é seguido por um nó [Transformar 2D](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md) definido como &#39;Em relação ao pai&#39; (ou seja, a resolução do gráfico de host).

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Parâmetros

</td>
<td style="border: 0;" valign="top">

### Ferramentas de pintura de bitmap

</td>
<td style="border: 0;" valign="top">

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
| <b>Modo de cores</b> *Booleano* | Determina o tipo de saída do nó, para retornar em cor ou em escala de cinza. |
| <b>Caminho do recurso PKG</b> *Cadeia de Caracteres* | Caminho para o [recurso de bitmap](../../../../resources/bitmap-resource/bitmap-resource.md) que está sendo referenciado pelo nó.   É recomendável não digitar manualmente, mas copiar um recurso do explorador e colá-lo no campo de texto de parâmetro ou arrastar e soltar um recurso de bitmap diretamente do [Explorador](../../../../interface/the-explorer-window/the-explorer-window.md) no nó Bitmap do gráfico. |
| <b>Redimensionar método</b> *Inteiro* | O método de reamostragem a ser usado ao aumentar ou diminuir a escala de um bitmap:<ul data-preserve-html="true"> <li data-preserve-html="true"><i>Alongar suavemente:</i> aplique a [filtragem bilinear](../../../../glossary/glossary.md) para interpolar sobre os pixels de origem da imagem ampliada.</li> <li data-preserve-html="true"><i>Esticar mais próximo:</i> estica a imagem e usa a cor do pixel de origem mais próximo como está.</li> </ul> |

## Ferramentas de pintura de bitmap

Os bitmaps podem ser editados no Designer. Saiba mais sobre as ferramentas de edição em [esta seção](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md).

## Conectores de saída

|  |  |
| --- | --- |
| <b>Saída</b> *Tons de cinza/Cor* |  |

## Exemplos

*Em breve.*
