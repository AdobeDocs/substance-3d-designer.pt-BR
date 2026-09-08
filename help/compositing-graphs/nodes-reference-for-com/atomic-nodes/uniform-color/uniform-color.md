---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/uniform-color.html"
breadcrumb-title: ''
description: Use o nó de Cor uniforme para gerar texturas de cor uniforme para criar preenchimentos de cores sólidas e camadas base.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Uniform color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Cor uniforme
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 8%

---


# Cor uniforme

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: Cor uniforme](../../../../assets/comp_uniform_1.png "Nó atômico: Cor uniforme"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Gera um valor plano de tons de cinza ou de cor.

É um nó simples que é usado com frequência como ponto de partida para adicionar cores ou criar valores específicos.

</td>
</tr>
</table>

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
> Otimização de desempenho
> 
> Esses dois ajustes reduzem o tempo de computação e o espaço de memória do nó:
> 
> * Se for necessário um valor de tons de cinza, certifique-se de alternar o [modo de cores](#parameters) do nó para &#39;Tons de Cinza&#39;.
> * Como a saída do nó é uma cor sem graça, você pode usar a menor resolução possível. Defina o parâmetro &#39;[Tamanho de saída](../../../../compositing-graphs/output-size/output-size.md)&#39; do nó para usar o [método de herança](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) &#39;Absoluto&#39; e uma resolução de 16x16 pixels.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Parâmetros

</td>
<td style="border: 0;" valign="top">

### Conectores de saída

</td>
<td style="border: 0;" valign="top">

### Exemplos

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## Parâmetros

|  |  |
| --- | --- |
| <b>Modo de cores</b> *Booleano* | Alterna entre uma imagem em tons de cinza e uma imagem colorida de saída. |
| <b>Cor de saída</b> *Precisão decimal/Precisão decimal 4* | Seleciona a cor uniforme a ser usada na imagem de saída.   Ao usar o modo de cores “Cor”, o canal Alfa é usado para opacidade, em que 0 é totalmente transparente e 1 é totalmente opaco. |

## Conectores de saída

|  |  |
| --- | --- |
| <b>Saída</b> *Cores/Tons de Cinza* |  |

## Exemplos

*Em breve.*
