---
helpx_url: "https://helpx.adobe.com/br/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/input.html"
breadcrumb-title: ''
description: Use o nó Entrada para criar parâmetros de entrada para gráficos de Substance que podem ser expostos e ajustados pelos usuários.
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Input
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Entrada
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---


# Entrada

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Nó atômico: cor de entrada](../../../../assets/comp_inputcolor_1.png "Nó atômico: cor de entrada"){width="200px"}

</td>
<td style="border: 0;" valign="top">

![Nó atômico: escala de cinza de entrada](../../../../assets/comp_inputgrayscale_1.png "Nó atômico: escala de cinza de entrada"){width="200px"}

</td>
<td style="border: 0;" valign="top">

![Nó atômico: valor de entrada](../../../../assets/comp_inputnumeric_1.png "Nó atômico: valor de entrada"){width="200px"}

</td>
</tr>
</table>

Os nós de entrada são um tipo especial de nó que cria um slot dinâmico no gráfico, permitindo que qualquer entrada seja conectada quando o gráfico é usado em outro contexto.

Diferentemente dos [nós de saída](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md), você deve inserir explicitamente uma entrada Color, Grayscale ou Value. Não é possível criar suas próprias entradas “agnósticas” que alteram o tipo dependendo do que está conectado a elas.

Os nós de entrada não são tão cruciais quanto os [Nós de saída](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md): você pode ter Gráficos avançados em perfeito funcionamento que não precisam de uma Entrada. As entradas só são usadas quando você deseja basear o resultado de uma Instância de Gráfico ou nó em uma entrada externa, por exemplo, ao criar uma [Instância](../../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)ou um [Filtro](https://experienceleague.adobe.com/pt-br/docs/substance-3d-painter/using/effects/filter) para o Substance 3D Painter.

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

## PARÂMETROS

</td>
<td style="border: 0;" valign="top">

### ATRIBUTOS

</td>
<td style="border: 0;" valign="top">

### HERANÇA

</td>
<td style="border: 0;" valign="top">

### ATRIBUTOS DE INTEGRAÇÃO

</td>
</tr>
</table>

## Parâmetros

Por padrão, uma Cor de entrada ou Escala de cinza retorna preto se nada estiver conectado. Você pode definir um valor padrão diferente ou arrastar um[Recurso de Bitmap](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) existente do [Explorer](../../../../interface/the-explorer-window/the-explorer-window.md) para o nó de Entrada do gráfico, para visualizar esses dados no slot. Isso só funciona para Entradas coloridas e em tons de cinza. O valor padrão é persistente quando usado em outros contextos. O bitmap de visualização é descartado em todos os outros lugares.

Se quiser visualizá-lo com as saídas de outro gráfico, será necessário exportar o gráfico para bitmap no método acima ou usar a edição de “contexto interno”.

|  |  |
| --- | --- |
| <b>Caminho do recurso PKG</b> *Cadeia de Caracteres* | Aponta para um recurso de bitmap personalizado para visualização. |
| <b>Valor padrão</b> *Cor/Tons de Cinza/Valor* | Permite usar outro valor diferente de preto como entrada padrão, se nada estiver conectado a este slot. |

## Atributos

|  |  |
| --- | --- |
| <b>Identificador</b> *Cadeia de Caracteres* | O único Atributo obrigatório e exclusivo. Não pode conter espaços.   Esse é usado para rotular entradas se nenhum Rótulo estiver configurado e para diferenciar saídas diferentes. Não deixe apenas isso como “input\_1”! |
| <b>Descrição</b> *Cadeia de Caracteres* | Descrição opcional usada na biblioteca do Designer e na prateleira do Painter. |
| <b>Rótulo</b> *Cadeia de Caracteres* | Rótulo de interface usado para boa rotulagem na interface do Designer e Painter. Pode conter espaços.   Recomenda-se configurar com um nome semelhante à Identificador, apenas com barras de espaço em vez de sublinhados. |
| <b>Dados do usuário</b> *Cadeia de Caracteres* | Dados do usuário adicionais e opcionais que podem ser usados para operações de filtragem específicas, Basicamente um curinga, campo de dados personalizado. |
| <b>Grupo</b> *Cadeia de Caracteres* | Atributo de Grupo usado para agrupar entradas para os [Modos de Criação de Link](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md) do Designer.   Entradas com um Atributo de Grupo idêntico (diferencia maiúsculas de minúsculas) serão apresentadas como uma única conexão no Modo de Material Compacto. |

## Herança

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Quando várias entradas estão presentes, você precisa prestar atenção à maneira como o gráfico [herdará seus parâmetros Base](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) dessas entradas.\
Os parâmetros base incluem, entre outros, <b>Tamanho de Saída</b>, <b>Formato de Saída</b> e <b>Modo Revestimento</b>.

</td>
<td width="33.33%" style="border: 0;" valign="top">

[![Entrada primária no Substance](../../../../assets/node-primary-input.png)](https://helpx.adobe.com/Primary%20input%20in%20Substance%20graph)

</td>
</tr>
</table>

Uma entrada pode ser definida como a [Entrada primária](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md). Essa entrada, em seguida, orienta os atributos de todas as entradas cujo método de herança está definido como *Relativo ao pai*. Este é o método de herança *definido por padrão* nos nós de entrada.

Você pode definir um nó de entrada como a entrada Primária de um gráfico clicando em *RMB* no nó e selecionando a opção <b>Definir como entrada Primária</b> no menu contextual.\
A entrada Primária de um nó está marcada com um *pequeno ponto escuro no conector* (circulado em vermelho no exemplo ao lado desta seção).

Como alternativa, qualquer entrada definida para o método de herança *Relativo à entrada* herdará os atributos do nó ao qual está conectado, *independentemente* da entrada Primária.

Finalmente, você pode substituir qualquer valor de um determinado atributo definindo seu método de herança como *Absoluto*.

>[!TIP]
>
> Para saber mais sobre herança, vá para a página [Herança em gráficos de Substance](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md) desta documentação.

>[!IMPORTANT]
>
> O método de herança *Relativo à entrada* para nós de entrada *não tem suporte* em [Ativos do Substance 3D (SBSAR)](https://helpx.adobe.com/br/substance-3d-assets.html). Defina todos os métodos de herança dos nós de entrada como *Relativo ao pai* antes de publicar o pacote.

## Atributos de integração

As entradas não são enviadas diretamente ao Visualização 3D, mas seus Atributos de Uso são usados pelo [Substance 3D Painter](https://experienceleague.adobe.com/pt-br/docs/substance-3d-painter/using/home) para preencher automaticamente slots com certos mapas (usados principalmente com [Filtros](https://experienceleague.adobe.com/pt-br/docs/substance-3d-painter/using/effects/filter)).

Além disso, os atributos de Uso também são usados com os [Modos de Criação de Link](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md), para corresponder aos slots de entrada e saída corretos.

<b>Uso</b>

|  |  |
| --- | --- |
| <b>Componente</b> *Cadeia de Caracteres* | Isso determina quais canais estão realmente na entrada resultante.   Essa é uma configuração herdada que não é mais usada por integrações e gráficos. |
| <b>Uso</b> *Cadeia de Caracteres* | Defina um tipo ou uso para esta entrada. Indica como outros nós devem se conectar a essa entrada. |
| <b>Espaço de cores</b> *Cadeia de Caracteres* | Define o espaço de cores no qual esta entrada deve ser interpretada. |
