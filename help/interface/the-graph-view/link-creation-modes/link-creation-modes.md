---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-graph-view/link-creation-modes.html"
breadcrumb-title: ''
description: Saiba mais sobre os modos de criação de links na visualização de gráfico do Substance 3D Designer para conectar nós de maneira eficiente.
helpx_creative_field: ""
helpx_description: Designer > Interface > The graph view > Link creation modes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Modos de criação de link
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0b8b2d2c05587d7fe84a71bb54244a492540d6dc
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---


# Modos de criação de link

Em [gráficos de Substance](../../../compositing-graphs/substance-compositing-graphs.md), você pode conectar nós usando um dos 3 <b>modos de criação de link</b>:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Modo de criação do link: padrão](../../../assets/link-creation-mode-standard.gif "Modo de criação do link: padrão"){zoomable="yes"}

*Clique para ampliar*

<b>![](../../../assets/image2020-10-6-19-40-25.png) Padrão</b> (1)

Nenhuma condição é aplicada.

</td>
<td style="border: 0;" valign="top">

![Modo de criação do link: material](../../../assets/link-creation-mode-material.gif "Modo de criação do link: material"){zoomable="yes"}

*Clique para ampliar*

![](../../../assets/image2020-10-6-17-11-20.png) <b>Material</b> (2)

As entradas e as saídas são comparadas com base em seus usos.

Se apenas um dos dois tiver um uso, a conexão será executada como no modo Padrão.

</td>
<td style="border: 0;" valign="top">

![Modo de criação do link: material compacto](../../../assets/link-creation-mode-compact-material.gif "Modo de criação do link: material compacto"){zoomable="yes"}

*Clique para ampliar*

![](../../../assets/image2020-10-6-19-40-46.png) <b>Material Compacto</b> (3)

Igual ao material.

Entradas e saídas pertencentes a um mesmo *grupo* estão recolhidas.

</td>
</tr>
</table>

Você pode alternar entre os modos a qualquer momento na barra de ferramentas do gráfico clicando no botão ![](../../../assets/link-creation-mode.png) <b>Modo de criação do link</b> ou nos atalhos de teclado listados acima.

Nos modos <b>Material</b> e <b>Material Compacto</b>, conexões entre entradas e saídas com *usos não correspondentes* são proibidas.

## Os modos

|  | <div><img data-preserve-html="true" height="23" src="../../../assets/image2020-10-6-19-40-25.png"/></div> Padrão | <div><img data-preserve-html="true" height="23" src="../../../assets/image2020-10-6-17-11-20.png"/></div> Compactar | <div><img data-preserve-html="true" height="23" src="../../../assets/image2020-10-6-19-40-46.png"/></div> Material compacto |
| --- | --- | --- | --- |
| <b>Entradas</b> | Todas as entradas são visíveis | Todas as entradas são visíveis | Apenas 1 entrada por grupo |
| <b>Saídas</b> | Todas as saídas são visíveis | Todas as saídas são visíveis | Somente 1 saída por grupo |
| <b>Links</b> | Todos os vínculos estão visíveis | Todos os vínculos estão visíveis | Somente 1 link por grupo (verde) |
| <b>Conexões</b> | Você conecta os links um por um | Você conecta os vínculos em conjunto como um grupo de materiais de vínculo múltiplo com base nos usos correspondentes.   Quando um uso está presente em uma extremidade, a conexão é padrão. | Você conecta os vínculos em conjunto como um grupo de materiais de vínculo único. |

## Atribuição de grupos

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Você deve atribuir grupos aos nós <b>Entrada</b> e <b>Saída</b> do gráfico para usar os modos <b>Material</b> e <b>Material compacto</b>.

Atribua um grupo nos parâmetros <b>Atributos</b> do nó, preenchendo o nome do grupo na propriedade <b>Grupo</b>. Um grupo pode ser qualquer valor de cadeia de caracteres e os links serão agrupados se compartilharem o *mesmo*, nome de grupo que diferencia maiúsculas de minúsculas.

Entradas e saídas agrupadas de um gráfico são denotadas visualmente por serem *delimitadas em uma cápsula escura* em instâncias de nó que fazem referência a esse gráfico.

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Agrupar cápsula no nó](../../../assets/link-creation-mode-group-node.png "Agrupar cápsula no nó"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">

![Atributo de grupo](../../../assets/link-creation-mode-group.png "Atributo de grupo"){zoomable="yes"}

*Clique para ampliar*

</td>
<td width="25.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

## Correspondência de link com uso

Depois que os vínculos são agrupados, as entradas individuais precisam ser correspondidas com as saídas. Isso é feito por meio do atributo <b>Uso</b> dos nós <b>Entrada</b> e <b>Saída</b>. Se o uso entre a entrada e a saída *corresponder*, um link será criado. Se nenhum uso correspondente for encontrado, nenhum link será criado.

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">

![Atributo de uso](../../../assets/link-creation-mode-usage.png "Atributo de uso"){zoomable="yes"}

*Clique para ampliar*

</td>
<td width="25.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>
