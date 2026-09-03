---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/fx-map.html"
breadcrumb-title: ''
description: Use o nó FX-Map para aplicar gráficos de função a texturas para criar efeitos e padrões de procedimento.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > FX-Map
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: FX-Map
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 2%

---


# FX-Map

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Nó atômico: FX-Map](fx-map.resources/fx-map-01.png "Nó atômico: FX-Map"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

O FX-Map pode replicar e subdividir uma imagem ou entrada de padrão várias vezes e controlar a distribuição de cada padrão graças a parâmetros e funções lógicas.

É um dos nós atômicos mais poderosos, bem como o nó mais complexo disponível na aplicação.

</td>
</tr>
</table>

Semelhante ao [processador de pixels](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md), cabe a você definir e criar as funções que determinam o comportamento e a saída deste nó.

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
> Consulte o [guia dedicado](../../../../function-graphs/fxmaps/fxmaps.md) para saber mais e entender mais sobre o processo FX-Map.

>[!IMPORTANT]
>
> É recomendável estar familiarizado com todos os aspectos do software e não ter problemas para criar [funções matemáticas](../../../../function-graphs/function-graphs.md) para os parâmetros antes de tentar usar o nó FX-Map.

## Exemplos

## Parâmetros

Lembre-se de que, diferentemente de outros nós, a maior parte do comportamento de um FX-Map não é determinada pelos parâmetros, mas [editando as funções FX-Map](../../../../function-graphs/fxmaps/fxmaps.md) dentro dele.

|  |  |
| --- | --- |
| <b>Modo de cores</b> *Booleano* | Alterna entre uma imagem em tons de cinza e uma imagem colorida de saída. A cor será muito mais lenta do que a escala de cinza. |
| <b>Fundo</b> *Flutuante/Flutuante4* | Define a cor inicial do plano de fundo na qual serão compostos os resultados. |
| <b>Região de renderização</b> *Flutuante4* | Permite definir o intervalo de pixels inicial para cada lado do FX-Map, resultando em um efeito de amplificação. |
| <b>Região de divisão</b> *Flutuante4* | Permite que você desloque a distância de divisão em blocos gráficos do FX-Map. |
| <b>Selecionar para fora</b> *Booleano* | Executa uma otimização por [remoção](../../../../glossary/glossary.md) de padrões que estão fora do intervalo normal. |
| <b>Aspereza</b> *Precisão decimal* | Funciona como um multiplicador de profundidade e opacidade. Isso aplica uma tendência ao processo de mesclagem do FX-map. |
| <b>Opacidade global</b> *Precisão decimal* | Define a opacidade global da saída do FX-map. |

## Guia do FX-Map

*Em breve.*

## Conectores de entrada

|  |  |
| --- | --- |
| <b>Fundo</b> *Tons de Cinza/Cor* PRIMÁRIO | A cor de plano de fundo da imagem de saída. |
| <b>Imagem de entrada #</b> *Tons de cinza/Cor* |  |

## Conectores de saída

|  |  |
| --- | --- |
| <b>Saída</b> *Tons de cinza/Cor* |  |

## Exemplos

![](fx-map.resources/fx-map-02.png)
