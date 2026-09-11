---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-graph-view/node-alignment-tools.html"
breadcrumb-title: ''
description: Use ferramentas de alinhamento de nó para organizar e alinhar nós na visualização de gráfico para gráficos mais claros e legíveis.
helpx_creative_field: ""
helpx_description: Designer > Interface > The graph view > Node alignment tools
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ferramentas de alinhamento de nó
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 1%

---


# Ferramentas de alinhamento de nó

![Barra de ferramentas de alinhamento de nó](../../../assets/node-alignment-toolbar.png "Barra de ferramentas de alinhamento de nó"){zoomable="yes"}

As ferramentas de alinhamento de nós permitem organizar os nós em gráficos para melhorar a legibilidade e a experiência de criação. Eles oferecem ações para alinhar nós, distribuí-los uniformemente e encaixá-los na grade.

Eles atuam somente nos <b>nós atualmente selecionados</b>.

>[!NOTE]
>
> Atalhos do teclado
> 
> Algumas ações têm atalhos de teclado para acesso rápido: H, V e S. Eles são exibidos entre parênteses na lista de ações abaixo.
> 
> Observe que eles substituirão qualquer [atalho de teclado atribuído aos nós](../../../interface/preferences-window/preferences-window.md).

## Alinhamentos

Os nós podem ser alinhados horizontal e verticalmente, com três modos para cada eixo:

### Alinhamentos horizontais

<b>![](../../../assets/node-alignment-h-left.png) Esquerda:</b> Alinhe o lado esquerdo dos nós selecionados ao lado esquerdo do nó mais à esquerda.

<b>![](../../../assets/node-alignment-h-center.png) Centro (H):</b> Alinhe o centro horizontal dos nós selecionados ao centro horizontal da caixa delimitadora que os abrange.

<b>![](../../../assets/node-alignment-h-right.png) Direita:</b> Alinhe o lado direito dos nós selecionados ao lado direito do nó mais à direita.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ferramentas de alinhamento de nó: esquerda](../../../assets/node-alignment-left.gif "Ferramentas de alinhamento de nó: esquerda"){zoomable="yes"}

*Esquerda*

</td>
<td style="border: 0;" valign="top">

![Ferramentas de alinhamento de nó: centralizar](../../../assets/node-alignment-center.gif "Ferramentas de alinhamento de nó: centralizar"){zoomable="yes"}

*Centro*

</td>
<td style="border: 0;" valign="top">

![Ferramentas de alinhamento de nó: direita](../../../assets/node-alignment-right.gif "Ferramentas de alinhamento de nó: direita"){zoomable="yes"}

*Direita*

</td>
</tr>
</table>

### Alinhamentos verticais

<b>![](../../../assets/node-alignment-v-top.png) Superior:</b> Alinhe o lado superior dos nós selecionados ao lado superior do nó superior.

<b>![](../../../assets/node-alignment-v-middle.png) Médio (V):</b> Alinha o centro vertical dos nós selecionados ao centro vertical da caixa delimitadora que os abrange.

<b>![](../../../assets/node-alignment-v-bottom.png) Inferior:</b> Alinhe o lado inferior dos nós selecionados ao lado inferior do nó mais inferior.

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Ferramentas de alinhamento de nó: superior](../../../assets/node-alignment-top.gif "Ferramentas de alinhamento de nó: superior"){zoomable="yes"}

*Superior*

</td>
<td style="border: 0;" valign="top">

![Ferramentas de alinhamento de nó: intermediárias](../../../assets/node-alignment-middle.gif "Ferramentas de alinhamento de nó: intermediárias"){zoomable="yes"}

*Meio*

</td>
<td style="border: 0;" valign="top">

![Ferramentas de alinhamento de nós: parte inferior](../../../assets/node-alignment-bottom.gif "Ferramentas de alinhamento de nós: parte inferior"){zoomable="yes"}

*Inferior*

</td>
</tr>
</table>

### Empilhamento

A <b>opção ![](../../../assets/node-alignment-stack.png)Empilhar </b> permite <b>evitar qualquer sobreposição</b> ao usar alinhamentos. Ela fica ativada por padrão.

Quando ativado, os nós serão movidos o mais longe possível para a posição de referência até que colidam com outro nó na seleção. Isso os empilha efetivamente no eixo selecionado com uma margem de uma célula de grade média entre cada nó.

![Ferramentas de alinhamento de nó: empilhamento](../../../assets/node-alignment-stacking.gif "Ferramentas de alinhamento de nó: empilhamento"){zoomable="yes"}

## Distribuições

Os nós podem ser distribuídos uniformemente entre os nós em cada extremo da seleção atual no eixo desejado.

<b>![](../../../assets/node-alignment-distribute-h.png) Horizontalmente:</b> nós são distribuídos uniformemente entre os nós mais à esquerda e mais à direita na seleção.

<b>![](../../../assets/node-alignment-distribute-v.png) Verticalmente:</b> Os nós são distribuídos uniformemente entre os nós superiores e inferiores na seleção.

As distribuições visam o <b>espaçamento par</b> entre os nós, independentemente de seu tamanho.

Quando vários nós têm seus centros perfeitamente alinhados no eixo selecionado, eles permanecem e são <b>tratados como um</b> na distribuição. O *maior* dos nós alinhados é usado para calcular o espaçamento uniforme.

Observe que quando o tamanho total dos nós selecionados é maior que o espaço disponível no eixo selecionado, pode ocorrer sobreposição.

<table>
<tr style="border: 0;">
<td width="58.33%" style="border: 0;" valign="top">

![Ferramentas de alinhamento de nó: distribuição horizontal](../../../assets/node-alignment-distribute-h.gif "Ferramentas de alinhamento de nó: distribuição horizontal"){zoomable="yes"}

*Horizontalmente*

</td>
<td width="100.00%" style="border: 0;" valign="top">

![Ferramentas de alinhamento de nó: distribuição vertical](../../../assets/node-alignment-distribute-v.gif "Ferramentas de alinhamento de nó: distribuição vertical"){zoomable="yes"}

*Verticalmente*

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.33%" style="border: 0;" valign="top">

## Ajuste de grade

A ação <b>Encaixar (S) ![](../../../assets/node-alignment-snap.png)</b> move cada nó selecionado para que o canto superior esquerdo fique no ponto mais próximo da grade média.

</td>
<td width="100.00%" style="border: 0;" valign="top">

![Ferramentas de alinhamento de nó: ajuste de grade](../../../assets/node-alignment-snapping.gif "Ferramentas de alinhamento de nó: ajuste de grade"){zoomable="yes"}

</td>
</tr>
</table>
