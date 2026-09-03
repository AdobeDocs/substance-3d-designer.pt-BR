---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blend.html"
breadcrumb-title: ''
description: Use o nó Combinar para mesclar duas texturas usando vários modos de mesclagem para criar efeitos compostos.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Misturar
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 9%

---


# Misturar

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: Combinar](blend.resources/blend-01.png "Nó atômico: Combinar"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Combina duas imagens usando um modo de mesclagem especificado e uma máscara opcional.

É o nó mais útil de todos os nós Atômicos, quase todos os Gráficos que você criar no [Substance 3D Designer](https://www.adobe.com/br/products/substance3d-designer.html) usarão esse nó.

</td>
</tr>
</table>

Sua funcionalidade é semelhante a ter duas camadas acima uma da outra no [Substance 3D Painter](https://www.adobe.com/br/products/substance3d-painter.html) ou no [Photoshop](https://www.adobe.com/ch_fr/products/photoshop/landpa.html), que se mesclam pelo modo de mesclagem definido na camada superior.

>[!TIP]
>
> Saiba mais sobre os modos de mesclagem disponíveis no nó Combinar em [esta página dedicada](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blending-modes-des/blending-modes-description.md).

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

## Conectores de saída

</td>
<td style="border: 0;" valign="top">

### Exemplos

</td>
</tr>
</table>

## Parâmetros

|  |  |
| --- | --- |
| <b>Opacidade</b> *Precisão decimal* | Opacidade da mesclagem da camada de primeiro plano no plano de fundo. Ele funciona independentemente da entrada de Opacidade e atua como um multiplicador adicional para ele. |
| <b>Modo de mesclagem</b> *Inteiro* [Estático](../../../../glossary/glossary.md) | Define a operação de mesclagem a ser usada.   Consulte a [página dedicada sobre modos de mesclagem](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blending-modes-des/blending-modes-description.md). |
| <b>Mesclagem de alfa</b> *Inteiro* [Estático](../../../../glossary/glossary.md) | Determina o comportamento de mesclagem quando as entradas de cor têm canais Alfa:<ul data-preserve-html="true"> <li data-preserve-html="true">Usar alfa de origem</li> <li data-preserve-html="true">Ignorar alfa</li> <li data-preserve-html="true">Mesclagem alfa direta</li> <li data-preserve-html="true">Mesclagem alfa pré-multiplicada</li> </ul> |
| <b>Área de corte</b> *Precisão decimal 4* [Estática](../../../../glossary/glossary.md) | Permitir a configuração de uma região de corte personalizada que se comporte como uma máscara de Opacidade adicional. Qualquer área cortada mostra apenas o plano de fundo. |

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Primeiro Plano</b> *Tons de cinza/Cor* | Camada superior ou de primeiro plano da operação Combinar. |
| <b>Fundo</b> *Tons de Cinza/Cor* PRIMÁRIO | Camada inferior ou de plano de fundo da operação de mesclagem. |
| <b>Opacidade</b> *Tons de cinza* | Entrada opcional de máscara de Alpha. |

>[!IMPORTANT]
>
> Os nós de Combinar têm entradas dinâmicas que alternam entre Tons de Cinza e Cor, dependendo de suas conexões.<b> Um nó Combinar só pode mesclar duas entradas do mesmo tipo </b>.
> 
> Conectar uma entrada Colorida e em Tons de Cinza ao Primeiro Plano e ao Plano de Fundo resultará em uma linha de conexão tracejada vermelha, significando um erro de cálculo.
> 
> Esta é a razão principal pela qual os novos usuários têm problemas com conexões coloridas vs. tons de cinza: certifique-se de que ambas as conexões sejam do mesmo tipo!

## Conectores de saída

|  |  |
| --- | --- |
| <b>Saída</b> *Tons de cinza/Cor* |  |

## Exemplos

*Em breve.*
